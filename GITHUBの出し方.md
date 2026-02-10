# GitHub に出す手順

## 1. GitHub でリポジトリを作る

1. https://github.com にログイン
2. 右上の **+** → **New repository**
3. **Repository name** を入力（例: `timer` や `learning-analog-timer`）
4. **Public** を選択
5. **Create repository** をクリック
6. 表示された画面の「…or push an existing repository from the command line」のコマンドをあとで使います

## 2. ターミナルでこのフォルダを開く

- エクスプローラーで `タイマー` フォルダを開き、アドレス欄に `cmd` と入力して Enter  
  または  
- Cursor / VSCode で **ターミナル** → **新しいターミナル** を開き、このフォルダがカレントになっていることを確認

## 3. Git でコミットして GitHub に送る

ターミナルで次を順に実行してください。

```bash
git init
git add .
git commit -m "学習用アナログ時計タイマーを追加"
git branch -M main
git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
git push -u origin main
```

- **あなたのユーザー名** … GitHub のユーザー名
- **リポジトリ名** … 手順1で作ったリポジトリ名

GitHub でリポジトリを作ったあとに表示される「push an existing repository」のコマンドを使っても同じです。

## 4. GitHub Pages で公開する（任意）

ブラウザでタイマーを公開したい場合:

1. GitHub のリポジトリページで **Settings** → **Pages**
2. **Source** で **Deploy from a branch** を選択
3. **Branch** で `main`、フォルダで **/ (root)** を選んで **Save**
4. 数分後、`https://あなたのユーザー名.github.io/リポジトリ名/timer.html` でアクセスできます

---

**注意**: Git が入っていない場合は https://git-scm.com/ からインストールしてください。
