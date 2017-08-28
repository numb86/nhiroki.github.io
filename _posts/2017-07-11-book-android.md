---
layout: post
title: "「Android を支える技術 I ― 60 fps を達成するモダンな GUI システム」読了"
date: 2017-07-11 00:00:00 +09:00
tags: book
---

「[Android を支える技術 I ― 60 fps を達成するモダンな GUI システム](http://gihyo.jp/book/2017/978-4-7741-8759-4)」を読み終わった。

# 感想

- Android のアーキテクチャや実装を、歴史や周辺知識を押さえつつ分かりやすく詳しく解説している素晴らしい本。
- グラフィックスシステムのアーキテクチャを詳しく知らなかったので、入力イベントが描画に至るまでの流れの説明が特に勉強になった。
- 枯れたシステムならまだしも、現在活発に開発されているシステムをここまで徹底的に調べて、かつ最新情報まで追っかけて本に仕上げたのは本当にすごい。自分だったら心折れそう。
- コラムがどれも面白い。著者のモバイル OS への思い入れの強さを感じる。そのあたりの経緯は Morrita さんの記事「[死んでしまった OS たちへ](https://bellflower.dodgson.org/to-ones-that-have-gone-eeb5f81f8a58)」を読むとさらに楽しめる。
- 続刊の「Android を支える技術 II ― 真のマルチタスクに挑んだモバイル OS の心臓部」も読みたい。

# 読書メモ

[Twitter でのメモ書き](https://twitter.com/nhiroki_/status/854652413696917506)

## 第 1 章　Android と GUI システムの基礎知識

GUI システムの全体像、それに関係するシステム群、Android の起動シーケンスなどの解説。

## 第 2 章　タッチとマルチタッチ

Linux のインプットサブシステムから Android のビューシステムへ入力イベントが伝播する流れの解説。Linux 側の説明も丁寧にされててとても勉強になった。図が分かりやすい。

## 第 3 章　UI スレッドと Handler

UI スレッド、メッセージループ実装の Looper、そしてタスクを投入実行する Handler の解説。Looper は fd を監視できて、タッチイベントなどを待つ。タスクのスケジューリング（優先度の扱いとか）をどうしてるのか気になった。

## 第 4 章　View のツリーとレイアウト

View ツリーの構造、リソースフォーマットと Asset Manager、LayoutInflater、measure / layout パスなどの解説。

## 第 5 章　OpenGL ES を用いたグラフィックスシステム

View ツリーから DisplayList を経由して OpenGL ES の API 呼び出しになるまでの解説。スクロールの最適化の話など。

## 第 6 章　OpenGL ES 呼び出しが画面に描かれるまで

SurfaceFlinger の仕組みと Hardware Composer によるグラフィックスバッファの合成の話が興味深かった。

## 第 7 章　バイトコード実行環境 Dalvik と ART

バイトコード実行環境の進化の歴史を丁寧に解説した章。スマートフォンに適した実行環境とはどのようなものか、レジスタ型・スタック型の比較、メモリ節約の工夫と Zygote、JIT/AOT など。