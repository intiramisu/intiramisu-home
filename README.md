# intiramisu-home

[intiramisu.com](https://intiramisu.com) のランディングページ。

素の HTML だけの静的サイト。ビルド手順はなく、外部へのリクエストも発生しない（CSS はインライン、フォントはシステムスタック）。

```
public/
  index.html    ページ本体
  404.html      存在しないパス用のページ
  favicon.svg   アイコン
```

Cloudflare Pages でホスティングしている。GitHub 連携で `master` への push が自動デプロイされ、配信されるのは `public/` だけ（Pages のビルド出力ディレクトリを `public` に設定）。リポジトリ直下の README などは公開されない。

ローカル確認は `pnpm dlx wrangler pages dev public` で、本番と同じく 404.html の扱いも再現される。

ブログはこちら → [blog.intiramisu.com](https://blog.intiramisu.com)
