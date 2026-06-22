# KleopatraでPGP署名を確認する

本体ファイルと `.asc` 署名ファイルをKleopatraで確認します。
**赤いエラーが出たら実行しません。**

初めて使う場合は、先に次のページを読んでください。

- [Kleopatraとは](./about.md)
- [Gpg4winを取得してインストールする](./install.md)

## 手順

1. 配布元の公開鍵をKleopatraにインポートします。
2. 本体ファイルと `.asc` を同じフォルダーに置きます。
3. `.asc` をKleopatraへドラッグ&ドロップして結果を見ます。

## 結果の見方

| 表示 | 判断 |
| --- | --- |
| 署名が合っている | 実行してよい可能性が高いです。 |
| 黄色い注意 | Fingerprintを確認します。 |
| 赤いエラー / Bad / Invalid signature | 実行しません。 |

## hato.lifeの鍵

[公開鍵ページ](../public/index.md)から取得します。用途に合うFingerprintを確認してください。

| 用途 | Fingerprint |
| --- | --- |
| コミット用 | `A2563716E50215E25B75E4EEF6033F2A3D70179C` |
| CIリリース用 | `BE40AA8D082F493F613BC07221DC34861B40E77D` |

## MySQLの例

`MySQL Release Engineering` を探し、Key-IDまたはFingerprintが `5072E1F5` であることを確認します。

例:

- `mysql-installer-community-8.0.29.msi`
- `mysql-installer-community-8.0.29.msi.asc`

この2つを同じフォルダーに置き、`.asc` をKleopatraで確認します。

参考: [MySQL公式ドキュメント](https://dev.mysql.com/doc/refman/8.0/ja/checking-gpg-signature-windows.html)
