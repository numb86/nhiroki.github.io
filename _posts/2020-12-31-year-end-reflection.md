---
layout: post
title:  "2020 年の振り返り"
date: 2020-12-31 00:00:00 +09:00
tags: text
image: /images/2020-year-end-reflection-minecraft-block.webp
---

2020 年の雑多な振り返り兼備忘録です。今年で 34 歳になりました。

![マインクラフト](/images/2020-year-end-reflection-minecraft-block.webp)

<p class="caption">子どもが作ってくれたマイクラのスティーブ。会社の机に置き去りに・・・。</p>

- [2019 年の振り返り](/2019/12/31/year-end-reflection)
- [2018 年の振り返り](/2018/12/31/year-end-reflection)
- [2017 年の振り返り](/2017/12/31/year-end-reflection)

# 目次

- [主な出来事](#主な出来事)
- [ソフトウェアエンジニアとしての活動](#ソフトウェアエンジニアとしての活動)
- [趣味の活動](#趣味の活動)
- [今年買ってよかった物](#今年買ってよかった物)
- [今年のつぶやき](#今年のつぶやき)
- [おわりに](#おわりに)

# 主な出来事

## Q1

- 2020 年初仕事は長期インターンのホスト (メンター) で始まりました。期間は 3 月末までで、ぎりぎりオフィス閉鎖前にインターンを終えることができてホッと一安心。インターン氏の仕事が速過ぎて仕事の供給がめちゃ大変でした。嬉しい悲鳴です！ES Modules for Shared Workers の設計・実装・テストをすべてやってもらい、[Chrome 83 から使える](https://blog.chromium.org/2020/04/chrome-83-beta-cross-site-scripting.html)ようにしてもらいました。詳しくは[ブログ記事](https://elkurin.hatenablog.com/entry/2020/04/21/124758)を書いてくれたのでそっちを読んでください。
- 2 月、細菌性の急性胃腸炎で私を含め家族 4 人中 3 人が倒れる。夕方まで普通に仕事してたのに帰ろうとしたらだんだん調子が悪くなり、帰りの電車で立っていられなくなって途中下車。ホームのベンチに座ってたら手足が痺れて感覚がなくなり、視界もノイズまみれになってきて「これは本気でヤバい」と思いながらも本能で歩いて帰宅。その晩には妻にも類似の症状が出始め、さらに数日前から体調が悪かった次男の容態も悪化し、体調不良者が体調不良者を看病するという地獄でその晩は本当に辛かったです。幸い妻と私はわりと早く回復しましたが、次男の嘔吐が収まらず結局一週間入院しました・・・
- ウェブブラウザ開発者のカンファレンス (BlinkOn) に参加するためにロンドンへ出張する予定が[コロナウイルスの流行により中止](https://twitter.com/nhiroki_/status/1234668858700529667)に。初めてのロンドンのはずだったのでとてもがっかり。これ以降の出張はすべてキャンセルになりました。
- 趣味の時間は線形代数の勉強をしているかコンピュータサイエンスの論文を読んでました。

![スーツケース](/images/2020-year-end-reflection-suitcase.webp)

<p class="caption">コロナ禍で出張や旅行がなく、取っ手も壊れかけていたのでスーツケースを処分。2012 年に社会人デビューした時に買って、それから一緒に色々な国に行った思い出の詰まった品でした。</p>

## Q2

- オフィス閉鎖により完全リモートワークがスタート。幼稚園も閉鎖されて生活スタイルが崩壊しました。妻も在宅で働いており、育児と家事と仕事を成立させながら家族全体の生活リズムを作るのに時間がかかりました。春休み明けは分散登園になったけど保育時間が短く、園バスも休止で送り迎えが必要だったので忙しかったです。とてもつらい時期だった。子どもの面倒を見ながら仕事するのは相当なマルチタスク能力とストレスコントロールが求められるので、万人がリモートワークに適応できるとは思えないですね・・・
- 仕事 (Chromium) の主担当領域が Workers (Web Workers, Service Workers, Worklets) から Loading に変わりました。実際には昨年末ぐらいから徐々に移動していたんですが、Q1 は公私ともに色々あり過ぎてまったく手が回っていなかったので Q2 から本格的に活動し始めました。
- ウェブブラウザの変更がコロナウイルスの影響で停滞している企業活動・社会活動に影響を与えないよう、[Chrome のリリースが停止](https://chromereleases.googleblog.com/2020/03/chrome-and-chrome-os-release-updates.html)されました。それに伴いリファクタリングや実行時フラグを持たない機能開発が禁止され、この時期はコード変更を入れるのが難しかったです。私のチームでは規制解除後にプロジェクトを進められるよう種蒔きのような活動をしていました。具体的にはローディング (ナビゲーション) のための新しいメトリクスを設計・実装したり、適当に選んだウェブページのプロファイリング調査をひたすらしてボトルネックの洗い出しなんかをしていました。あと、新しい HTTP ステータスコード (103 Early Hints) のブラウザ対応に向けて、その[予備調査用のメトリクスの設計・実装](https://source.chromium.org/chromium/chromium/src/+/master:docs/early-hints.md)をしていました。これらを通して Chromium の loading や networking 周りの実装がだいぶ分かるようになって良かったです。
- 趣味の時間では取り組んでいた線形代数の参考書が一通り終わったので、天文宇宙検定の勉強を始めました。あと宅建士の本を読んで、問題集を解いたりしてました。

## Q3

- 子どもが夏休みに突入し、何をやっていたのか記憶にないくらい忙しかったです。事件的なことは特になかった気がします。
- 仕事 (Chromium) では最適化のためのヒント情報をレンダリングエンジン内で使うための基盤設計・実装をしていました。Q2 では調査系のタスクが多くてコーディングしたい欲が消化不良気味だったんですが、このプロジェクトでは純粋な設計・実装タスクに没頭できて良かったです。Q3 後半からは [Prerender API](https://groups.google.com/a/chromium.org/g/blink-dev/c/4oKgdB26p6g/m/4M2fIR_aAwAJ) のプロジェクトに加わりました。あとチーム内 LT イベントの運営をして、自分でも発表しました。
- 趣味の時間では主に地学や天文学に関する本を読んでました。Q3 後半頃から天文宇宙検定への焦りを感じ始めました。

## Q4

- ぎっくり腰になりました。三年半ぶり二回目。時間が経つほど身体が固くなって背筋が伸ばせなくなり、しばらく腰を曲げながら生活してました。リモートワークで良かった。初めて背面に針を打ってもらったんですが、なんか身体がグニョってしてすごかった。
- 七五三のお祝いをやりました。親族の間で使われてきた子ども用の袴を手直ししたり、当日のスケジュールを綿密に立てたりと、結構やることが多くて大変でした。当日は晴天で、袴姿で素敵な写真が撮れて良い思い出になりました。
- 仕事 (Chromium) では今まで関わってきたプロジェクトの仕上げをしつつ、Prerender API の設計や試験実装を本格的に始めました。
- 母校の情報工学科で特別講義をする機会をいただき、『[ウェブの進化とウェブブラウザ開発の最前線](/2020/12/04/web-and-browser)』というタイトルで話をしてきました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">Chromium で新しい Prerender API を試験実装しています。実は現在の link rel=prerender 実装では NoStatePrefetch と呼ばれる少しリッチな先読みをしているだけでページの事前描画はしていないんですが、諸々の課題をクリアして prerender を再実装し instant な page load を目指しています <a href="https://twitter.com/hashtag/nhspec?src=hash&amp;ref_src=twsrc%5Etfw">#nhspec</a> <a href="https://t.co/seSAGgeOHI">https://t.co/seSAGgeOHI</a></p>&mdash; nhiroki (@nhiroki_) <a href="https://twitter.com/nhiroki_/status/1339006997027438597?ref_src=twsrc%5Etfw">December 16, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# ソフトウェアエンジニアとしての活動

## Chromium (Chrome) の開発

仕事では引き続き Chromium プロジェクトに参加してウェブブラウザを作っていました。プロジェクトについては主な出来事のところに書いたとおりです。今年私が入れたパッチは 187 個、レビューしたパッチは 357 個でした。レビュー数は微減といった感じですが、自分で入れたパッチの数はかなり減りました。これはコロナウイルスでパッチを入れられない期間があったこと、一年を通してプロジェクトを何度か変更していること、プロジェクトが主に調査・設計フェーズにあったことに拠ります。来年は今のプロジェクトが本格的に実装フェーズに入ると思うので、コミット数は増えるんじゃないかなーと予想しています。

![Chromium CLs](/images/2020-year-end-reflection-chromium-cls.png)

||コミット数|レビュー数|備考|
|2020|187|358|コロナウイルスによるコードフリーズ、プロジェクト変更|
|2019|259|385||
|2018|181|275|育児休暇 (二ヶ月)|
|2017|240|300||

Chromium のコードが [Space X の宇宙船で使われたり](https://old.reddit.com/r/spacex/comments/gxb7j1/we_are_the_spacex_software_team_ask_us_anything/?limit=500)、GitHub の [Arctic Code Vault プロジェクトによって北極圏に埋められたり](https://github.blog/jp/2020-07-20-github-archive-program-the-journey-of-the-worlds-open-source-code-to-the-arctic/)しました。次はどんなところで使われるのか、考えるだけで楽しいです😁

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">書いたコードが北極に行ったし宇宙にも行ったので、次は別の惑星にでも行ってほしいな。今度火星に行く探査機辺りに Chromium 載ってたりしませんか？？ <a href="https://t.co/llPwa34EeO">pic.twitter.com/llPwa34EeO</a></p>&mdash; nhiroki (@nhiroki_) <a href="https://twitter.com/nhiroki_/status/1284028944195260416?ref_src=twsrc%5Etfw">July 17, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 技術記事の執筆

ウェブの何となく理解している挙動について仕様を読み解いてそれを裏付けていく作業が好きでよくやっているんですが、こういう仕様の細かい知見はすぐに忘れるわりに後々必要になることが多いので、いくつかブログ記事にまとめたり、Twitter に [#nhspec というタグ](https://twitter.com/hashtag/nhspec?f=live)を付けてつぶやいてました。Twitter だと後から見返す時に少し不便なので、来年は細かいトピックでもブログ記事にしていくか、もしくは zenn.dev のような気楽に書き足していけるサービスに書き溜めてみようかなと思ってます。

- [HTTPS state の仕様を追う](/2020/02/13/spec-https-state) (02/13)
- [environment settings object の origin の仕様を追う](/2020/02/16/spec-environment-settings-object-origin) (02/16)
- [Resource Timing と HTTP ステータスコード 1xx](/2020/11/21/resource-timing-informational-response) (11/21)

同様に Chromium の実装やトレンドに関するメモもなるべく記事にして公開したいと思っています。とてもニッチで開発者以外 (もしかしたら開発者であっても) 興味ないような話題が多くて記事にするのをためらっていたんですが、でもやはり自分の知識はパブリックな場所にまとめて残しておくと役に立つことも多いので来年はもっとやっていきたいところ。

- [WFH で Audio Worklets の使用率が増えている話](/2020/05/12/usage-of-audio-worklets) (05/12)
- [Chromium の HttpStreamParser によるヘッダ処理](/2020/11/16/chromium-http-stream-parser) (11/16)

## 特別講義

母校で特別講義をする機会をいただき、理工学部情報工学科の 3, 4 年生向けに『[ウェブの進化とウェブブラウザ開発の最前線](/2020/12/04/web-and-browser)』というタイトルで話をしてきました。

<div class="youtube"><iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQA7761ZtEk8uqs6wQ3sOsXo2B-IGpsvRHHftseFDoPTcE4Jq0TPCuX92GrLeL0D4wkJNhUk0jVxE3V/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe></div>

ウェブの進化の歴史を知ることで現在のトレンドについて理解し、またウェブブラウザというグローバルで大規模なソフトウェアの開発の一端を垣間見ることで、ウェブやウェブブラウザの開発に少しでも興味を持ってくれたら良いなぁという気持ちで話をしてきました。将来一緒に開発してくれる人が現れると良いな。

## 論文読み

コンピュータサイエンスの論文を読むのは楽しくてもっとやりたいんですが、時間の制約があってなかなか読めずにいるのが悩みでした。

> 読みたい論文がいっぱいある一方、各論文をじっくり読み込まないと内容を詳しく理解できないため、一編の論文を読むのにとてつもない時間がかかっていました。また「読んだ論文は記事に残す」という自分ルールによってその負荷はさらに重くなっていました。慣れない英文を読み解いて理解しそれを自分なりに整理して記事にまとめるコストは莫大で、上記の記事を書くのにそれぞれ一週間以上かかっています。またこれら以外にも読みながら記事を書いていたけど途中で力尽きてそのまま放置されている論文がいくつもあります。仮にモチベーションを維持してこの作業に時間を注ぎ込めたとしても、一年は約 52 週間なので単純計算で年間 52 編しか読めません。
>
> ― [コンピュータサイエンス論文を多読する試み](/2020/03/02/how-to-read-more-papers)

そこで論文をもっと気軽に読むフォーマットを作ってみました。

- [コンピュータサイエンス論文を多読する試み](/2020/03/02/how-to-read-more-papers) (03/02)

そしてこのフォーマットを使って実際に FAST 2020 の論文を読んだときのメモがこれです。

- [FAST 2020 全論文アブストラクト](/2020/03/15/papers-fast-2020) (03/15)

しかしその後オフィス閉鎖で集中して論文を読む時間が取りにくくなり、結局 FAST 2020 でしかやれてません。また今回のフォーマットが良かったのかどうかも正直よく分かっていません。「暇ができたら論文を読もう」だと一生暇な時がこなくて読めないので、学会の開催に合わせてあらかじめ予定をいれておくべきかな・・・

## その他

近年の量子コンピュータの盛り上がりを楽しむためにも基本的な事柄についてキャッチアップしておきたくて少し勉強しました。『動かして学ぶ量子コンピュータプログラミング』はウェブブラウザ上で実行できる QCEngine という量子計算シミュレータを使って実際にプログラミングしてみるという本で、これのおかげで理解がだいぶ深まった気がします (まだ読みかけ)

- [驚異の量子コンピュータ ― 宇宙最強マシンへの挑戦](/2020/01/02/book-quantum-computer) (01/02)
- [動かして学ぶ量子コンピュータプログラミング](https://twitter.com/nhiroki_/status/1304430907269369856) (読みかけ)

今年はローディングやネットワーク寄りのことをやっていたので、そっち系の本を読んだり読み途中で放置してたりします。

- [Real World HTTP ― 歴史とコードに学ぶインターネットとウェブ技術 [第 2 版]](/2020/06/30/book-real-world-http-2nd-edition) (06/30)
- [TCP 技術入門 ― 進化を続ける基本プロトコル](https://twitter.com/nhiroki_/status/1237504427793068038) (読みかけ)

ゲームを作った経験が、Java プログラミングの授業でマインスイーパを、コンピュータビジョンの実験で OpenCV とカメラ映像を使ったガンシューティング的なゲームを作ったくらいだったので、もうちょっとちゃんと勉強したいなと思って『グラフィックスプログラミング入門』を途中まで読みました。

- [グラフィックスプログラミング入門](https://twitter.com/nhiroki_/status/1223236408409645056) (読みかけ)

読みかけで放置しているものも来年にはちゃんと消化したいですね・・・

# 趣味の活動

## 英語

一昨年から受講していた英会話のグループディスカッションの授業を 7 月にやめました。理由は、クラスメートが契約満了でやめる一方でコロナ禍によって新たなメンバーの補充が行われる見通しがなくクラスの存続が怪しくなってきたこと、授業の時刻 (20:20 ~ 21:40) が子どもの寝かしつけのタイミングと被っていて家族の負担が大きいこと、私自身も契約満了のタイミングだったこと、などです。授業はとても満足していたのでぜひ続けたかったのですがこればかりはしょうがない。英語は業務でも必須なので、落ち着いたらまたレッスンを取りたいと思っています。

あと IT に関する技術書は定期的に読むのに英語に関する本ってあんまり読んでないなーと思い、気になった本を適当に買って読みました。いっぱい積んであるので来年もコンスタントに読みます。

- [伝わる短い英語 ― 新しい世界基準 Plain English](/2020/07/06/book-plain-english) (07/06)
- [法助動詞の底力](/2020/09/22/book-power-of-modal-auxiliary-verb) (09/22)

## 数学

「[数学をツールとして使えるようにし、応用的な分野を学んでいく足固めをする](/2020/01/14/study-math)」という目的を立て、とりあえずマセマのロードマップを制覇することを目標にした 2020 年でした。Q2 までで線形代数は終わったんですが、その後から地学や天文学の勉強を優先したため、結局他は全然進められませんでした。2021 年も細々と続けていきます。

![ロードマップ](/images/book-linear-algebra-campus-seminar-roadmap.png)

- [大学基礎数学 線形代数 キャンパス・ゼミ](/2020/03/20/book-basic-linear-algebra-campus-seminar) (03/20)
- [線形代数 キャンパス・ゼミ](/2020/04/26/book-linear-algebra-campus-seminar) (04/26)
- [数学好きの人のためのブックガイド](/2020/05/04/book-book-guide-for-math-lovers) (05/04)
- [数学ビギナーズマニュアル [第 2 版]](/2020/05/19/book-math-beginners-manual) (05/17)

## 天文宇宙検定

三度目の正直ということで今年も天文宇宙検定 1 級を受けるために Q2 頃からぼちぼち勉強を始め、11 月に試験を受けました。結果はまだ出ていませんが、自己採点の結果 49/100 だったので残念ながら今回も不合格でしょう。前々回 (39) よりは上がっていますが、前回 (62) よりは大幅に下がっていて、ちょっとどうしたもんかな・・・

![看板](/images/astronomy-space-test-2020-1st-grade-signboard.webp)

詳しくは受験記に書きました。

- [天文宇宙検定 1 級受験記 (3rd try)](/2020/12/29/astronomy-space-test-2020-1st-grade)

関連して宇宙関係に関する本をいくつか読みました。

- [深宇宙ニュートリノの発見 ― 宇宙の巨大なエンジンからの使者](/2020/07/25/book-discovery-of-neutrino-from-deep-space) (07/25)
- [2 つの粒子で世界がわかる ― 量子力学から見た物質と力](/2020/08/02/book-boson-and-fermion) (08/02)
- [見えない絶景 ― 深海底巨大地形](/2020/09/03/book-huge-landforms-in-deep-sea) (09/03)
- [火星ガイドブック](/2020/10/02/book-mars-guidebook) (10/02)
- [宇宙岩石入門 ― 起源・観測・サンプルリターン](/2020/10/24/book-introduction-to-planetary-materials-sciences) (10/24)
- [極・宇宙を解く ― 現代天文学演習](/2020/11/24/book-kyoku-uchu-wo-toku) (11/24)

天文学に関連して地学にも興味が湧き始め、来年少し勉強してみたいという気持ちになっています。

## 読書

リモートワークで通勤がなくなって書籍を持ち運ぶ必要がなくなったこと、紙書籍の方が一覧性が高くて便利なことから、漫画や小説などを除いて電子書籍ではもう買わないことにしました。既に電子書籍で持ってる本も読み直すときに紙書籍で書い直しています。これに合わせて大型の本棚を買い足しました。

今まで「とりあえず積んでおけば後で読むだろう」と思ってセールのときにいっぱい電子書籍を買い込んでいたんですが、デジタルデータだと意識的にアクセスしないと目につかず結局読む前に内容が古くなってしまうものが多かったです。あと在宅勤務で子どもといる時間が増えたので、読書しているようには見えにくい電子書籍よりかは紙書籍を読んでる姿を見せたいなって気持ちもあります。

新しい取り組みとして宅建士に関する本を読みました。実は土地や建物の情報を眺めるのが趣味でよく SUUMO とか見ているんですが、どうせならもう少し専門的なことも知りたいと思って本屋で適当に見繕ってきました。宅建や建築に関する本も何冊か積まれているのでこれも来年もう少し消化したい・・・

- [2020 年版 マンガ宅建士 はじめの一歩](/2020/08/22/book-manga-real-estate-notary-first-step) (08/22)

## アニメ

コロナウィルスが流行る前はジムでランニングしながら観るのが日課だったんですが、Q1 途中からそれがなくなり代わりに自宅でフィットネスバイクをこぎながら観ることが多かったです。

新作で最終回まで観たアニメは次の通り。『呪術廻戦』のクオリティが高くて面白かった。

- 痛いのは嫌なので防御力に極振りしたいと思います。
- 攻殻機動隊 SAC_2045
- デカダンス
- 魔王学院の不適合者
- BURN THE WITCH
- ダンジョンに出会いを求めるのは間違っているだろうか III
- Re:ゼロから始める異世界生活 (Season 2 前半)
- キミと僕の最後の戦場、あるいは世界が始まる聖戦
- 魔法科高校の劣等生 来訪者編
- 呪術廻戦

旧作で観たやつ。『メイドインアビス』の劇場版最新作の配信はいつから始まるの？

- メイドインアビス
- アングリーバード
- 幼女戦記
- 劇場版 幼女戦記
- 劇場版 ダンジョンに出会いを求めるのは間違っているだろうか -オリオンの矢-
- ゴブリンスレイヤー GOBLIN’S CROWN

観直したやつ。『落第騎士の英雄譚』と『最弱無敗の神装機竜』は好きで何度も見直してます。『甘城ブリリアントパーク』も良かった。

- 落第騎士の英雄譚
- 最弱無敗の神装機竜
- 甘城ブリリアントパーク
- BLAME!

## ゲーム

ゲームは主に長男とやることが多かったです。

- **beatmania IIDX**：ライフワークだった IIDX ですが、リモートワークになった 4 月以降全くやっておらず、HEROIC VERSE のプレイ回数はわずか 273 回でした。HEROIC VERSE では DP をメインにプレイしてて、初めて DP の方が DJ POINT が高くなりました。BISTROVER はまだやれてないです。ほぼ在宅なのでゲーセンに行くきっかけがなく・・・

![beatmania IIDX HEROIC VERSE](/images/2020-year-end-reflection-beatmania-iidx.webp)

- **マインクラフト**：昨年に引き続き長男とはマインクラフトをやる時間が長かったです。もうすっかり子どもの方が知識が多いので、子ども主導で何かを進めつつ私は雑用をするみたいなプレイスタイルに。あとついにネザーアップデートが入って大喜びでした。来年の洞窟アップデートも楽しみにしています。
- **ヨッシーのクラフトワールド**：横スクロールアクションゲームをプレイしたことがない長男に試しにやらせてみようと思って買いました。私は小学生の頃にヨッシーアイランドにハマって全ステージ 100 点取るまでやったんですが、そのときのことを思い出して懐かしい気持ちになりました。本作は二人協力プレイができるし、初心者向けにジャンプを補助する「パタパタ」の設定ができるので、子どもと一緒に楽しく遊べました。子どもはヨッシーをパタパタさせてるときに自分の身体にも力が入るみたいで、片足が上がってきたり上半身を反ったりしていて可愛かったです。
- **スーパーマリオメーカー 2**：長男はマイクラのように自分で色々作れるゲームが好きそうということで妻が選んで買ってきました。もっぱら子どもがコースを作って、私がテストプレイをしています。UI が複雑で最初は操作に戸惑っていましたが、慣れてくると私なんかじゃ思いつかないようなギミックを作り込むようになりました。世界中の人が作ったコースで遊べるので、そこからインスピレーションを得ているようです。自分で作ったコースもいくつか公開していて、「公開したばかりなのにもう xx 人もプレイしてくれた！海外の人もいる！！」ってとても喜んでいます。自分の作ったものを他の人が遊んでくれたって経験は素晴らしい成功体験になると思うので、これは良い買い物でした。
- **ポケットモンスター Let's Go! ピカチュウ**：Pokemon GO と同じように直感的にポケモンをゲットでき、協力プレイもできて子どもと一緒に楽しめました。平仮名モードがあるので子どもが一人でストーリーを追えるのも良かった。バトルになると毎回「このポケモンにはピカチュウの雷効く？」って聞いてきて可愛かったです。ヨッシーと同じくポケモンも自分の幼少時代を形作っている思い出深いゲームで、世代を超えて同じシリーズのゲームをやっていることに感慨を覚えました。
- **あつまれどうぶつの森**：発売されてすぐに買い、長男が島リーダーとなって妻と私も同じ島に住み始めました。リアルではコロナ禍で季節感のあるイベントにほとんど参加できない一年でしたが、あつもりのおかげで擬似的に季節イベントを堪能することができました。開発に携わった方々に感謝。結局妻と私も自分用の Switch を買って、それぞれ島を作って遊んでいます。毎晩のようにお互いの島におでかけしていて楽しいです。

![あつまれどうぶつの森](/images/2020-year-end-reflection-animal-crossing.webp)

- **FF7 Remake**：体験版をやったときは「戦闘は面白いしビジュアルも綺麗だけど、リメイクだし時間食いそうだから製品版はやらなくていっかー」なんて思ってたんですが、発売後レビュー記事などを読んでたら「これをやらないのはまずい」と思って始め、そのまま一気にハマりました。クリアするまでは毎晩睡眠時間を削って進めてました。2 週間でクリアしてプレイ時間が 42 時間 49 分だったんですが、一日当たりおよそ 3 時間やってる計算で、仕事や子育てしながらよくやったなぁと我ながら・・・。音楽も素晴らしくてサントラを買って仕事中ずっと聴いてました。特にお気に入りなのが「陥没道路」と「ハイタッチ」で、「真夜中のまちぶせ」からのシーン・音楽の流れが本当に良くて無限に聴いてます。これら楽曲については [AUTOMATON の記事](https://automaton-media.com/articles/now-gaming/20200607-126549/)が良いまとめになってます。あと「落日の街」や「反神羅の火」のエモいシーンを経て至る「ヘリガンナー」もめちゃくちゃ良い😁

![FF7 Remake アルティマニア](/images/2020-year-end-reflection-ff7-remake-ultimania.webp)

<p class="caption">アルティマニアも買った。アルティマニアを買うのはベイグラントストーリー以来。</p>

- **リングフィットアドベンチャー**：抽選販売に応募し続けてやっと買えました。想像していた以上にハードなゲームですね。運動をうまくゲーミフィケーションしていて素晴らしい。フィットネスバイクと併せて運動不足解消に努めています。

![リングフィットアドベンチャー](/images/2020-year-end-reflection-ringfit.webp)

<p class="caption">子どもと一緒にビクトリーポーズをしています。</p>

- **ゼルダ無双 厄災の黙示録**：体験版の頃から楽しみにしていました。今絶賛プレイ中。

# 今年買ってよかった物

2020 年はずっとリモートワークだろうと踏んで、仕事場兼書斎の環境整備に色々買いました。

![書斎](/images/2020-year-end-reflection-workplace.webp)

<p class="caption">MBP に 28 インチ 4K (コーディング用) と 24 インチ Full HD (ブラウジング用) を繋いでトリプルディスプレイ。MBP の画面はチャット用。机はオカムラの Swift スタンディングデスク。</p>

## 椅子

オカムラのコンテッサセコンダを買いました。座面をメッシュにするかクッションにするか悩んだんですが、家で使う分には夏場に汗ばむことを気にする必要はないし、メッシュだと長時間座ると痛くなると聞いてクッションにしました。以前使っていたダイニングテーブルに比べて座り心地が良くなり、リクライニングしながら仕事できるようになって圧倒的に快適になりました。

(実際には椅子の上にさらに p!nto を置いているので座面はあまり関係なかったりする)

![椅子](/images/2020-year-end-reflection-chair.webp)

## フィットネスバイク

コロナ禍でジムに通えなくなったので、家で何か作業をしながら手軽に有酸素運動できる器具が欲しくなり、ALINCO の AF6200 フィットネスバイクを買いました。スタンディングデスクの下に置いたらこぎながら仕事できるようになって最高の環境になりました。

![フィットネスバイク](/images/2020-year-end-reflection-fitness-bike.webp)

## スクリーンバー

机が壁に向かっているため自分の影で手元が暗くなってしまい本を読む時に不便だったので BenQ のスクリーンバーを買いました。メインの 4K ディスプレイの上に置いて使っています。BenQ のスクリーンバーは二種類のモデルがあり、上位機種だと光量調節などが手元で行えるデスクトップダイヤルが付いているんですが、これ以上机の上に物を置きたくなかったのでダイヤルのないモデルを選びました。ダイヤルのないモデルでは本体に付いたボタンで操作することになります。光量調節は自動でできるし一度電源を入れたらしばらく付けっぱなしなので自分にはダイヤルがないモデルで十分でした。

![スクリーンバー](/images/2020-year-end-reflection-screen-bar.webp)

# 今年のつぶやき

自分の根幹を成す価値観は「知らないことを知りたい。自分なりに理解し整理したい」という知的好奇心で、特にこの世界の成り立ちに強い興味があることを改めて認識した一年でした。その好奇心を満たしてくれるのが天文学で、それを記述する言語が数学や物理学であると思っています。私は科学に憧憬するファンの一人にしか過ぎませんが、研究者の方々の肩越しにこの世界の真理の一端を垣間見ることができるかもしれないと淡い期待を持っています。彼ら彼女らが明らかにしてくれたことを自分なりに咀嚼し味わえるだけの知識をこれからも吸収していきたいです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">コンピュータサイエンスのあらゆる分野に精通したいという気持ちがある一方、それよりも数学や物理学といったより根源的な分野に精通したいという気持ちが年々強くなっている。この世界がどのように構成されているのか、非才ながらも死ぬまでにその真理の一端に少しでも近づいてみたい :)</p>&mdash; nhiroki (@nhiroki_) <a href="https://twitter.com/nhiroki_/status/1212748559893721089?ref_src=twsrc%5Etfw">January 2, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

これは子どもに向けた言葉ですが自戒でもあります。基準は他人ではなく常に自分の中に持ち続けるべきです。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">これからの人生色々なことで悔しい思いをするだろうけど、そこで腐らずに少しずつ前に進んで成長していって欲しいな。あとどんなに頑張っても何かで一番を維持し続けるのは不可能なので、他人との比較ではなく過去の自分との相対位置が重要なんだよってことは親としてしっかり伝えていきたい。</p>&mdash; nhiroki (@nhiroki_) <a href="https://twitter.com/nhiroki_/status/1239176186690826241?ref_src=twsrc%5Etfw">March 15, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

今年一番反響のあったツイートはこれでした。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">『あつまれどうぶつの森』の攻略本を買ったら辞書並みの厚さだった。約 1200 ページあって『詳解 LINUX カーネル』(約 1000 ページ) よりも分厚い。実家に置いてあるので比較できないけど『LINUX プログラミングインタフェース』(約 1600 ページ) よりは薄いはず <a href="https://twitter.com/hashtag/nhbk?src=hash&amp;ref_src=twsrc%5Etfw">#nhbk</a> <a href="https://t.co/SizL9S3ozV">pic.twitter.com/SizL9S3ozV</a></p>&mdash; nhiroki (@nhiroki_) <a href="https://twitter.com/nhiroki_/status/1256389937886199809?ref_src=twsrc%5Etfw">May 2, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# おわりに

2020 年は色々やりすぎてどれも中途半端になってしまいましたが、少しずつでも目標に向かって進めていると信じて 2021 年も引き続き頑張っていきたいです。来年は上の子が小学校に入学し、下の子が幼稚園に入園します。社会情勢も先行き不透明で、私個人の生活スタイルもまた大きく変わりそうですが、来年もしなやかにみんなで楽しく元気に過ごせると良いなと思ってます。それでは良いお年を！