---
title: async を使用した非同期フロー制御
slug: Learn/Server-side/Express_Nodejs/Displaying_data/flow_control_using_async
tags:
  - Express
  - Node
  - displaying data
  - part 5
  - server-side
---
_LocalLibrary_ 中のいくつかのコントローラーのコードは、複数の非同期リクエストの結果に依存しています。そのため、操作を特定の順序もしくは並列して実行することが必要になる場合があります。フロー制御を管理して、必要となるすべての情報を取得した後でページをレンダリングするために、ここでは人気のある node [async](https://www.npmjs.com/package/async) を使うことにします。

> **Note:** JavaScript で非同期動作やフロー制御を管理する手法には [Promises](/ja/docs/Web/JavaScript/Guide/Using_promises) のような比較的最近 JavaScript に導入された言語機能を含め、他にもあります。

async には多くの便利なメソッドがあります（詳しくは [the documentation](https://caolan.github.io/async/v3/docs.html) を参照してください）。ここでは重要ないくつかの関数を紹介します。

- [`async.parallel()`](https://caolan.github.io/async/v3/docs.html#parallel) は、並列して行う必要のある操作を実行する場合に使用します。
- [`async.series()`](https://caolan.github.io/async/v3/docs.html#series) は、非同期操作が直列に実行される必要がある場合に使用します。
- [`async.waterfall()`](https://caolan.github.io/async/v3/docs.html#waterfall) は、直列に実行する必要がある操作の中でも、各操作が前の操作の結果に依存する場合に使用します。

## なぜ非同期フロー制御が必要なのか？

_Express_ で使用するメソッドの多くは非同期です。なので実行する操作を指定して、コールバックを渡します。メソッドはすぐに戻り、そしてコールバックは要求された操作が完了したときに呼び出されます。_Express_ の慣例として、コールバック関数は第 1 引数にエラー値 (成功時には `null`)、第 2 引数には関数からの結果 (存在する場合のみ) を渡します。

もしコントローラーがページのレンダリングに必要な情報を得るために **1 つの非同期操作**を実行するだけならば、実装は簡単です。コールバックでテンプレートをレンダリングするだけです。以下のコードでは、`SomeModel` モデルのカウントをレンダリングする関数 (Mongoose の [`countDocuments`](https://mongoosejs.com/docs/api.html#model_Model.countDocuments) メソッドを使用) を示しています。

```js
exports.some_model_count = function(req, res, next) {

  SomeModel.countDocuments({ a_model_field: 'match_value' }, function (err, count) {
    // ... エラーが発生した場合

    // 成功したら count を render 関数に渡して結果をレンダリングする (ここでは変数 'data')
    res.render('the_template', { data: count } );
  });
}
```

では**複数**の非同期クエリを実行する必要があり、すべての操作が完了するまでページをレンダリングできない場合はどうすればよいでしょうか？甘い考えで実装するとリクエストを「デイジーチェーン」して、前のリクエストのコールバックで後続のリクエストを開始し、最後のコールバックでレスポンスを受け取ってレンダリングすることができます。この方法の問題点は並列で実行した方が効率的である場合でも、リクエストを直列で実行する必要がある点です。これにより一般的に[コールバック地獄](http://callbackhell.com/)と呼ばれる複雑にネストされたコードになる可能性があります。

より良い解決策はすべてのリクエストを並列で実行して、すべてのクエリが完了したときに実行される単一のコールバックを持つことです。そして、そのようなフロー操作を簡単に行うことができるのが _async_ モジュールなのです！

## 非同期操作の並列化

[`async.parallel()`](https://caolan.github.io/async/v3/docs.html#parallel) メソッドは、複数の非同期処理を並列で実行するために使用されます。

`async.parallel()` の第 1 引数は実行する非同期関数 (配列、オブジェクト、またはその他の反復可能なもの) のコレクションです。各関数には `callback(err, result)` が渡され、完了時にはエラー `err` (もしくは `null`) と任意で `results` 値を指定して呼び出す必要があります。

`async.parallel()` の任意の第 2 引数は、第 1 引数のすべての関数が完了したときに実行されるコールバックです。このコールバックはエラー引数と個々の非同期操作の results を含む result コレクションを使用して呼び出されます。result コレクションは最初の引数と同じ型です (つまり非同期関数の配列を渡す場合、最終的なコールバックは results の配列で呼び出されます)。並列関数のいずれかがエラーを返した場合、コールバックは (エラー値とともに) 早期に呼び出されます。

以下の例では第 1 引数にオブジェクトを渡した場合の動作を示しています。この例から分かるように results は渡された元の関数と同じプロパティ名を持つオブジェクトで**返されます**。

```js
async.parallel({
  one: function(callback) { ... },
  two: function(callback) { ... },
  ...
  something_else: function(callback) { ... }
  },
  // 任意のコールバック
  function(err, results) {
    // 'results' が {one: 1, two: 2, ..., something_else: some_value} になりました
  }
);
```

代わりに関数の配列を第 1 引数として渡すと、results は配列になります (results に入る配列の順序は関数が完了した順番ではなく、関数が宣言された元の順番と一致します)。

## Asynchronous operations in series

The method [`async.series()`](https://caolan.github.io/async/v3/docs.html#series) is used to run multiple asynchronous operations in sequence, when subsequent functions do not depend on the output of earlier functions. It is essentially declared and behaves in the same way as `async.parallel()`.

```js
async.series({
  one: function(callback) { ... },
  two: function(callback) { ... },
  ...
  something_else: function(callback) { ... }
  },
  // optional callback after the last asynchronous function completes.
  function(err, results) {
    // 'results' is now equal to: {one: 1, two: 2, ..., something_else: some_value}
  }
);
```

> **Note:** The ECMAScript (JavaScript) language specification states that the order of enumeration of an object is undefined, so it is possible that the functions will not be called in the same order as you specify them on all platforms. If the order really is important, then you should pass an array instead of an object, as shown below.

```js
async.series([
  function(callback) {
    // do some stuff ...
    callback(null, 'one');
  },
  function(callback) {
    // do some more stuff ...
    callback(null, 'two');
  }
 ],
  // optional callback
  function(err, results) {
  // results is now equal to ['one', 'two']
  }
);
```

## Dependent asynchronous operations in series

The method [`async.waterfall()`](https://caolan.github.io/async/v3/docs.html#waterfall) is used to run multiple asynchronous operations in sequence when each operation is dependent on the result of the previous operation.

The callback invoked by each asynchronous function contains `null` for the first argument and results in subsequent arguments. Each function in the series takes the results arguments of the previous callback as the first parameters, and then a callback function. When all operations are complete, a final callback is invoked with the result of the last operation. The way this works is more clear when you consider the code fragment below (this example is from the _async_ documentation):

```js
async.waterfall([
  function(callback) {
    callback(null, 'one', 'two');
  },
  function(arg1, arg2, callback) {
    // arg1 now equals 'one' and arg2 now equals 'two'
    callback(null, 'three');
  },
  function(arg1, callback) {
    // arg1 now equals 'three'
    callback(null, 'done');
  }
], function (err, result) {
  // result now equals 'done'
}
);
```

## Installing async

Install the async module using the NPM package manager so that we can use it in our code. You do this in the usual way, by opening a prompt in the root of the _LocalLibrary_ project and entering the following command:

```bash
npm install async
```

## Next steps

- Return to [Express Tutorial Part 5: Displaying library data](/en-US/docs/Learn/Server-side/Express_Nodejs/Displaying_data).
- Proceed to the next subarticle of Part 5: [Template primer](/en-US/docs/Learn/Server-side/Express_Nodejs/Displaying_data/Template_primer).