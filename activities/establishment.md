# 日本語 TeX 開発コミュニティに関わる主な動向

日本における TeX の動向と，現在の[日本語 TeX 開発コミュニティ (texjporg)](https://texjp.org/)
に至る経緯をご紹介します。

## 黎明期：TeX の日本語化の試み，ディスク回覧による配布

Donald E. Knuth が TeX の最初のバージョンをリリースしたのが 1978 年，
[The TeX Users Group (TUG)](http://www.tug.org/) が設立されたのが 1980 年です。
TeX の最初の公開版 (TeX78) は DEC-10 上で SAIL 言語を用いて実装されましたが，
その後 Pascal 言語を用いて再実装された TeX82 が公開されます。

TeX の存在は間もなく日本でも知られるようになり，
日本語化の試み（代表的なものが NTT JTeX と ASCII pTeX）が始まります。
並行して，TeX を様々なマシンで実行できるように移植する試みや
周辺ツール（ドライバ）の整備も進み，それらは日本 TeX ユーザ会の会合や
磁気テープの郵送，パソコン通信サービスなどを通じて徐々に普及していきます。

* 1980年代  
  TeX の日本語化の試みが始まる。  
  アスキーが ASCII 日本語 TeX（後の pTeX）を開発。  
  NTT が JTeX を開発。  
* 1986年  
  日本ソフトウェア科学会の下部組織として「日本 TeX ユーザ会」（TeX ユーザ・グループ）が発足。  
  1993年までに，例会（15回），セミナー（2回）を開催。
* 1990年  
  アスキーが『日本語 TeX テクニカルブック I』刊行。  
* 1990年頃？  
  奥村晴彦氏主宰 PC-VAN SIG SCIENCE で大島利雄氏が dviout/dviprt 開発開始。  
* 1990年頃  
  PC-VAN SIG SCIENCE で pTeX を含むフロッピーディスク回覧。  
* 1991年  
  奥村氏『LaTeX 美文書作成入門』刊行。  
* 1994年3月  
  日本ソフトウェア科学会の下部組織（研究会）としての「TeX ユーザ・グループ」が活動を終了。  
* 1994年頃  
  角藤亮氏による TeX 関連アプリケーションの Windows 用バイナリ配布が始まる（現在の [W32TeX](http://w32tex.org/index-ja.html)）。  

## 1990 年代：研究集会やオンライン掲示板での交流

学会の研究会としての「日本 TeX ユーザ会」は 1994 年に解散しますが，
その後も研究集会やオンライン掲示板での緩いユーザ間交流が続きます。

* 1996年11月  
  Donald Knuth 氏，[京都賞受賞](https://www.kyotoprize.org/laureates/donald_ervin_knuth/)のため来日し，慶應大学などで[講演](https://www.jstage.jst.go.jp/article/jssst/14/1/14_1_83/_article/-char/ja)。  
* 1997年  
  Tsukuba Conference で Frank Mittelbach 氏，Yannis Haralambous 氏らが講演。  
* 2000年10月6日  
  東京大学駒場で[研究集会「非欧文言語における TeX」](http://web.archive.org/web/20020612020146/http://ms326.ms.u-tokyo.ac.jp/otobe/noneurotex.html)開催。  
* 2001年  
  奥村氏が [TeX Q & A](https://oku.edu.mie-u.ac.jp/~okumura/texfaq/qa/) 掲示板を開設（2015年まで）。  
* 2002年  
  アスキーがライセンスを Modified BSD license に変更した pTeX 3.0 を公開。  
* 2003年  
  阿瀬はる美氏がハワイ開催の [TUG 2003](https://www.tug.org/tug2003/) に出席。  
  この頃阿瀬氏を通じて TUG より日本のユーザ会設立の打診を受ける。  

## 2000 年代：日本語 TeX ディストリビューション (ptetex, ptexlive) への集約

多くの日本語対応ツールやパッチが有志によって開発されてきた一方で，
それらの配布場所やインストール方法がバラバラであるため，特に UNIX 環境で
「日本語 TeX 環境の構築が煩雑である」という問題が指摘されるようになります。
そこでこれらの手順を単純化すべく，日本語 TeX 環境に必要なパッチ類を取りまとめ，
コンパイル作業を自動化したディストリビューション (ptetex, ptexlive)
の整備が進みます。

同時に，アスキーが pTeX のライセンスを変更したことをきっかけに，
コミュニティによる pTeX の拡張も進みます。代表的なものが，
複数の日本語文字コード（UTF-8 を含む）を扱えるようにする
ptexenc ライブラリ，内部文字コードの Unicode 化（upTeX），
世界的に普及していた TeX の拡張「e-TeX 拡張」のマージ（e-pTeX）です。

* 2004年2月  
  土村展之氏が pTeX と関連するソフトウェアをインストールしやすい [ptetex](http://tutimura.ath.cx/~nob/tex/ptetex.html) にまとめる。  
  2006年頃から，pTeX のソース入力の UTF-8 対応を始める。  
* 2007年3月  
  田中琢爾氏による upTeX が初めて公開される。  
* 2007年8月  
  土村氏が ptetex3 の後継として [ptexlive](http://tutimura.ath.cx/ptexlive/) の開発を開始。  
  これが後に pTeX などを TeX Live に収録するに際してのベースとなる。  
* 2007年10月  
  奥村氏が TeX Q & A の後継として [TeX フォーラム](https://oku.edu.mie-u.ac.jp/tex/)開設。  
* 2008年1月  
  北川弘典氏による e-pTeX が初めて公開される。  
* 2009年  
  pTeX 3.1.11 公開（2020 年時点でのアスキー最新版）。  

## 2010 年代：国際的な TeX ディストリビューション (TeX Live) への収録

日本語 TeX 環境に必要なパッチ類を取りまとめた ptexlive でしたが，
一部のプラットフォームを除き，依然として
ユーザは（自動化されているとはいえ）自分でソースから pTeX などを
コンパイルする必要がありました。
この状況が改善したのが 2010 年の pTeX の TeX Live への収録で，
これによりユーザは簡単にコンパイル済みのプログラムを
入手できるようになりました。

2015 年以降は LaTeX が精力的に開発されており，それに合わせて
(e-)pTeX や pLaTeX も「コミュニティ版」として開発が進められています。

* 2009年  
  奥村氏，黒木裕介氏が中心となり [TeX ユーザの集い 2009](https://oku.edu.mie-u.ac.jp/texconf09/) が東京大学で開催される。  
  これ以降，ほぼ毎年日本のユーザ会が開催され，情報交換の重要な一助となる。  
  2014年からは木枝祐介氏が中心となって開催されており，2017年からは TeXConf という名称となっている。  
* 2010年  
  Norbert Preining 氏の尽力で TeX Live 2010 に pTeX, pLaTeX が初めて収録される。  
  次いで，2011年には e-pTeX が，2012年には (e-)upTeX, upLaTeX も TeX Live に収録される。  
* 2013年  
  黒木氏が中心となり，東京で [TUG 2013](https://www.tug.org/tug2013/jp/) 開催。  
* 2015年  
  山本宗宏氏，黒木氏，富樫秀昭氏が [texjp.org](https://texjp.org/) を構築。  
  [devel ML](https://ml.texjp.org/mailman/listinfo/devel) も開設。  
* 2016年  
  黒木氏が Github に [texjporg](https://github.com/texjporg) 開設。  
  この頃より「コミュニティ版」の用語が使われ始める。  
* 2016年  
  [TeX Wiki](https://texwiki.texjp.org/) を奥村氏のサイトより texjp.org に移設。  
* 2017年  
  鹿野桂一郎氏が TeX ユーザの Slack 部屋 ([TeX users slack](https://texuser.slack.com/)) を開設。  

2010 年代以降の動向は，エンジニア Hub のインタービュー記事「[知ってるようで知らないTeXの世界 自分の人生より歴史あるソフトウェア開発をマネジメントする技術](https://employment.en-japan.com/engineerhub/entry/2019/07/04/103000)」でも紹介されています。
