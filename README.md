# intiramisu-home

[intiramisu.com](https://intiramisu.com) のランディングページ。

素の HTML だけの静的サイト。ビルド手順はなく、ページ自体は外部リソースを読み込まない（CSS はインライン、フォントはシステムスタック）。

例外として、Cloudflare Web Analytics を有効にしているため、ブラウザからのアクセスには Cloudflare が配信時に計測用スクリプト（`static.cloudflareinsights.com`）を自動で差し込む。Cookie は使わず、EU からの訪問者には差し込まない設定。HTML には含まれないので、リポジトリを見ても出てこない。

```
public/
  index.html    ページ本体
  404.html      存在しないパス用のページ
  favicon.svg   アイコン
```

Cloudflare Pages でホスティングしている。GitHub 連携で `master` への push が自動デプロイされ、配信されるのは `public/` だけ（Pages のビルド出力ディレクトリを `public` に設定）。リポジトリ直下の README などは公開されない。

ローカル確認は `pnpm dlx wrangler pages dev public` で、本番と同じく 404.html の扱いも再現される。

ブログはこちら → [blog.intiramisu.com](https://blog.intiramisu.com)
