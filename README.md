# 声占い ✨ 大阪のおばちゃん鑑定所

ブラウザだけで動く静的Webアプリです。録音音声は端末内で処理され、サーバーへは送信しません。

## すぐ試す（自分のPC）

```bash
cd voice-fortune
python -m http.server 8765
```

ブラウザで `http://127.0.0.1:8765/index.html` を開いてください。

## たくさんの人に配る（無料・おすすめ：GitHub Pages）

1. [GitHub](https://github.com) で新しいリポジトリを作成する（空でOK）。
2. このフォルダで Git を初期化し、`main` ブランチで push する。

   ```bash
   git init
   git add index.html fortunes.js .github README.md .gitignore
   git commit -m "Initial commit: 声占いアプリ"
   git branch -M main
   git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
   git push -u origin main
   ```

3. リポジトリの **Settings → Pages** を開く。
4. **Build and deployment** の **Source** で **GitHub Actions** を選ぶ。
5. 1〜2分後、`https://あなたのユーザー名.github.io/リポジトリ名/` に公開されます。  
   アプリのURLは **`.../index.html`** でも **`.../`**（`index.html` が自動表示）でも利用できます。

### QRコード

公開URLを [QRコード生成ツール](https://www.google.com/search?q=QR%E3%82%B3%E3%83%BC%E3%83%89+%E7%84%A1%E6%96%99) に貼り、印刷・スライドに載せると対面配布に便利です。

## デモ動画（15秒）台本サンプル

| 秒 | 画面 |
|----|------|
| 0–3 | タイトル「声占い」→マイクタップ |
| 3–8 | 録音カウントダウン→結果表示のドキドキ部分 |
| 8–15 | おもしろ結果の一瞬＋「URLは概要欄」など一言 |

## ファイル構成

| ファイル | 説明 |
|----------|------|
| `index.html` | メインUI・録音・表示 |
| `fortunes.js` | 占いパターンデータ |
| `手順書.html` | 鑑定パターン追加の手引き |
