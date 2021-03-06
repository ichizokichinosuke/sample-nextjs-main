# sample-nextjs-main
公開サイトのリンク

https://nextjs-blog-todos-chi-ten.vercel.app/

以下のサンプルコードを含む。
- 40x対応
- 50x対応
- sitemap対応
- RSS対応
- リダイレクト方法
- トレイリングスラッシュ対応

## 開始方法

リポジトリをクローン

```bash
git clone https://github.com/ichizokichinosuke/sample-nextjs-main.git
```

development serverを起動

```bash
npm run dev
# or
yarn dev
```

[http://localhost:3000](http://localhost:3000) をブラウザで開く。

## 40x対応、50x対応
**参考（公式ドキュメント）**

https://nextjs.org/docs/advanced-features/custom-error-page

- next.jsはデフォルトで404エラーページと500エラーページを提供しており、何も設定しなくてもそれらが表示される。
- pages/404.js, pages/500.js をそれぞれ作成することで表示内容をカスタマイズ可能。
- 404エラーページ
    - https://nextjs-blog-todos-chi-ten.vercel.app/no-exist-page
- 500エラーページに関しては未検証


## sitemap対応
```next-sitemap``` を使用

**参考リンク**

リポジトリ

https://github.com/iamvishnusankar/next-sitemap

記事

https://fwywd.com/tech/next-sitemap

サイトマップリンク

https://nextjs-blog-todos-chi-ten.vercel.app/sitemap-0.xml

## RSS対応
```feed``` を使用

**参考リンク**

記事

https://fwywd.com/tech/next-feed-rss-atom

リポジトリ

https://github.com/jpmonette/feed

RSSリンク

https://nextjs-blog-todos-chi-ten.vercel.app/rss/feed.xml

## リダイレクト方法
getServerSidePropsを使用

参考記事
https://zenn.dev/uttk/articles/4649e49f1e6628

**リダイレクト元**

ページ

https://nextjs-blog-todos-chi-ten.vercel.app/redirect-origin-page

コード

https://github.com/ichizokichinosuke/sample-nextjs-main/blob/main/pages/redirect-origin-page.js

**リダイレクト先**

ページ

https://nextjs-blog-todos-chi-ten.vercel.app/redirect-destination-page

コード

https://github.com/ichizokichinosuke/sample-nextjs-main/blob/main/pages/raise-server-error-page.js



## トレイリングスラッシュ対応

公式

https://nextjs.org/docs/api-reference/next.config.js/trailing-slash

デフォルトで "/about/" -> "/about" となる

next.config.jsonで "/about" -> "/about/" となるように設定することも可能
