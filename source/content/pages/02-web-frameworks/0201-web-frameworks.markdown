title: Web Frameworks
category: page
slug: web-frameworks
sort-order: 0201
choice1url: ./django.html
choice1icon: fa-terminal fa-inverse
choice1text: Djangoについてもっと知りたい
choice2url: ./flask.html
choice2icon: fa-flask
choice2text: Flaskについてもっと学びたい
choice3url: ./bottle.html
choice3icon: fa-tint fa-inverse
choice3text: Bottleについてもっと知りたい
choice4url: ./other-web-frameworks.html
choice4icon: fa-question fa-inverse
choice4text: 他のWebフレームワークは？


<!--# Web frameworks-->
# Webフレームワーク
<!--A web application framework is a code library that makes a developer's life
easier when building reliable, scalable and maintainable web applications.-->
Webアプリケーションフレームワークは、開発者が信頼性が高く、スケーラブルでメンテナンス性の高いWebアプリケーションを構築する手助けをしてくれるライブラリです。

<!--## Why are web frameworks necessary?-->
## なぜWebフレームワークが必要？
<!--Web frameworks encapsulate what developers have learned over the past twenty
years while building dynamic web applications. Frameworks make it easier
to reuse code for common HTTP operations and to structure your code so that 
it is maintainable.-->
Webフレームワークには開発者たちが20年間、動的なWebアプリケーションを構築してきたノウハウが詰まっています。一般的なHTTPの操作やメンテナンス性の高いコード構造を簡単に再利用できるように作られています。

<!--## Common web framework functionality-->
## 一般的なWebフレームワークの機能
<!--Frameworks provide functionality in their code or through extensions to 
perform common operations required to run web applications. These common 
operations include:-->
フレームワーク自体が機能を提供している場合もありますし、拡張することによってWebアプリケーションを動作させるのに必要な機能を備えていく物もあります。一般的な機能とは以下の様なものです。

<!--1. URL routing
2. HTML, XML, JSON, and other output format templating
3. Database manipulation
4. Security against Cross-site request forgery (CSRF) and other attacks-->
1. URLのルーティング
2. HTML、XML、JSONなどのフォーマットを出力するテンプレート
3. データベースの操作
4. CSRFなどの脆弱性に対するセキュリティ対策

<!--Not all web frameworks include code for all of the above 
functionality. Frameworks fall somewhere between simply executing a 
single use case and attempting to be everything to every developer with
increased complexity. Some frameworks take the "batteries-included" approach 
where everything possible comes bundled with the framework while others 
have a minimal code library that plays well with extensions.-->
すべてのフレームワークが、上記の機能のすべてを備えてるわけではありません。フレームワークは、単純な用途に的を絞って提供されているものもあれば、複雑な機能を全て備えているものもあります。「電池付属(batteries-included)」のアプローチで、すべての機能を提供しているフレームワークがある一方で、フレームワーク自体はシンプルに保ち、特定の機能は拡張機能として提供されているものもあります。

