# 実行ファイルのPGP署名を確認する

結論: WindowsではKleopatraで確認します。

`.exe` と `.exe.asc` を同じフォルダーに置き、`.exe.asc` をKleopatraへドラッグ&ドロップします。
赤いエラーが出たら、その `.exe` は実行しません。

Kleopatraを入れていない場合は、先にこちらを読んでください。

- [Kleopatraとは](./about.md)
- [Gpg4winを取得してインストールする](./install.md)

## 手順

1. 配布元の公開鍵をKleopatraにインポートします。
2. 本体ファイルと `.asc` を同じフォルダーに置きます。
3. `.asc` をKleopatraへドラッグ&ドロップして結果を見ます。

Windowsでは、PGP署名の確認にKleopatraというアプリがよく使われます。
KleopatraはGpg4winに含まれています。

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
