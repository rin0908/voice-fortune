# 声占い ✨ 大阪のおばちゃん鑑定所

ブラウザだけで動く静的Webアプリです。録音音声は端末内で処理され、サーバーへは送信しません。

## すぐ試す（自分のPC）

プロジェクトのフォルダに移動してから、次を実行します。

```bash
python -m http.server 8765
```

ブラウザで `http://127.0.0.1:8765/index.html` を開いてください。

**ターミナルでフォルダに移動する例**

| 使っているシェル | コマンド例 |
|------------------|------------|
| **Git Bash（MINGW64）** | `cd /c/Users/heart/voice-fortune` |
| **PowerShell / CMD** | `cd c:\Users\heart\voice-fortune` |

※ `cd voice-fortune` は、**すでにそのひとつ上のフォルダにいるときだけ**使えます。迷ったら上の「フルパス」をコピーしてください。

---

## 【コピペ用】書き換えなし（このプロジェクト名のとき）

**自分のGitHubが `rin0908` で、リポジトリ名が `voice-fortune` の場合だけ**、下は **そのままコピー＆貼り付けでOK** です（中身を編集しないでください）。

### みんなに見せるページの住所（ブラウザのアドレス欄用）

```text
https://rin0908.github.io/voice-fortune/
```

### Git Bash で「フォルダに入る」だけ

```bash
cd /c/Users/heart/voice-fortune
```

### コードをGitHubに送る（まだ送っていない／やり直したいとき）

**1行ずつ** 順に実行します。`remote remove` でエラーが出ても **気にせず次へ** 進んでください。

```bash
cd /c/Users/heart/voice-fortune
git remote remove origin
git remote add origin https://github.com/rin0908/voice-fortune.git
git push -u origin main
```

※ `git remote remove origin` が **`No such remote`** と言ったら、**その行だけ失敗**です。**次の行から続けて大丈夫**です。

※ **すでに push まで終わっている**人は、上の **3行（remove / add / push）はもう不要**です。

---

## たくさんの人に配る（無料：GitHub Pages）

### 事前チェック（重要）

- 次の `https://github.com/〇〇/△△.git` の **〇〇 と △△ はダミーです。**
- **必ず自分のGitHubユーザー名と、作ったリポジトリ名に書き換えてから**実行してください。
- すでに間違った `git remote add` をしてしまった場合は、[よくある失敗と直し方](#よくある失敗と直し方)を見てください。

---

### ステップA：GitHubでリポジトリを作る

1. ブラウザで [https://github.com](https://github.com) にログインする。
2. 右上の **＋** → **New repository**。
3. **Repository name** に英語の名前を入れる（例：`voice-fortune`）。日本語は使わない方が無難です。
4. **Public** を選ぶ（無料でPagesしやすい）。
5. **「Add a README」などはチェックしない**（空のリポジトリのまま **Create repository**）。

作成後、画面に表示される **HTTPS のURL** をメモします。  
形は次のとおりです（`あなたのID` と `リポジトリ名` は画面に出ている本物の文字）。

`https://github.com/あなたのID/リポジトリ名.git`

---

### ステップB：手元のPCからコードを送る（push）

ターミナルを開き、**必ずこのアプリのフォルダに移動してから** 次を実行します。

**Git Bash の場合：**

```bash
cd /c/Users/heart/voice-fortune
```

**PowerShell の場合：**

```powershell
cd c:\Users\heart\voice-fortune
```

すでに `git init` と初回コミットが済んでいる場合は、次だけで大丈夫です（`origin` が未設定のとき）。

```bash
git remote add origin https://github.com/ここにGitHubのユーザーID/ここにリポジトリ名.git
git push -u origin main
```

**まだ Git を始めていない場合**（`git status` でエラーになるとき）の一例：

```bash
git init
git add .
git commit -m "声占いアプリ"
git branch -M main
git remote add origin https://github.com/ここにGitHubのユーザーID/ここにリポジトリ名.git
git push -u origin main
```

初回 `git push` のとき、GitHubのユーザー名とパスワードを聞かれたら、**パスワードの代わりに Personal Access Token** を使う必要があります（GitHubの案内に従ってください）。

---

### ステップC：GitHub Pages を有効にする

1. GitHubで、そのリポジトリのページを開く。
2. **Settings**（設定）タブ。
3. 左メニューの **Pages**。
4. **Build and deployment** の **Source** で **GitHub Actions** を選ぶ（「Deploy from a branch」ではなく **GitHub Actions**）。

数分待つと、**Actions** タブに緑のチェックが付きます。

---

### ステップD：公開URLを確認する

ブラウザで次を開きます（`ユーザーID` と `リポジトリ名` は自分のものに置き換え）。

`https://ユーザーID.github.io/リポジトリ名/`

または

`https://ユーザーID.github.io/リポジトリ名/index.html`

---

### QRコード

公開URLを [QRコード生成ツール](https://www.google.com/search?q=QR%E3%82%B3%E3%83%BC%E3%83%89+%E7%84%A1%E6%96%99) に貼り、印刷・スライドに載せると対面配布に便利です。

---

### よくある失敗と直し方

**1. `No such file or directory`（cd で失敗）**

- Git Bash では `cd /c/Users/heart/voice-fortune` のように **スラッシュ** と **`/c/`** を使います。
- フォルダ名のスペル（`voice-fortune` など）が本当のフォルダ名と一致しているか確認します。

**2. `fatal: repository 'https://github.com/ユーザー名/リポジトリ名.git' not found`**

- URLの中に **日本語の「ユーザー名」「リポジトリ名」という文字が残っていないか**確認してください。**英数字の本物のID**に置き換える必要があります。
- リポジトリをGitHub上でまだ作っていない、または名前を間違えている可能性があります。

**3. 一度間違えて `git remote add` してしまった**

```bash
cd /c/Users/heart/voice-fortune
git remote -v
git remote remove origin
git remote add origin https://github.com/正しいID/正しいリポジトリ名.git
git push -u origin main
```

---

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
