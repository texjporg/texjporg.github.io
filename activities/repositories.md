# 日本語 TeX 開発コミュニティのリポジトリ

[日本語 TeX 開発コミュニティ (texjporg)](https://texjp.org/)
は
https://github.com/texjporg
上のリポジトリを使用しています。

この中から主なリポジトリをご紹介していきます（すべてではありません）。

## pTeX

Donald E. Knuth が作った TeX に対して株式会社アスキー（当時）が日本語を使えるようにしたものをベースとし，いくつかの拡張を取り込んでコミュニティで管理している，コミュニティ版 pTeX です。

* [ptex-base](https://github.com/texjporg/ptex-base)
    * pTeX 用の plain TeX マクロ類です。
* [ptex-fonts](https://github.com/texjporg/ptex-fonts)
    * pTeX 用のフォント関連ファイル群 (TFM/JFM, VF) です。
    * 上記の VF を生成するプログラム makejvf のドキュメントも含まれます。
* [platex](https://github.com/texjporg/platex)
    * pTeX 用の LaTeX である pLaTeX と，そのドキュメントです。
* [pbibtex-base](https://github.com/texjporg/pbibtex-base)
    * pTeX 用の BibTeX である pBibTeX 用のスタイルファイルと，そのドキュメントです。
* [ptex-manual](https://github.com/texjporg/ptex-manual)
    * pTeX のマニュアルです。

## upTeX

pTeX の内部を Unicode 化した upTeX です。

* [uptex-base](https://github.com/texjporg/uptex-base)
    * upTeX 用の plain TeX マクロ類と，そのドキュメントおよびサンプルです。
* [uptex-fonts](https://github.com/texjporg/uptex-fonts)
    * upTeX 用のフォント関連ファイル群 (TFM/JFM, VF) です。
* [uplatex](https://github.com/texjporg/uplatex)
    * upTeX 用の LaTeX である upLaTeX とそのドキュメントです。
* [uptex-manual](https://github.com/texjporg/ptex-manual)
    * upTeX のマニュアルです。

## [jsclasses](https://github.com/texjporg/jsclasses)

pLaTeX や upLaTeX 用の新ドキュメントクラスです。
原作者は奥村晴彦氏です。
2016 年以降，コミュニティによって開発が進められています。

## [ptex-fontmaps](https://github.com/texjporg/jfontmaps)

pTeX, upTeX の和文フォント設定を行うためのファイル群です。
かつて jfontmaps という名称でしたが，日本語に加え中国語・韓国語フォント設定も追加した際に改名しました。

## [babel-japanese](https://github.com/texjporg/babel-japanese)

多言語化に使われる Babel パッケージに日本語オプション `japanese` を追加する言語定義ファイルです。
また，海外の LaTeX 開発者に「日本語と西欧言語の組版の違い」を概説する英語ドキュメントも用意しています。

## [cjk-gs-support](https://github.com/texjporg/cjk-gs-support)

CJK（日中韓）フォントを Ghostscript で簡単に使えるようにする設定スクリプトです。

## [ptex2pdf](https://github.com/texjporg/ptex2pdf)

(u)pTeX / (u)pLaTeX と dvipdfmx とを連続して実行し，PDF を生成するスクリプトです。

## [tex-jp-build](https://github.com/texjporg/tex-jp-build)

日本語 TeX 関連の実行ファイルをビルドするための，最小限のソースを上流から取り込んでいるリポジトリです。
pTeX, e-pTeX, makejvf, mendex などのプログラムの開発拠点となっています。
