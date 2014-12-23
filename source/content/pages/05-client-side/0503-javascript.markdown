title: JavaScript
category: page
slug: javascript
sort-order: 052
choice1url: ./cascading-style-sheets.html
choice1icon: fa-css3 fa-inverse
choice1text: WebアプリケーションのUIを作るには？
choice2url: ./static-content.html
choice2icon: fa-spinner fa-inverse
choice2text: JavaScriptの様な静的なファイルを配信するには？
choice3url: ./source-control.html
choice3icon: fa-code-fork fa-inverse
choice3text: どのようにコードのバージョン管理をすれば良いですか？
choice4url: ./application-programming-intefaces.html
choice4icon: fa-exchange
choice4text: APIとは？


# JavaScript
<!-- JavaScript is a small scripting programming language embedded in web browsers 
to enable dynamic content and interaction.  -->
JavaScriptはWebブラウザに組み込まれたスクリプト言語で、Webページをダイナミックでインタラクティブにすることができます。

<!-- ## Why is JavaScript necessary? -->
## なぜJavaScriptは必要？
<!-- JavaScript executes in the client and enables dynamic content and interaction
that is not possible with HTML and CSS alone. Every modern Python web 
application uses JavaScript on the front end.  -->
JavaScriptはクライアント側で実行され、HTMLとCSSだけでは実現できないダイナミックなWebアプリケーションを作ることができます。モダンなPython Webアプリケーションでは、フロントエンドにJavaScriptを利用しています。

<!-- ## Front end frameworks -->
## フロントエンドフレームワーク
<!-- Front end JavaScript frameworks move the rendering for most of a web 
application to the client side. Often these applications are informally 
referred to as "one page apps" because the webpage is not reloaded upon every
click to a new URL. Instead, partial HTML pages are loaded into the 
document object model or data is retrieved through an API call then displayed
on the existing page. -->
フロンエンドJavaScriptフレームワークでは、Webアプリケショーンのレンダリングの大部分をクライアントサイドで行います。このようなアプリケーションは、URLの遷移のためにページを再読み込みを行わないことから"シングルページアプリケーション"と呼ばれることがあります。DOM内に部分的なHTMLを読み込んだり、データをAPIから取得しページに表示することができます。

<!-- Examples of these front end frameworks include: -->
このような機能を持つフロントエンドのJavaScriptフレームワークには以下の様なものがあります。

* [Angular.js](https://angularjs.org/)

* [Backbone.js](http://backbonejs.org/)

* [Ember.js](http://emberjs.com/)

<!-- Front end frameworks are rapidly evolving. Over the next several years 
consensus about good practices for using the frameworks will emerge. -->
フロントエンドJavaScriptフレームワークの進化はとても速く、数年もすれば、これらのフレームワークを利用するための、一致した最適解も出てくるでしょう。

<!-- ## How did JavaScript originate? -->
## JavaScriptはどのように発展してきたか

<!-- JavaScript is an implementation of 
[the ECMAScript specification](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/JavaScript_Overview) 
which is defined by the 
[Ecma International Standards Body](http://www.ecma-international.org/default.htm). -->
JavaScriptは、[Ecma International Standards Body](http://www.ecma-international.org/default.htm)によって定められた[the ECMAScript specification](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/JavaScript_Overview)の実装です。

<!-- ## JavaScript resources -->
## JavaScriptを学ぶためのリソース
<!-- * [How Browsers Work](http://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
  is a great overview of both JavaScript and CSS as well as how pages are 
  rendered in a browser. -->
* [How Browsers Work](http://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)は、JavaScriptとCSS、そしてブラウザでページがどのようにレンダリングされるかを解説している素晴らしい記事です。

<!-- * [A re-introduction to JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)
  by Mozilla walks through the basic syntax and operators. -->
* Mozillaの[A re-introduction to JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)は、文法と演算子の基本を学ぶことができます。

<!-- * [Coding tools and JavaScript libraries](http://www.smashingmagazine.com/2011/10/28/useful-coding-workflow-tools-for-web-designers-developers/)
  is a huge list by Smashing Magazine with explanations for each tool and 
  library for working with JavaScript. -->
* Smashing Magazineの[Coding tools and JavaScript libraries](http://www.smashingmagazine.com/2011/10/28/useful-coding-workflow-tools-for-web-designers-developers/)は、JavaScriptのツールとライブラリに関する巨大なリソースです。

<!-- * [Superhero.js](http://superherojs.com/) is an incredibly well designed list
  of resources for how to test, organize, understand and generally work with
  JavaScript. -->
* [Superhero.js](http://superherojs.com/)は、テスト、管理、JavaScriptの基礎に関するリソースをまとめたリストです。

<!-- * [Unheap](http://www.unheap.com/) is an amazing collection of reusable JQuery 
  plugins for everything from navigation to displaying media. -->
* [Unheap](http://www.unheap.com/)はナビゲーションからメディアの表示まで、様々なjQueryプラグインが紹介されています。

<!-- * [The State of JavaScript in 2015](http://www.breck-mckye.com/blog/2014/12/the-state-of-javascript-in-2015/)
  is an opinion piece about favoring small, single-purpose JavaScript libraries 
  over larger frameworks due to churn in the ecosystem. -->
* [The State of JavaScript in 2015](http://www.breck-mckye.com/blog/2014/12/the-state-of-javascript-in-2015/)では、JavaScriptの開発サイクルに大きく影響する大規模なフレームワークを使うよりも、単一の目的を達成するための小さなライブラリを使うべきとする意見が述べられています。

<!-- ## JavaScript learning checklist -->
## JavaScriptを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i> 
<!-- Create a simple HTML file with basic elements in it. Use the
``python -m SimpleHTTPServer`` command to serve it up. Create a 
``<script type="text/javascript"></script>`` 
element at the end of the ``<body>`` section in the HTML page. Start playing 
with JavaScript within that element to learn the basic syntax. -->
基本的な要素を含んだ単純なHTMLファイルを作りましょう。``python -m SimpleHTTPServer``コマンドを使って、サーバを起動しHTMLを配信します。HTMLの``<body>``セクションの最後に``<script type="text/javascript"></script>``を記述して、JavaScriptを試してみましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Download [JQuery](http://jquery.com/) and add it to the page above your 
JavaScript element. Start working with JQuery and learning how it makes basic
JavaScript easier. -->
[jQuery](http://jquery.com/)をダウンロードし、使ってみましょう。jQueryを使い始めたら、JavaScriptの基本を簡単に学ぶことができます。

<i class="fa fa-check-square-o"></i> 
<!-- Work with JavaScript on the page. Incorporate examples from open source 
projects listed below as well as JQuery plugins. Check out the Unheap link
below to find a large collection of categorized JQuery plugins. -->
ページ上でJavaScriptを動かしてみましょう。オープンソースのサンプルやjQueryプラグインを試したり、[Unheap](http://www.unheap.com/)で色々なjQueryプラグインを探してみましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Check out the JavaScript resources below to learn more about advanced concepts
and open source libraries. -->
JavaScriptのリソースを読み、応用的なコンセプト、オープンソースのライブラリを学びましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Integrate JavaScript into your web application and check the 
[static content](/static-content.html) section for how to host the JavaScript
files. -->
あなたのWebアプリケーションにJavaScriptを導入しましょう。JavaScriptのファイルを扱う方法は[static content](./static-content.html)の章を参照してください。


<!-- ### Do you need to style your app or deploy it next? -->
### Webアプリケーションのデザイン、またはデプロイを学びますか？