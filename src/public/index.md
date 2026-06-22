# hato.lifeのPGP公開鍵

インポート前にFingerprint全体が一致しているか確認してください。

| 用途 | Fingerprint | リンク |
| --- | --- | --- |
| コミット用 | `A2563716E50215E25B75E4EEF6033F2A3D70179C` | [Fingerprint](https://keys.openpgp.org/search?q=A2563716E50215E25B75E4EEF6033F2A3D70179C) / [メール](https://keys.openpgp.org/search?q=poppo@hato.life) / [asc](https://keys.openpgp.org/vks/v1/by-fingerprint/A2563716E50215E25B75E4EEF6033F2A3D70179C) |
| CIリリース用 | `BE40AA8D082F493F613BC07221DC34861B40E77D` | [Fingerprint](https://keys.openpgp.org/search?q=BE40AA8D082F493F613BC07221DC34861B40E77D) / [メール](https://keys.openpgp.org/search?q=release-signing@hato.life) / [asc](https://keys.openpgp.org/vks/v1/by-fingerprint/BE40AA8D082F493F613BC07221DC34861B40E77D) |

Kleopatraでは、取得した `.asc` をドラッグ&ドロップしてインポートします。

実行ファイルのチェックはCIリリース用を使用します。

## exeの署名をCIリリース用で確認する

hato.lifeのリリースで配布される `.exe` は、CIリリース用の公開鍵で確認します。

1. CIリリース用の [asc](https://keys.openpgp.org/vks/v1/by-fingerprint/BE40AA8D082F493F613BC07221DC34861B40E77D) を取得します。
2. 取得した公開鍵をKleopatraへドラッグ&ドロップしてインポートします。
3. 表示されたFingerprintが `BE40AA8D082F493F613BC07221DC34861B40E77D` と一致するか確認します。
4. リリースページから `.exe` と `.exe.asc` を同じフォルダーに保存します。
5. `.exe.asc` をKleopatraへドラッグ&ドロップします。
6. 署名者のFingerprintがCIリリース用と一致し、赤いエラーがなければ確認完了です。

赤いエラー、`Bad`、`Invalid signature` が出た場合は、その `.exe` を実行しないでください。
