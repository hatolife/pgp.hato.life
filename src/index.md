# PGP確認ガイド

結論: Windowsで実行ファイルのPGP署名を確認するなら、Kleopatraを使います。

- [実行ファイルのPGP署名を確認する](./Kleopatra/index.md)
- [hato.lifeのPGP公開鍵](./public/index.md)

見るものは2つだけです。

1. 本体ファイルと `.asc` 署名ファイルが合っているか
2. 署名に使われた公開鍵のFingerprintが正しいか

赤いエラー、`Bad`、`Invalid signature` が出たファイルは実行しません。
