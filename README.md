# site

GitHub Pages 用の最小サンプルです。

## Files

- `docs/index.html`
  サイト一覧のトップページ
- `docs/assets/`
  CSS、画像、JavaScript などの静的ファイル置き場
- `docs/site-a/`
  個別サイト A
- `docs/site-b/`
  個別サイト B
- `.github/workflows/deploy-pages.yml`
  GitHub Pages への自動デプロイ設定

## Static assets

- 公開したい HTML、画像、CSS、JS は `docs/` 配下に置く
- 画像は `docs/assets/logo.png` のように置いて、HTML から `./assets/logo.png` で参照する
- CSS は `docs/assets/styles.css` のように置いて、`<link rel="stylesheet" href="./assets/styles.css">` で読む
- JavaScript も同じく `docs/assets/app.js` などに置いて、`<script src="./assets/app.js"></script>` で読む

## Multiple sites

- 1 repo で複数サイトを置くときは `docs/site-a/`, `docs/site-b/` のようにサブフォルダを分ける
- URL は `https://<user>.github.io/site/site-a/` のようになる
- 各サイトから共通 assets を読むときは `../assets/...` の相対パスを使う
- 追加するときは既存フォルダをコピーして、`docs/index.html` にリンクを足す

## Publish

1. GitHub に `site` リポジトリを作る
2. この内容を push する
3. `Settings > Pages > Source` を `GitHub Actions` にする

標準の公開 URL は通常 `https://<user>.github.io/site/` です。
