<p data-height="265" data-theme-id="0" data-slug-hash="jAmGBq" data-default-tab="result" data-user="maru0014" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/maru0014/pen/jAmGBq/">R-reviewLoader（preview）</a> by maru (<a href="http://codepen.io/maru0014">@maru0014</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>



# 機能概要

#### 商品レビュー自動表示ツール 楽天市場

既存のテクニックで楽天市場商品ページ内に最新レビューを自動で表示するにはインラインフレームでレビューページ
を読みこませるというものがあります。

しかし、このテクニックではレビューページがそのまま表示されてしまうため見栄えがよくない上に、ユーザーがスクロールしないと上の方にあるレビューしか見ることができませんでした。

　

#### xdomainajaxでレビュー情報を読み込んでくる

今回作ったツールでは商品のレビューページからリアルタイムにhtml情報を取得。
フレーム内にヘッダーや検索バーなどを除いた**必要な情報のみ**を表示します。

　

#### 自動スクロール機能実装

新着レビュー評価5 → 4 へ順に自動スクロールします。
ユーザーがスクロールしなくても多くのレビューをアプローチできます。

　
#### デザインを自由に変更可能

デフォルトでは楽天市場のスタイルシートをほぼそのまま流用していますが、style.cssを書き換えることで
文字サイズ・色・情報の表示/非表示 などカスタマイズが可能です。

　
# 導入方法

#### iframeで読み込むだけ
楽天GOLDサーバーに「r-reviewLoader」のフォルダごとアップロード。
各商品ページ内にインラインフレームとして「index.html」を読み込むだけで自動的に動作します。

　
PC用販売説明文へ

```html
<iframe src="http://www.rakuten.ne.jp/gold/ショップ名/r-reviewLoader/" width="100%" height="600" frameborder="0"></iframe>
```

などと記述すればOK。
