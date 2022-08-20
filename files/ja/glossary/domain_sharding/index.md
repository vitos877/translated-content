---
title: Domain sharding (ドメインシャーディング)
slug: Glossary/Domain_sharding
tags:
  - DNS
  - Glossary
  - HTTP
  - Reference
  - Web Performance
  - latency
translation_of: Glossary/Domain_sharding
---
ブラウザはアクティブな接続数をドメインごとに制限します。この制限を超えてアセットを同時ダウンロードできるようにするために、**ドメインシャーディング**はコンテンツを複数のサブドメインに分割します。複数のアセットを提供するために複数のドメインが使用されると、ブラウザはより多くのリソースを同時にダウンロードすることができるため、より速いページ読み込み時間とユーザ体験の向上をもたらします。

ドメインシャーディングの性能面での問題は各ドメインの DNS ルックアップの追加コストと各 TCP コネクション確立のオーバヘッドです。

HTTP からの初回レスポンスは通常、 JavaScript、 CSS、画像、その他ダウンロードの必要なメディアファイルが列挙された HTML ファイルです。ブラウザはドメインごとにアクティブな接続数を制限するため、 1 ドメインからの全ての必要リソースの提供は、アセットが順番にダウンロードされることになり、遅くなることがあります。ドメインシャーディングでは必要なダウンロードは 2 つ以上のドメインから提供され、ブラウザでの必要なリソースの同時ダウンロードを可能にします。しかし、複数のドメインを用いることは DNS ルックアップが初回ロード時間を遅くするため、アンチパターンと言えます。

HTTP2 は無制限の同時リクエストをサポートしているため、 HTTP/2 が有効な場合にはドメインシャーディングはもはや必要なくなります。

## 詳細情報

- [Transport Layer Security (TLS)](/ja/docs/Archive/Security/SSL_and_TLS)
- [DNS](/ja/docs/Glossary/DNS)
- [HTTP/2](/ja/docs/Glossary/HTTP_2)