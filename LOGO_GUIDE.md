# NagisinnraLinux — 導入実績ロゴの追加ガイド

## 追加手順

1. 導入先から、Webサイトへのロゴ掲載許可を得ます。
2. ロゴ画像を `assets/partners/` フォルダへ入れます。
3. `index.html` を開き、`id="deployment-logo-list"` を検索します。
4. その `<div>` の中に、次のHTMLを追加します。

```html
<a class="deployment-logo-link" href="https://example.com/"
   target="_blank" rel="noopener noreferrer">
    <img src="assets/partners/company-name.svg"
         alt="企業・団体名">
</a>
```

5. `company-name.svg` を実際の画像ファイル名に変更します。
6. `https://example.com/` を導入先の公式サイトに変更します。
   公式サイトへのリンクが不要なら `href` と `target` と `rel` を削除しても構いません。
7. `alt` にはロゴの企業・団体名を入力します。
8. 保存してGitHub Pagesへアップロード／pushします。

## 画像について

- 推奨形式：SVG（推奨）、PNG、WebP
- 背景：透過PNGまたはSVGがおすすめ
- 画像は横長・正方形どちらでもOK。表示サイズはCSSで自動調整します。
- ファイル名は `company-name.svg` のように半角英数字とハイフンにします。
- 画像ファイルは `index.html` と同じ階層にある `assets/partners/` 内へ置きます。

## 仕組み

- ロゴを1件ずつHTMLに追加するだけでOKです。
- 追加したロゴは自動で複製され、横方向にシームレスに流れます。
- ロゴ部分にマウスを乗せると一時停止します。
- スマートフォンでも横スクロール表示に対応します。
- ロゴが0件の場合は「導入実績ロゴはまだありません」と表示されます。
- ロゴを増やすとき、JavaScriptやCSSを編集する必要はありません。

## 注意

導入実績として掲載するのは、実際に導入・検証した企業や団体に限ります。
ロゴの掲載許可を得てから追加してください。スポンサーであることと導入実績があることは別なので、必要なら別の枠で表示してください。
