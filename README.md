# アクトの日 2026 福井（特設サイト）

国際ロータリー第2650地区 福井ゾーンのローターアクトクラブが、2026年10月25日（日）に行う「アクトの日」（世界ポリオデー）の案内ページ。

- 公開URL：https://fukui-act.github.io/
- バージョン：1.12.0（更新のたびに上げる。履歴は CHANGELOG.md。ページには表示しない）
- 制作：瀬戸 浩太郎（福井東ローターアクトクラブ 2026-27 会長）
- 公開方法：GitHub Pages（main ブランチのルートをそのまま公開）

## ファイル構成

```
index.html        トップページ（CSSも内包）
story/index.html  サブページ「ありがとう、ロータリー」（ポリオ根絶の物語。CSS・JS・世界地図を内包）。トップからの入口はまだ置いていない（内容の確認中のため保留。sitemap.xml にも入れていない）
assets/
  story/          story/ で使うイラスト（ソコストの素材をトリミングしたSVG）
  favicon.svg     タブのアイコン（クランベリー地に白と水色の子ども2人）
  favicon-32.png  タブのアイコン（SVGが使えないブラウザ用）
  apple-touch-icon.png  iPhoneのホーム画面用（180×180）
  icon-192.png / icon-512.png  Androidのホーム画面用
  ogp.png         SNSで共有したときのサムネ（1200×630）
  logo-rotaract-d2650.png        地区ロゴ（クランベリー。幹事用/地区ロゴ.png を切り抜いたもの）
  logo-rotaract-d2650-white.png  地区ロゴの白版（フッター用）
  drop.svg        雫の形（トップでは1.1.0から未使用。story/ の「2滴」で使う）
  nurie.pdf       塗り絵（内海さんから届いたら置く。まだ無い）
favicon.ico       古いブラウザ用のアイコン
site.webmanifest  ホーム画面に追加したときの名前とアイコン
robots.txt        検索エンジン向けの案内（sitemap.xml の場所）
sitemap.xml       検索エンジン向けのページ一覧
.nojekyll         Jekyllの変換を止める
CHANGELOG.md      更新履歴
```

## 作りの方針

- 読み手は一般市民。書体は BIZ UDPゴシック（Google Fonts）。
- 色はローターアクトの公式色クランベリー（#D41367）が基調。ポリオとワクチンの説明には雫の青（#1466B8）を使う。1クラブのブランド色（福井東RACの緑など）には寄せない。
- 地区ロゴは国際ロータリー第2650地区ローターアクトのもの。色・比率は変えない（白版はフッターの濃い地に置くためだけに使う）。ロゴはすべて地区ローターアクトの公式サイト（https://rac-2650.com/）へのリンク。フッターの「国際ロータリー第2650地区」はロータリー地区の公式サイト（https://www.rid2650.gr.jp/）へのリンク。
- 動き：最初の画面で見出しと日付が出るのと同時に雫が2滴落ちて盾（守られる子ども）が現れる。当日までの日数は100から数え下がって止まり、下線が引かれる（0から始めると「残り0日」に見えるため）。99.9%は画面に入ったときに数え上がる。各段落はスクロールで浮き上がる。OSで「視差効果を減らす」を選んだ人には動きを止めて最初から全部表示する。
- ポリオの説明は、国際ロータリーなどが公表している確立した事実に限る。
- 講師のお名前は、ご本人の了承が取れるまで載せない（「医師の先生」と表記）。
- 1.5.0（2026-09-28）で noindex を外し、検索に出るようにした。robots.txt と sitemap.xml を置いている。1.12.0 で検索対策を追加：トップのタイトルに日にち・場所・「イベント」を入れ、イベントの構造化データ（schema.org Event と WebSite）を埋め込んだ。story/ は内容の確認中のため、検索対策は保留にしている。トップの head にある google-site-verification は Search Console（瀬戸さんのアカウントで登録）の所有権確認用なので消さないこと。開催日時・会場を変えるときは、index.html の構造化データ（application/ld+json）も一緒に直すこと。

## アクセス解析（Googleアナリティクス）

- 測定ID：**G-GGWTF598PY**（瀬戸さんの Google アカウントで作成、2026-09-28）。index.html の `window.GA_ID` に入れている。`G-XXXXXXXXXX` にすると読み込まない。
- QRの行き先：チラシ `https://fukui-act.github.io/?utm_source=flyer&utm_medium=qr`、ポケットティッシュ `https://fukui-act.github.io/?utm_source=tissue&utm_medium=qr`。GA4の「集客」で参照元（flyer／tissue）ごとに数えられる。
- タップの計測は `data-track` の付いたリンク。イベント名は map_open／link_rotaract2650／link_rid2650／link_rc_fukui／link_rc_fukuihigashi／link_rc_fukuisuisen／nurie_download。story/ では story_to_top（トップへ）／story_to_outline（開催のご案内を見る）。

## 塗り絵を公開するとき

1. `assets/nurie.pdf` に置く。
2. `index.html` の「準備中」の `span` を、直前のコメントにある `a` タグに差し替える。
3. バージョンを上げて CHANGELOG に書く。

## 未確定（調整中の札を外すもの）

- お問い合わせ先
- 講演の先生のお名前（了承後）
- 塗り絵のPDF

## 使っている素材

- story/ のイラスト：ソコスト（https://soco-st.com/ 、商用可・点数制限なし・クレジット不要・色変更やアニメーションも可）。27475 小学生と園児（顔）／27491 赤ちゃんと幼児（顔）／20166 病院／27457 子どもの成長／8099 ワクチン／7685 握手する手／24237 松葉杖をつく男の子（1.11.3から未使用）／13274 赤ちゃんを抱っこする女性／17305 地球と手／11383 手をつなぐ色々な人種／20015 会議／1289 住宅街／12611 医者・看護師／世界の子どもたち（25385・25366・25400・25413・25392・25406・25378・25447）。ダウンロードしたカラーSVGをトリミングして assets/story/ に置いている（各ファイルの先頭に出典のコメント）。スポイト・募金箱・500円玉の絵は story/index.html の中で描いたもの。
- story/ の改行位置：BudouX（https://github.com/google/budoux 、Apache 2.0）の日本語モデルで文節の切れ目に<wbr>を入れている（ビルド時に実行。ページには BudouX のコードは入っていない）。

- story/ の背景の世界地図：Natural Earth 1:110m の国境データ（パブリックドメイン）を world-atlas 経由で読み込み、太平洋中心の Equal Earth 図法で描いてSVGにしたもの。「125か国」「予防接種が進む」の場面の塗り分けはイメージ（画面にもそう書いている）。
- story/ の「1979年9月29日、マニラ」の見出し：Noto Serif JP 900（Google Fonts、SIL OFL）。使う文字だけを読み込む。

- 最初の画面とSNSサムネの盾の中の子ども2人、タブやホーム画面のアイコン：Font Awesome Free 7.3.1「children」（https://fontawesome.com 、アイコンは CC BY 4.0）。クレジットは index.html と assets/favicon.svg のコメントに入れている。
