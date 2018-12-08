---
layout: post
title: "第 2 回はじパタ読書会 ― 識別規則と学習法の概要"
date: 2013-07-05 11:24:00 +09:00
tags: event
image: /images/profile.png
---

第 2 回「はじめてのパターン認識」読書会に参加してきました。

**この読書会について**: [http://atnd.org/events/40743](http://atnd.org/events/40743 "http://atnd.org/events/40743")

参加者の多くは研究や仕事でパターン認識を使われているようで、現場での事例などを交えながら分かりやすく説明してくれてとてもためになります。逆に未学習者はしっかりと教科書を予習して、分からないところを洗い出しておくことが大事そうです。(私は超初学者です)

さてさて、今回やった第二章は識別規則と学習法の概要が紹介されていて、様々な用語や手法が登場します。各項目の説明はそれなりに分かったつもりになれたのですが、一読しただけでは全体像が把握できなかったので、改めてざっくりと整理してみました。

("はじめてのパターン認識" の第 1 版を参考にしています。)

## 識別規則の構成法

入力データ x からクラス Ci への写像を **識別規則** という。識別規則は関数 y=f(x) を用いて表現する。実際には写像の性質を決めるパラメータ w を付加した y=f(x; w) となるらしい。

識別規則を構成する方法は主に次の 4 つがある。

- **事後確率による方法**: ベイズの最大事後確率、など
- **距離による方法**: 最近傍法、など
- **関数値による方法**: パーセプトロン型学習回路、サポートベクトルマシン、など
- **決定木による方法**: 決定木

学習の目的は、入力データが正しいクラスに対応する関数値を出すように、パラメータ w を決めること。

## 学習の方法

**教師あり学習**、**教師なし学習**。**半教師あり学習**というものもあるらしい。

## データの分割方法

データを学習用とテスト用に分割する方法 (交差確認法とブートストラップ法を理解しておけば、とりあえず「はじパタ読んだよ」と言える、らしい)。

1. **ホールドアウト法 (holdout 法)**
2. **交差確認法 (cross validation 法)**
3. **一つ抜き法 (leave-one-out 法)**
4. **ブートストラップ法 (bootstrap 法)**

## モデル選択

モデル選択とは誤り率が小さくなるようなパラメータ w を選択する方法のこと ("モデル" という言葉が何を指すのかがいまいちよく分かってない・・・。あと "統計モデル" というものも分かっていない。)。

モデル選択のための代表的な手法としては次の 3 つがある。

- **赤池の情報量基準 (AIC: Akaike Information Criterion)**
- **ベイズ情報量基準 (BIC: Bayesian Information Criterion)**
- **最小距離基準 (MDL: Minimum Distance Length)**

AIC の場合、算出された値が最も小さいモデルを選択すると良いことが多いらしい。他の手法については気が向いたら調べる。

## まとめ

次回も楽しみです！