# Linux での TeX Live のインストールと設定

ここでは Linux (x86_64) に TeX Live 2019 をインストーラー install-tl を使ってインストールする方法を説明します。FreeBSD, NetBSD などでもほぼ同じですので，参考にしてください。

なお，各 Linux ディストリビューションが用意しているパッケージマネージャから TeX Live をインストールすることもできます。この方法には，install-tl を使う方法と比べると次のような相違点があります：

- 他のアプリケーションと同様に，パッケージマネージャで統一的に管理することができる。
- バイナリは /usr/bin 以下などに配置されるので，自分で PATH を追加する必要がない。
- ファイルの配置場所が install-tl を使う場合と異なるため，他の人が TeX Live について書いた記事を読むときに混乱することがある。
- バージョンが最新のものより古いことがある。
- tlmgr を使って TeX Live の各パッケージを更新したり新規に追加したりすることはできない。

パッケージマネージャからのインストールについては，ディストリビューション毎にやり方やインストール後の細かな仕様が異なり，網羅的な解説が困難なため，この文書では扱わないことにします。

## インストーラーの取得

まず，インストーラーをダウンロードします。TeX Live のインストーラーは ISO イメージとネットインストーラーの2種類が提供されています。

- ISO イメージはリリース時点での各種パッケージも全て含めた DVD のイメージで，そのファイルサイズは3GBを超えます。ただし，BSD や Solaris，および Linux i386 や ARM のバイナリは収録されていないので，これらが必要な場合はネットインストーラーを使います。
- ネットインストーラーはインストーラー本体のみなのでファイルサイズは4MBほどであり，その時点での最新のパッケージを必要に応じてダウンロードしてくれます。公式に推奨されている方法です。

この説明だけを読むとネットインストーラーを使えばよいように思われますが，残念なことにネットインストーラーを使うと環境によっては途中でパッケージのダウンロードに失敗して終了してしまうことがあります。さらに悪いことに，ネットインストールにはそれなりに時間がかかるのに対し，途中終了した場合にはそこから再開することができず，最初からやり直しになってしまいます。ネットワーク環境に問題がない限りは最初から ISO イメージをダウンロードしてしまった方が無難です。

以下ではターミナルからダウンロードとインストーラの実行を行います。ダウンロードは wget があることを前提にしていますが，ない場合は curl や Web ブラウザで代用してももちろんよいです。

プロキシを使う必要がある場合は，次のようにして環境変数を設定しておいてください。

```
$ export http_proxy=http://<host>:<port>
$ export https_proxy=http://<host>:<port>
```

### ISO イメージを使う場合

ISO イメージをダウンロードしてマウントします。適当な作業ディレクトリで次のようにします。

```
$ wget http://mirror.ctan.org/systems/texlive/Images/texlive2019.iso
$ mkdir install-tl-2019
$ su
# mount -o loop texlive2019.iso install-tl-2019
# cd install-tl-2019
```

### ネットインストーラーを使う場合

Tarball をダウンロードして展開します。適当な作業ディレクトリで次のようにします。

```
$ wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
$ tar zxf install-tl-unx.tar.gz
$ cd install-tl-2019*
$ su
```

## インストール

管理者権限のまま，インストーラーを起動します。

```
# ./install-tl
======================> TeX Live installation procedure <=====================

======>   Letters/digits in <angle brackets> indicate   <=======
======>   menu items for actions or customizations      <=======

 Detected platform: GNU/Linux on x86_64

 <B> set binary platforms: 1 out of 5

 <S> set installation scheme: scheme-full

 <C> set installation collections:
     40 collections out of 41, disk space required: 5845 MB

 <D> set directories:
   TEXDIR (the main TeX directory):
     /usr/local/texlive/2019
   TEXMFLOCAL (directory for site-wide local files):
     /usr/local/texlive/texmf-local
   TEXMFSYSVAR (directory for variable and automatically generated data):
     /usr/local/texlive/2019/texmf-var
   TEXMFSYSCONFIG (directory for local config):
     /usr/local/texlive/2019/texmf-config
   TEXMFVAR (personal directory for variable and automatically generated data):
     ~/.texlive2019/texmf-var
   TEXMFCONFIG (personal directory for local config):
     ~/.texlive2019/texmf-config
   TEXMFHOME (directory for user-specific files):
     ~/texmf

 <O> options:
   [ ] use letter size instead of A4 by default
   [X] allow execution of restricted list of programs via \write18
   [X] create all format files
   [X] install macro/font doc tree
   [X] install macro/font source tree
   [ ] create symlinks to standard directories
   [X] after install, set CTAN as source for package updates

 <V> set up for portable installation

Actions:
 <I> start installation to hard disk
 <P> save installation profile to 'texlive.profile' and exit
 <H> help
 <Q> quit

Enter command:
```

