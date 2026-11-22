# SNS SafeArea Preview — ダウンロード

After Effects のプレビューに、TikTok / YouTube Shorts / Instagram Reels / X の UI とセーフエリア（危険エリア・警告エリア）を重ねて確かめる Windows 用のツールです。

- このリポジトリには、アプリのインストーラーだけを置いています（ソースコードはありません）。
- テンプレートの新しい版と UI のズレの報告は [ae-sns-preview-packs](https://github.com/catwalking22/ae-sns-preview-packs) です。

## 動く環境

- Windows 10（1809 以降）/ 11 の 64 ビット
- After Effects 2024 以降
- アプリは外部と通信しません（自動更新もありません）。

## 入れ方

1. [Releases](https://github.com/catwalking22/ae-sns-preview-download/releases/latest) の「Assets」から `SNSPreviewSetup-<版>.exe` をダウンロードします。
2. After Effects などの Adobe のアプリを終了してから、ダウンロードしたファイルを実行します。
3. 「Windows によって PC が保護されました」と出ることがあります（コード署名をしていないためです）。「詳細情報」を押し、発行元が「不明な発行元」であることを確かめてから「実行」を押してください。
4. 管理者の権限を求められます（After Effects 用のプラグインを入れるためです）。
5. After Effects の「編集 → 環境設定 → ビデオ」で Mercury Transmit を有効にし、出力先で「SNS SafeArea Preview」を選びます。

最初のテンプレートはインストーラーに入っています。

### ファイルが本物か確かめる（任意）

各リリースに SHA-256 を載せています。PowerShell で次を実行し、同じ値か確かめてください。

```powershell
Get-FileHash .\SNSPreviewSetup-<版>.exe -Algorithm SHA256
```

## アンインストール

「設定 → アプリ → インストールされているアプリ」から「SNS SafeArea Preview」をアンインストールします。テンプレート・マイテンプレート・設定（`%LocalAppData%\SNSPreviewViewer`）は残ります。不要なら手で削除してください。

## 注意

- 各 SNS の名称は、それぞれの会社の商標です。このツールは各社とは関係がありません。
