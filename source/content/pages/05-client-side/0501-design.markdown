title: Web Design
category: page
slug: web-design
sort-order: 0501
choice1url: ./cascading-style-sheets.html
choice1icon: fa-css3
choice1text: CSSでデザインするには？
choice2url: ./static-content.html
choice2icon: fa-spinner fa-inverse
choice2text: CSSのような静的なファイルをホストするには？
choice3url: ./javascript.html
choice3icon: fa-html5 fa-inverse
choice3text: JavaScriptを使ってインタラクティブなコンテンツを作るには？
choice4url: 
choice4icon: 
choice4text: 


<!-- # Web Design -->
# Webデザイン
<!-- Web design is the creation of a web application's style and user interaction
using CSS and JavaScript. -->
WebデザインはCSSとJavaScriptを使ってWebアプリケーションの見た目やユーザインタラクションを作ることです。


<!-- ## Why is web design important? -->
## なぜWebデザインは重要？
<!-- You don't really expect users to use your 2014 web application if it looks
like this, do you? -->
今時、このようなWebアプリケーションを使いたいと思うユーザがいると思いますか？

<img src="theme/img/no-style-webpage.png" width="100%" alt="HTML with no CSS or JavaScript." class="technical-diagram" /> 

<!-- Creating web pages with their own style and interactivity so users can easily
accomplish their tasks is a major part of building modern web applications. -->
独自のスタイルとユーザが目的を達成することができるインタラクティブ性を考慮することは、モダンなWebアプリケーションを構築する上で最も重要な要素の一つです。


<!-- ## Responsive design -->
## レスポンシブデザイン
<!-- Separating the content from the rules for how to display the content allows 
devices to render the output differently based on factors such as screen size
and device type. Displaying content differently based on varying screen 
attributes is often called *responsive design*. The responsiveness is 
accomplished by implementing
[media queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)
in the [CSS](/cascading-style-sheets.html).  -->
Webアプリケーションを表示しているスクリーンサイズやデバイスに最適なコンテンツの提供の仕方を、コンテンツそのものとは切り離して定義することができます。スクリーンの特徴に応じて異なるコンテンツを表示させることを*レスポンシブデザイン*と呼ぶことがあります。[CSS](./cascading-style-sheets.html)で[CSS media queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)を使うことでレスポンシブなWebアプリケーションを構築することができます。

<!-- For example, a mobile device does not have as much space to display a 
navigation bar on the side of a page so it is often pushed down 
below the main content. The 
[Bootstrap Blog example](http://getbootstrap.com/examples/blog/) 
shows that navigation bar relocation scenario when you resize the browser 
width. -->
例えば、モバイルデバイスにはページ上にナビゲーションバーを表示するための十分なスペースがありません。そこで、メインのコンテンツの下に置くことがあります。[Bootstrap Blog example](http://getbootstrap.com/examples/blog/) を開き、ブラウザの横幅を狭くしてみると、右に位置していたエリアが、ページ下部に移動するのが確認できます。


<!-- ## Design resources -->
## デザインを学ぶためのリソース

<!-- * The [Bootstrapping Design](http://bootstrappingdesign.com/) book is one of 
  the clearest and concise resources for learning design that I've ever read. 
  Highly recommended especially if you feel you have no design skills but 
  need to learn them. -->
* [Bootstrapping Design](http://bootstrappingdesign.com/)は、著者がこれまで読んだデザインを学ぶための書籍として、最も完結でわかりやすいものです。

<!-- * [Kuler](https://kuler.adobe.com/create/color-wheel/) is a complementary
  color picker by Adobe that helps choose colors for your designs. -->
* [Kuler](https://kuler.adobe.com/create/color-wheel/)はAdobe製のカラーピッカーで、色の選択をする際に役立ちます。

<!-- * If you want to learn more about how browsers work behind the scenes, 
  here's a 
  [blog post series on building a browser engine](http://limpet.net/mbrubeck/2014/08/08/toy-layout-engine-1.html)
  that will show you how to build a simple rendering engine. -->
* ブラウザについてもっと知りたければ、[ブラウザエンジンを構築する](http://limpet.net/mbrubeck/2014/08/08/toy-layout-engine-1.html)ブログ記事を読めば、単純なレンダリングエンジンの実装方法を学ぶことができます。
