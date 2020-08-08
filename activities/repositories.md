# 日本語 TeX 開発コミュニティのリポジトリ

[日本語 TeX 開発コミュニティ (texjporg)](https://texjp.org/)
は
https://github.com/texjporg
上のリポジトリを使用しています。

この中から主なリポジトリをご紹介していきます（すべてではありません）。

## pTeX

Donald E. Knuth が作った TeX に対して株式会社アスキー（当時）が日本語を使えるようにしたものをベースとし，いくつかの拡張を取り込んでコミュニティで管理している，コミュニティ版 pTeX です。

* [ptex-base](https://github.com/texjporg/ptex-base)
    * pTeX 用の plain TeX です。
* [ptex-fonts](https://github.com/texjporg/ptex-fonts)
    * pTeX 用のフォント関連ファイル群 (TFM/JFM, VF) およびそれらを生成する makejvf のドキュメントです。
* [platex](https://github.com/texjporg/platex)
    * pTeX 用の LaTeX である pLaTeX とそのドキュメントです。
* [pbibtex-base](https://github.com/texjporg/pbibtex-base)
    * pTeX 用の BibTeX である pBibTeX 用のスタイルファイルなどです。
* [ptex-manual](https://github.com/texjporg/ptex-manual)
    * pTeX のマニュアルです。

## upTeX

pTeX の内部を Unicode 化した upTeX です。

* [uptex-base](https://github.com/texjporg/uptex-base)
    * upTeX 用の plain TeX とそのドキュメントおよびサンプルです。
* [uptex-fonts](https://github.com/texjporg/uptex-fonts)
    * upTeX 用のフォント関連ファイル群 (TFM/JFM, VF) です。
* [uplatex](https://github.com/texjporg/uplatex)
    * upTeX 用の LaTeX である upLaTeX とそのドキュメントです。
* [uptex-manual](https://github.com/texjporg/ptex-manual)
    * upTeX のマニュアルです。

## [jsclasses](https://github.com/texjporg/jsclasses)

pLaTeX や upLaTeX 用の新ドキュメントクラスです。

## [ptex-fontmaps](https://github.com/texjporg/jfontmaps)

pTeX, upTeX の和文フォント設定を行うためのファイル群です。
（※リポジトリ名は jfontmaps ですがパッケージ名は改名したため ptex-fontmaps です。）

## [cjk-gs-support](https://github.com/texjporg/cjk-gs-support)

CJK （日中韓）フォントを Ghostscript で簡単に使えるようにする設定スクリプトです。

## [tex-jp-build](https://github.com/texjporg/tex-jp-build)

日本語 TeX 関連の実行ファイルをビルドするための，最小限のソースを上流から取り込んでいるリポジトリです。