このような画面が出ます。書かれている通りにコマンドを入力すると設定を変更したりインストールしたりできます。よくわからなければ，**とにかく I を入力して Enter を押せばインストールが始まります**。

- S を入力して Enter を押すと，scheme を選択できます。初期状態では scheme-full，つまりほぼ全てのパッケージをインストールする設定になっています。
- C を入力して Enter を押すと，scheme よりも細かくどの collection をインストールするかを選択できます。初期状態では Windows 専用のプログラム以外の全てがインストールされます。
- D を入力して Enter を押すと，インストール先などのディレクトリの設定ができます。TeX Live 2018 以前のバージョンが既にインストールされている場合も共存できるようになっています。
- O を入力して Enter を押すと，細かなオプションの設定ができます。

あとはしばらく待てばインストールが終わります。インストールが終わると次のメッセージが出ます。

```
Welcome to TeX Live!


See /usr/local/texlive/2019/index.html for links to documentation.
The TeX Live web site (http://tug.org/texlive/) contains any updates and
corrections. TeX Live is a joint project of the TeX user groups around the
world; please consider supporting it by joining the group best for you. The
list of groups is available on the web at http://tug.org/usergroups.html.


Add /usr/local/texlive/2019/texmf-dist/doc/man to MANPATH.
Add /usr/local/texlive/2019/texmf-dist/doc/info to INFOPATH.
Most importantly, add /usr/local/texlive/2019/bin/x86_64-linux
to your PATH for current and future sessions.

Logfile: /usr/local/texlive/2019/install-tl.log
```

大事なのは最後に書いてある Most importantly, ... の部分です。TeX Live のバイナリは /usr/local/texlive/2019/bin/x86_64-linux 以下にインストールされるので，ここに PATH を通さなければ使うことができません。例えば Bash を使っているならば次のようにするとよいでしょう（管理者権限と普段のユーザーの権限の両方でやること）。

```
$ echo 'PATH=/usr/local/texlive/2019/bin/x86_64-linux:$PATH' >> ~/.bashrc
```

PATH を通したら，ターミナルを再起動して動作確認をします。

```
$ platex -version
e-pTeX 3.14159265-p3.8.2-190131-2.6 (utf8.euc) (TeX Live 2019)
kpathsea version 6.3.1
ptexenc version 1.3.7
Copyright 2019 D.E. Knuth.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the e-pTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the e-pTeX source.
Primary author of e-pTeX: Peter Breitenlohner.
```

このように "TeX Live 2019" が入ったバージョン情報が表示されればうまくできているでしょう。「platex: コマンドが見つかりません」と出る場合は PATH を通すのに失敗しているか，インストールそのものが失敗しています。インストール先のディレクトリを変更した場合は，PATH を通す先もそこにする必要があることに注意してください。

# 旧バージョンのアンインストール

TeX Live 2018 などの旧バージョンがもう不要な場合は，単に削除するだけでアンインストールが完了します。管理者権限で実行するので，**コマンドを打ち間違わないように要注意**。

```
$ su
# rm -rf /usr/local/texlive/2018
```

なんらかの理由で TeX Live 2019 を消したい場合，2017 以前のバージョンを消したい場合も同様で，上の 2018 の部分を該当バージョン番号に変更して rm を実行してください。
