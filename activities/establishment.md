# 日本語 TeX 開発コミュニティに関わる主な動向

日本における TeX の動向と，現在の[日本語 TeX 開発コミュニティ (texjporg)](https://texjp.org/)
に至る経緯をご紹介します。
  
* 1980年代  
  TeX の日本語化の試みが始まる。  
  ASCII が ASCII 日本語 TeX（後の pTeX）を開発。  
  NTT が JTeX を開発。  
* 1986年  
  日本ソフトウェア科学会の下部組織として「日本 TeX ユーザ会」が発足。  
  1992年（第14回）頃まで TeX ユーザ・グループ例会を開催。  
* 1990年  
  ASCII が『日本語 TeX テクニカルブック I』刊行。  
* 1990年頃？  
  奥村晴彦氏主宰 PC-VAN SIG SCIENCE で大島利雄氏が dviout/dviprt 開発開始。  
* 1990年頃  
  PC-VAN SIG SCIENCE で pTeX を含むフロッピーディスク回覧。  
* 1991年  
  奥村氏『LaTeX 美文書作成入門』刊行。  
* 1994年頃  
  角藤亮氏による TeX 関連アプリケーションの Windows 用バイナリ配布が始まる（現在の [W32TeX](http://w32tex.org/index-ja.html)）。  
* 1996年11月  
  Donald Knuth 氏，[京都賞受賞](https://www.kyotoprize.org/laureates/donald_ervin_knuth/)のため来日し，慶應大学などで[講演](https://www.jstage.jst.go.jp/article/jssst/14/1/14_1_83/_article/-char/ja)。  
* 1997年  
  Tsukuba Conference で Frank Mittelbach 氏，Yannis Haralambous 氏らが講演。  
* 2000年10月6日  
  東京大学駒場で[研究集会「非欧文言語における TeX」](http://web.archive.org/web/20020612020146/http://ms326.ms.u-tokyo.ac.jp/otobe/noneurotex.html)開催。  
* 2001年  
  奥村氏が [TeX Q & A](https://oku.edu.mie-u.ac.jp/~okumura/texfaq/qa/) 掲示板を開設（2015年まで）。  
* 2002年  
  ASCII がライセンスを Modified BSD license に変更した pTeX 3.0 を公開。  
* 2003年  
  阿瀬氏がハワイ開催の [TUG 2003](https://www.tug.org/tug2003/) に出席。  
  この頃阿瀬氏を通じて TUG より日本のユーザ会設立の打診を受ける。  
* 2004年2月  
  土村展之氏が pTeX と関連するソフトウェアをインストールしやすい [ptetex](http://tutimura.ath.cx/~nob/tex/ptetex.html) にまとめ，更に UTF-8 対応を行う。  
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
  鹿野桂一郎氏が TeX ユーザーの Slack 部屋 ([TeX users slack](https://texuser.slack.com/)) を開設。  

2010 年代以降の動向は，エンジニア Hub のインタービュー記事「[知ってるようで知らないTeXの世界 自分の人生より歴史あるソフトウェア開発をマネジメントする技術](https://employment.en-japan.com/engineerhub/entry/2019/07/04/103000)」でも紹介されています。

## TeX/LaTeX から pTeX/pLaTeX へ

Donald E. Knuth が，自身の著書を出版するために開発した組版システムが TeX です。そして Leslie Lamport が，TeX を用いて簡単に文書作成できるようにするために開発した TeX 用マクロパッケージが LaTeX です。これらは日本語に対応していないため，日本語の組版を行うことはできませんでしたが，今でいうオープンソースであったため日本語に対応した派生版を作る試みがいくつか行われました。そのうちの一つが株式会社アスキー（当時）による pTeX/pLaTeX です。この pTeX/pLaTeX は日本で広く使われるようになり，さまざまな環境へ移植されたり拡張されたりして，さらに派生版が作られるようになりました。

## TeX Live への組み込み

pTeX/pLaTeX は 2010 年から [TeX Live](http://www.tug.org/texlive/) という世界的な TeX ディストリビューション（関連するツールやファイルをまとめたもの）へ組み込まれていきました。TeX Live へ組み込まれることによって，TeX Live をインストールするだけで，あるいは各種 Linux ディストリビューションなどでは TeX Live をベースとしたパッケージをインストールするだけで，日本語が使える TeX 環境を簡単にインストールできるようになりました。

一方で，pTeX/pLaTeX は前記のような歴史的事情により様々な派生版が存在してきたため，統一した管理が行われていませんでした。また，開発者同士のコミュニケーション不足により予期せぬ不具合が発生したこともありました。さらに，TeX Live へ組み込まれたことにより，TeX Live 側の事情でコードが変更されることがあり，日本の事情を知らない人が破壊的な変更をしてしまう可能性もありました。

## そして日本語 TeX 開発コミュニティ設立

そこで，2015 年に黒木裕介と山本宗宏が発起人となって有志を集めたのが「[日本語 TeX 開発コミュニティ](https://texjp.org/)」です。これにより関連ツールや関連パッケージなどを含めた開発者同士のコミュニケーション不足を解消するとともに，コミュニティ版 pTeX/pLaTeX をはじめとした関連ツールなどを「コミュニティ版」として一元的に[リポジトリ](repositories.md)で管理することによって，ツール間の齟齬を防ぐようにしています。また，TeX Live など世界の TeX コミュニティとの窓口的な役割を担うことで，日本の事情を知らない人による破壊的変更を防いだり，協力して対処を行うなどしています。
