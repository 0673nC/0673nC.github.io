---
layout: post
title: emacsの設定でハマった話(shell-mode)
tags:
- emacs
---

### shellの設定

数日前emacs(24.5.1)の設定を見なおしていたらshell用に書いた設定ファイルが上手く読み込めてなかった

emacs上でのshellの設定は**zsh + shell-pop**という風にしていた

原因を調べた結果どうやら`shell-pop`の設定の書き方が古かったっぽい？

そこで公式リポジトリのREADMEのCustomizationの部分を改めて読んで設定しなおした

> [shell-pop](https://github.com/kyagi/shell-pop-el)

設定は反映されそれらしい動きを見せてくれる

またshell-modeのおすすめがデフォルトのshellよりもansi-termだったのでそちらを使ってみる

しかしansi-term上に謎の文字***4m***が…

これを消去するための方法をググる

幾つかの記事と方法が発見できた

どの方法でうまくいくか試したとことこちらの記事の方法のみで上手くいった

> [Emacs 上で快適に Bash や Zsh を利用する設定](http://sakito.jp/emacs/emacsshell.html)
>
>> tic -o ~/.terminfo /Applications/Emacs.app/Contents/Resources/etc/e/eterm-color.ti

MacOS付属のzshを利用する場合、termの情報を指定してあげる必要があるらしい

理由はよくわからなかったがこれで解決できた

#### 余談

ansi-termを使用している最中に気がついた事がある

Tabキーでの補完が効かない(というよりもTabキーそのものが利用できない)

困っていた所Ctrl+iを利用したら補完が効いた

emacs的にはTabとCtrl+iは同じ物だと思っていたが微妙に違うのか？

よくわからないが保管できたので良しとしておく
