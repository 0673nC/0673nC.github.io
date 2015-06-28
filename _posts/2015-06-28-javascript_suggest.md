---
layout: post
title: JavaScriptによる入力Formでの補完がしたかった話
tags:
- JavaScript
---

### suggest.jsで遊んでみる

ある入力From(テキストエリア)でこちらが用意した補完候補一覧から入力されたキーにより補完候補を出していく仕組みを作りたかった

emacsでいうところの`auto-complete`みたいな奴

ググってみるといくつかのJavaScriptライブラリが引っかかった

とりあえず最初に目についた`suggest.js`を使って遊んでみた

> [suggest.js](http://www.enjoyxstudy.com/javascript/suggest/index.html){:target="_blank"}

公式ページにあるとおりに設定し試してみるとすぐに動いた

デフォルトだと補完候補一覧が部分一致により出力されるため、やりたかった挙動とちょっと違う

オプション設定により前方一致に変更でき、実装したかった挙動となった

他にもオプションがありhighlightとかするといい感じになる

とりあえずやりたかったことが簡単に出来た

2015年6月現在、このライブラリの最終更新日が約2年前なのでいじらないといけない部分もその内出てくるかもしれない
