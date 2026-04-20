# コーヒーhouseヒロ ランディングページ (LP)

岡山県倉敷市の週末限定ロースター「コーヒーhouseヒロ」の公式ランディングページです。
React と Vite を使用して構築された静的シングルページアプリケーション（SPA）です。

## 技術スタック

- **React 19** + **TypeScript**
- **Vite 6**
- **Tailwind CSS v4**
- **Motion** (アニメーション)
- **Lucide React** (アイコン)

## ローカル開発

```bash
npm ci
npm run dev
```

開発サーバーは `http://localhost:3000` で起動します。

## ビルド

```bash
npm run build
```

ビルド成果物は `dist` フォルダに生成されます。

## ホスティング（公開）方法

静的なWebサイトとして動作するため、Vercel、Netlify、Cloudflare Pages などのモダンなホスティングサービスや、一般的なレンタルサーバーで公開できます。

### Vercel / Netlify / Cloudflare Pages

GitHubにプッシュし、ホスティングサービスと連携するのが最も簡単な方法です。

- **フレームワークプリセット**: `Vite`
- **ビルドコマンド**: `npm run build`
- **公開ディレクトリ**: `dist`

### レンタルサーバー（エックスサーバー、さくらのレンタルサーバ等）

1. ローカル環境でビルドします。
   ```bash
   npm install
   npm run build
   ```
2. `dist` フォルダの**中身すべて**を、FTPソフト（FileZillaなど）でサーバーの公開ディレクトリ（`public_html` など）にアップロードしてください。

## コード整形（Biome）

このプロジェクトでは [Biome](https://biomejs.dev/) をコードフォーマッター・リンターとして使用しています。

### インストール

```bash
npm ci
```

`@biomejs/biome` は `devDependencies` に含まれているため、上記コマンドで自動的にインストールされます。

### 整形コマンド

| コマンド | 内容 |
|---|---|
| `npm run format` | コードを自動整形する |
| `npm run check` | 整形 + lint を一括実行して自動修正する |
| `npm run lint` | TypeScript の型チェックのみ実行する |

```bash
# フォーマットのみ
npm run format

# フォーマット + lint + import 自動ソート
npm run check
```

### 主な設定（biome.json）

| 設定項目 | 値 |
|---|---|
| インデント | タブ |
| 行の最大幅 | 100文字 |
| クォート | ダブルクォート |
| セミコロン | あり |
| 末尾カンマ | あり |
| import 自動ソート | 有効 |

## アセット（画像）の変更手順

画像は `public/images/` に格納されています。差し替える場合は同名ファイルを上書きしてください。

| ファイル | 用途 |
|---|---|
| `public/images/logo.jpg` | ロゴ画像 |
| `public/images/favicon.png` | ファビコン |
| `public/images/IMAGE_1.jpeg` 〜 `IMAGE_10.jpeg` | スライドショー画像 |
