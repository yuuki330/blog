# マイブログ（Astro版）

このリポジトリは Astro のブログスターターをベースにしたローカル用ブログです。Markdown / MDX で記事を作成し、
`src/content/blog/` に配置するだけでモダンなブログサイトとして表示できます。今後、note や Qiita、Zenn への
エクスポート用スクリプトを追加する想定で構成しています。

## ディレクトリ構成

```
├── public/                # 静的アセット
├── src/
│   ├── components/        # 再利用可能なコンポーネント
│   ├── content/           # 記事コンテンツ（Markdown / MDX）
│   ├── layouts/           # ページレイアウト
│   └── pages/             # ルーティング定義
├── astro.config.mjs       # Astro の設定
├── package.json           # 依存関係とスクリプト
└── tsconfig.json          # TypeScript 設定
```

## セットアップ

```sh
npm install --install-strategy=hoisted
```

> `sharp` を含むため、環境によってはビルド時に追加のネイティブバイナリがダウンロードされます。

## 主なコマンド

| コマンド | 説明 |
| --- | --- |
| `npm run dev` | 開発サーバーを `http://localhost:4321` で起動します。 |
| `npm run build` | 本番ビルドを `dist/` に出力します。 |
| `npm run preview` | ビルド済みの `dist/` をローカルでプレビューします。 |
| `npm run astro ...` | `astro add` や `astro check` など CLI サブコマンドを実行します。 |

## 記事の追加

1. `src/content/blog/` に Markdown (`.md`) または MDX (`.mdx`) ファイルを追加します。
2. frontmatter にタイトルや公開日、タグなどを設定します。
3. `npm run dev` 中であれば即座に反映されます。

## 今後の拡張アイデア

- note / Qiita / Zenn 向けの Markdown 変換スクリプト
- 記事テンプレートやタグフィルタなどの UI 拡張
- GitHub Actions を用いた自動デプロイ / 同期フロー

Astro 自体の詳細は [公式ドキュメント](https://docs.astro.build/) を参照してください。
