# SOLIDEX Inc. コーポレートサイト(サンプル)

受託システム開発会社「ソリデックス株式会社(SOLIDEX Inc.)」を想定した、コーポレートサイトのトップページ サンプルです。

## 構成

```
.
├── index.html      # ページ本体
├── css/
│   └── style.css   # スタイル一式
├── js/
│   └── main.js     # スクロール演出・ハンバーガーメニューなど
└── README.md
```

外部ライブラリへの依存はありません。Googleフォント(Zen Kaku Gothic New / Noto Sans JP)のみ、`index.html`内でCDN読み込みしています。

## ローカルでの確認方法

`index.html` をブラウザで直接開くだけで表示されます。サーバーは不要です。

```
open index.html        # macOS
start index.html        # Windows
```

## GitHub Pagesで公開する方法

1. このフォルダの中身をリポジトリにpushします。

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
   git push -u origin main
   ```

2. GitHubのリポジトリページで **Settings → Pages** を開きます。
3. 「Build and deployment」の Source を **Deploy from a branch** にし、Branch を `main` / `/(root)` に設定して **Save** します。
4. 数分待つと、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

## 主な機能

- スクロールに合わせて要素がフェードインする演出
- 実績数値のカウントアップアニメーション
- 開発プロセスの縦線が伸びる演出
- 画面上部のスクロール進捗バー
- スマートフォン向けのハンバーガーメニュー

## カスタマイズする際は

- 会社名・住所・実績数値・ニュースなどはすべてダミーです。`index.html`内のテキストを差し替えてください。
- 配色は `css/style.css` 冒頭の `:root{ ... }` にあるCSS変数(`--blue`、`--orange`など)を変更すると、サイト全体に反映されます。