<!--For example, the Django web application framework includes an 
Object-Relational Mapping (ORM) layer that abstracts relational database 
read, write, query, and delete operations. However, Django's ORM
cannot work without significant modification on non-relational databases such as 
[MongoDB](http://www.mongodb.org/).-->
例えば、DjangoというWebアプリケーションフレームワークには関係データベースのCRUD操作を抽象化するためのORM(Object-Relational Mapping)を提供しています。ただし、DjangoのORMでは[MongoDB](http://www.mongodb.org/)のようなNOSQLデータベースをそのまま使うことはできません。

<!--Some other web frameworks such as Flask and Pyramid are easier to
use with non-relational databases by incorporating external Python libraries.-->
一方、FlaskやPyramidというフレームワークでは外部のPythonライブラリを利用することで、比較的簡単にNOSQLデータベースを利用することができます。

<!--There is a spectrum between minimal functionality with easy extensibility and
including everything in the framework with tight integration.-->
最小限の機能と拡張性を持つフレームワークから、すべての機能が密に結合されたフレームワークが存在します。

<!--## General web framework resources-->
## Webフレームワークに関する一般的な資料
<!--* "[What is a web framework?](http://www.jeffknupp.com/blog/2014/03/03/what-is-a-web-framework/)"-->
<!--by [Jeff Knupp](https://twitter.com/jeffknupp)
  is an in-depth explanation of what a web framework is and their relation
  to web servers.-->
* "[What is a web framework?](http://www.jeffknupp.com/blog/2014/03/03/what-is-a-web-framework/)" - [Jeff Knupp](https://twitter.com/jeffknupp)による記事ではWebフレームワークに関する詳しい説明と、Webサーバとの関係について触れています。

<!--* Check out the answer to the -->
<!--  "[What is a web framework and how does it compare to LAMP?](http://stackoverflow.com/questions/4507506/what-is-a-web-framework-how-does-it-compare-with-lamp)"
  question on Stack Overflow.-->
* Stack Overflowの"[What is a web framework and how does it compare to LAMP?](http://stackoverflow.com/questions/4507506/what-is-a-web-framework-how-does-it-compare-with-lamp)"という質問に対する回答を見てみましょう。

<!--* [Django vs Flask vs Pyramid: Choosing a Python Web Framework](https://www.airpair.com/python/posts/django-flask-pyramid)
  contains background information and code comparisons for similar
  web applications built in these three big Python frameworks.-->
* [Django vs Flask vs Pyramid: Choosing a Python Web Framework](https://www.airpair.com/python/posts/django-flask-pyramid)では、Pythonの3大Webフレームワークについて、その背景の説明やコードの比較が行われています。

<!--* This [Python web framework roundup](http://www.konstruktor.ee/blog/python-web-framework-roundup/)
  covers Django, Flask and Bottle as well as several other lesser known Python
  frameworks.-->
* [Python web framework roundup](http://www.konstruktor.ee/blog/python-web-framework-roundup/)では、Django、Flask、Bottle、その他のWebフレームワークが比較されています。

<!--* This fascinating blog post takes a look at the
  [code complexity of several Python web frameworks](http://grokcode.com/864/snakefooding-python-code-for-complexity-visualization/)
  by providing visualizations based on their code bases.-->
* [code complexity of several Python web frameworks](http://grokcode.com/864/snakefooding-python-code-for-complexity-visualization/)では、それぞれのWebフレームワークのコードベースを視覚化しています。

<!--* [What web frameworks do you use and why are they awesome?](http://www.reddit.com/r/webdev/comments/2les4x/what_frameworks_do_you_use_and_why_are_they/)
  is a language agnostic Reddit discussion on web frameworks. It's interesting
  to see what programmers in other languages like and dislike about their
  suite of web frameworks compared to the main Python frameworks.-->
* [What web frameworks do you use and why are they awesome?](http://www.reddit.com/r/webdev/comments/2les4x/what_frameworks_do_you_use_and_why_are_they/)では、Webフレームワークに関する議論が行われています。興味深いのは他の言語を利用している開発者が参加し、PythonのWebフレームワークと比較して、彼らが利用しているWebフレームワークの利点や欠点を話していることです。


<!--## Web frameworks learning checklist-->
## Webフレームを学ぶためのチェックリスト
<i class="fa fa-check-square-o"></i>
<!--Choose a major Python web framework ([Django](/django.html) or 
[Flask](/flask.html) are recommended) and stick with it. When you're just
starting it's best to learn one framework first instead of bouncing around
trying to understand every framework. -->
有名なPython Webフレームワークを選んで（[Django](/django.html)か[Flask](/flask.html)がお勧めです）、使ってみましょう。これから始めるのであれば、いろいろなフレームワークをいっぺんに理解しようとするよりも、ひとつのフレームワークを学ぶほうが効果的です。

<i class="fa fa-check-square-o"></i>
<!--Work through a detailed tutorial found within the resources links on the
framework's page.-->
フレームワークのページにある資料のリンクからチュートリアルを探して、やってみましょう。

<i class="fa fa-check-square-o"></i>
<!--Study open source examples built with your framework of choice so you can 
take parts of those projects and reuse the code in your application.-->
選択したフレームワークで構築されたオープンソースのアプリケーションを探し、参加したり、自分のアプリケーションで再利用してみましょう。

<i class="fa fa-check-square-o"></i>
<!--Build the first simple iteration of your web application then go to
the [deployment](/deployment.html) section to make it accessible on the 
web.-->
最初にシンプルなアプリケーションを作成し、[deployment](./deployment.html)の章を読み公開してみましょう。

<!--### Which web framework do you want to learn about?-->
### どのWebフレームワークを学びたいですか?
