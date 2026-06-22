# PGP確認ガイド

Windowsでダウンロードしたファイルが本物か確認するための短いガイドです。

- [Kleopatraで署名を確認する](./Kleopatra/index.md)
- [hato.lifeのPGP公開鍵](./public/index.md)

確認で見るものは、主に次の2つです。

1. 本体ファイルと `.asc` 署名ファイルが合っているか
2. 署名に使われた公開鍵のFingerprintが正しいか

赤いエラー、`Bad`、`Invalid signature` が出たファイルは実行しません。
