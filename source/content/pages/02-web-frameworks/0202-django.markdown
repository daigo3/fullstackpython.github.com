title: Django
category: page
slug: django
sort-order: 0202
choice1url: ./cascading-style-sheets.html
choice1icon: fa-css3 fa-inverse
choice1text: ひどいUIを作ってしまった。Webアプリケーションをかっこ良くするには？
choice2url: ./api-integration.html
choice2icon: fa-link fa-inverse
choice2text: Djangoアプリケーションに外部APIを組み込みたい。
choice3url: ./deployment.html
choice3icon: fa-share fa-inverse
choice3text: Djangoアプリケーションをデプロイする方法は？
choice4url: ./source-control.html
choice4icon: fa-code-fork fa-inverse
choice4text: どのようにコードのバージョン管理をすれば良いですか？


# Django
<!--[Django](http://www.djangoproject.com/) is a widely used Python web 
application framework with a "batteries-included" philosophy. The principle
behind batteries-included is that the common functionality for building
web applications should come with the framework instead of as separate
libraries. -->
[Django](http://www.djangoproject.com/) は「電池付属（batteries-included)」というコンセプトでPythonのWebフレームワークとして広く利用されています。「電池付属」というのは、Webアプリケーションを構築するための一般的な機能が、他のライブラリを利用するのではなく、フレームワーク自身によって提供されていることを指します。

<a href="http://www.djangoproject.com/" style="border: none;"><img src="theme/img/django-logo-positive.png" width="100%" alt="Official Django logo. Trademark Django Software Foundation." class="technical-diagram" /></a>


<!--For example, 
[authentication](https://docs.djangoproject.com/en/dev/topics/auth/),
[URL routing](https://docs.djangoproject.com/en/dev/topics/http/urls/), a 
[templating system](https://docs.djangoproject.com/en/dev/topics/templates/),
an [object-relational mapper](https://docs.djangoproject.com/en/dev/topics/db/),
and [database schema migrations](https://docs.djangoproject.com/en/dev/topics/migrations/)
(as of version 1.7) are all included with the [Django framework](https://pypi.python.org/pypi/Django/). -->
[Django framework](https://pypi.python.org/pypi/Django/)では、[認証](https://docs.djangoproject.com/en/dev/topics/auth/)、[URLルーティング](https://docs.djangoproject.com/en/dev/topics/http/urls/)、[テンプレートシステム](https://docs.djangoproject.com/en/dev/topics/templates/)、[ORM](https://docs.djangoproject.com/en/dev/topics/db/)や[データベースマイグレーション](https://docs.djangoproject.com/en/dev/topics/migrations/)(v1.7以降) が提供されています。

<!-- Compare that included functionality to the Flask framework which requires a 
separate library such as 
[Flask-Login](https://flask-login.readthedocs.org/en/latest/)
to perform user authentication. -->
ユーザ認証を実装するために[Flask-Login](https://flask-login.readthedocs.org/en/latest/)のような、分離したライブラリを必要とするFlaskのようなフレームワークと、組み込みの認証機能を比較してみましょう。

<!--The batteries-included and extensibility philosophies are simply two different 
ways to tackle framework building.  Neither philosophy is inherently better 
than the other.-->
電池付属と拡張性という考え方は、単純にフレームワークを作る際のアイデアの違いです。どちらのアイデアが優れているというものではありません。


<!--## Why is Django a good web framework choice?-->
## Djangoを選ぶ利点
<!--The Django project's stability, performance and community have grown 
tremendously over the past decade since the framework's creation. Detailed
tutorials and best practices are readily available on the web and in books.
The framework continues to add significant new functionality such as 
[database migrations](https://docs.djangoproject.com/en/dev/topics/migrations/)
with each release. -->
Djangoプロジェクトは安定していて、性能やコミュニティもフレームワークが作られた当時と比べて飛躍的に向上しています。詳しいチュートリアルやベストプラクティスもWebや書籍で簡単に見つかります。[データベースマイグレーション](https://docs.djangoproject.com/en/dev/topics/migrations/)のような、新しい機能の実装にも積極的です。

<!--I highly recommend the Django framework as a starting place for new Python web 
developers because the official documentation and tutorials are some of the 
best anywhere in software development. Many cities also have Django-specific
groups such as [Django District](http://www.meetup.com/django-district/),
[Django Boston](http://www.meetup.com/djangoboston/) and 
[San Francisco Django](http://www.meetup.com/The-San-Francisco-Django-Meetup-Group/) 
so new developers can get help when they are stuck.-->
著者としては、最初のフレームワークとしてDjangoをお勧めします。公式ドキュメントやチュートリアルが素晴らしく、[Django District](http://www.meetup.com/django-district/)、
[Django Boston](http://www.meetup.com/djangoboston/) や
[San Francisco Django](http://www.meetup.com/The-San-Francisco-Django-Meetup-Group/)など各地域ごとにユーザグループがあり、初心者が問題を解決しやすいでしょう。

<!--There's some debate on whether 
[learning Python by using Django is a bad idea](http://www.jeffknupp.com/blog/2012/12/11/learning-python-via-django-considered-harmful/). 
However, that criticism is invalid if you take the time to learn the Python
syntax and language semantics first before diving into web development.-->
[DjangoでPythonを学ぶな](http://www.jeffknupp.com/blog/2012/12/11/learning-python-via-django-considered-harmful/)という議論もありますが、Web開発に飛び込む前にPythonの基礎を学んでいれば問題ありません。


<!--## Django tutorials -->
## Djangoチュートリアル

<!--* [Tango with Django](http://www.tangowithdjango.com/book/) is an extensive 
  set of free introductions to using the most popular Python web framework. Several
  current developers said this book really helped them get over the initial
  framework learning curve.-->
* [Tango with Django](http://www.tangowithdjango.com/book/)は無料で読めるDjangoの包括的なガイドです。このガイドがDjangoの学び始めには最も役立ったという人もいます。

<!--* [2 Scoops of Django](http://twoscoopspress.com/products/two-scoops-of-django-1-6) 
  by Daniel Greenfeld and Audrey Roy is well worth the price of admission if
  you're serious about learning how to correctly develop Django websites.-->
* Daniel GreenfeldとAudrey Royによる[2 Scoops of Django](http://twoscoopspress.com/products/two-scoops-of-django-1-6)は、DjangoによるWeb開発を正しく学びたいのなら、購入する価値のある書籍です。

<!--* [Effective Django](http://effectivedjango.com/) is another free introduction
  to the web framework.-->
* [Effective Django](http://effectivedjango.com/)は無料のイントロダクションです。

<!--* [Test-Driven Development with Python](http://www.obeythetestinggoat.com/) 
  focuses on web development using Django and JavaScript. This book uses 
  the development of a website using the Django web framework as a real
  world example of how to perform test-driven development (TDD). There is
  also coverage of NoSQL, websockets and asynchronous responses. The book can
  be read online for free or purchased in hard copy via O'Reilly.-->
* [Test-Driven Development with Python](http://www.obeythetestinggoat.com/)はDjangoとJavaScriptを使ったWeb開発にフォーカスしています。Djangoを使って実践的なアプリケーションをテスト駆動開発によって開発する方法を学ぶことができます。また、NoSQL、WebSocket、非同期通信についても触れられています。オンラインであれば無料、書籍版はO'Reillyから出版されています。

<!--* The [Django subreddit](http://www.reddit.com/r/django) often has links to
  the latest resources for learning Django and is also a good spot to ask 
  questions about it.-->
* [Django subreddit](http://www.reddit.com/r/django)では、Djangoを学ぶための最新のリソースが投稿され、質問するにも良い場所でしょう。

<!--* Lincoln Loop wrote a 
  [Django Best Practices guide](http://lincolnloop.com/django-best-practices/)
  for the community.-->
* Lincoln Loopが[Django Best Practices guide](http://lincolnloop.com/django-best-practices/)をコミュニティに執筆しています。

<!--* Steve Losh wrote an incredibly detailed [Django Advice guide](http://stevelosh.com/blog/2011/06/django-advice/).-->
* Steve Loshは細部まで素晴らしい[Django Advice guide](http://stevelosh.com/blog/2011/06/django-advice/)を執筆しています。

<!--* [Lightweight Django](http://programming.oreilly.com/2014/04/simplifying-django.html)
  has several nice examples for breaking Django into smaller simplier 
  components.-->
* [Lightweight Django](http://programming.oreilly.com/2014/04/simplifying-django.html)はDjangoをより小さくシンプルなコンポーネントに分割して利用するための方法を学ぶことができます。

<!--* The [Definitive Guide to Django Deployment](https://github.com/rogueleaderr/definitive_guide_to_django_deployment)
  explains the architecture of the resulting set up and includes Chef scripts
  to automate the deployment.-->
* [Definitive Guide to Django Deployment](https://github.com/rogueleaderr/definitive_guide_to_django_deployment)はChefを利用したデプロイの自動化を含めた、アプリケーションの構成ガイドです。

<!--* [Deploying a Django app on Amazon EC2 instance](http://agiliq.com/blog/2014/08/deploying-a-django-app-on-amazon-ec2-instance/)
  is a detailed walkthrough for deploying an example Django app to Amazon
  Web Services.-->
* [Deploying a Django app on Amazon EC2 instance](http://agiliq.com/blog/2014/08/deploying-a-django-app-on-amazon-ec2-instance/)はDjangoアプリケーションをAmazon Web Servicesにデプロイする詳細なチュートリアルです。

<!--* This [step-by-step guide for Django](http://aliteralmind.wordpress.com/2014/09/21/jquery_django_tutorial/)
  shows how to transmit data via AJAX with JQuery.-->
* [step-by-step guide for Django](http://aliteralmind.wordpress.com/2014/09/21/jquery_django_tutorial/)はjQuetyを使ったAjaxによる通信する方法を解説しています。

<!--* [Deploying Django on AWS](http://www.nickpolet.com/blog/deploying-django-on-aws/1/)
  is another walkthrough for deploying Django to AWS.-->
* [Deploying Django on AWS](http://www.nickpolet.com/blog/deploying-django-on-aws/1/)でもDjangoをAWSにデプロイする方法を解説しています。

<!--* [django-awesome](https://github.com/rosarior/awesome-django) is a curated
  list of Django libraries and resources.-->
* [django-awesome](https://github.com/rosarior/awesome-django)では、Djangoに関係するライブラリや資料のリストが紹介されています。

<!--* [Starting a Django Project](https://realpython.com/learn/start-django/) answers the question, “How do I set up a Django (1.5, 1.6, or /1.7) project from scratch?”-->
* [Starting a Django Project](https://realpython.com/learn/start-django/)ではDjango（v1.5~1.7）によるプロジェクトのセットアップ方法について説明されています。

<!--* The [recommended Django project layout](http://www.revsys.com/blog/2014/nov/21/recommended-django-project-layout/)
  is helpful for developers new to Django to understand how to structure
  the directories and files within apps for projects.-->
* [recommended Django project layout](http://www.revsys.com/blog/2014/nov/21/recommended-django-project-layout/)では、初心者向けにDjangoプロジェクト内のアプリケーションにおけるディレクトリ構成を説明しています。

<!--* The [Django Request-Response Cycle](http://irisbeta.com/article/245366784/the-django-request-response-cycle/)
  explains what happens when you visit a webpage generated by Django.-->
* [Django Request-Response Cycle](http://irisbeta.com/article/245366784/the-django-request-response-cycle/)では、Djangoアプリケーションへアクセスした際に内部で何が起こっているのかを説明しています。

<!--* [Using Amazon S3 to Store your Django Site's Static and Media Files](http://www.caktusgroup.com/blog/2014/11/10/Using-Amazon-S3-to-store-your-Django-sites-static-and-media-files/)
  is a well written guide to a question commonly asked about static and
  media file serving.-->
* [Using Amazon S3 to Store your Django Site's Static and Media Files](http://www.caktusgroup.com/blog/2014/11/10/Using-Amazon-S3-to-store-your-Django-sites-static-and-media-files/)では、静的ファイルやメディアファイルを配信する方法を詳しく解説しています。

<!-- ## Django videos -->
## Djangoのビデオ

<!--* Kate Heddleston and I gave a talk at DjangoCon 2014 called
  [Choose Your Own Django Deployment Adventure](https://www.youtube.com/watch?v=QrFEKghISEI)
  which walked through many of the scenarios you'd face when deploying your
  first Django website.-->
Kate Heddlestonと著者によるDjangoCon 2014での[Choose Your Own Django Deployment Adventure](https://www.youtube.com/watch?v=QrFEKghISEI)では、初めてDjangoアプリケーションをデプロイする際に直面する様々なシナリオについて解説しています。

<!--* [GoDjango](https://godjango.com/) screencasts and tutorials are free short
  videos for learning how to build Django applications.-->
* [GoDjango](https://godjango.com/)スクリーンキャスト及びチュートリアルでは、Djangoアプリケーションを構築するための短いチュートリアルを無料で観ることができます。

<!--* [Getting Started with Django](http://gettingstartedwithdjango.com/) is a
  series of video tutorials for the framework.-->
* [Getting Started with Django](http://gettingstartedwithdjango.com/)はDjangoのビデオチュートリアルシリーズです。

<!--* The videos and slides from 
  [Django: Under the Hood 2014](http://www.djangounderthehood.com/talks/)
  are from Django core commiters and provide insight into the ORM, 
  internationalization, templates and other topics.-->
* Djangoの中心的なコミッターによる[Django: Under the Hood 2014](http://www.djangounderthehood.com/talks/)のビデオ、スライドはORM、国際化、テンプレートなどの話題について触れられています。

<!--* DjangoCon US videos from 
  [2014](https://www.youtube.com/playlist?list=PLE7tQUdRKcybbNiuhLcc3h6WzmZGVBMr3), 
  [2013](http://www.youtube.com/user/TheOpenBastion/videos), 
  [2012](http://pyvideo.org/category/23/djangocon-2012), 
  [2011](http://pyvideo.org/category/3/djangocon-2011), as well as  
  [earlier US and DjangoCon EU conferences](http://pyvideo.org/category) are
  all available free of charge.-->
* DjangoCon USのビデオ、[2014](https://www.youtube.com/playlist?list=PLE7tQUdRKcybbNiuhLcc3h6WzmZGVBMr3)、[2013](http://www.youtube.com/user/TheOpenBastion/videos)、[2012](http://pyvideo.org/category/23/djangocon-2012)、[2011](http://pyvideo.org/category/3/djangocon-2011)、[earlier US and DjangoCon EU conferences](http://pyvideo.org/category)は無料で視聴することができます。

<!-- ## Django 1.7-specific resources -->
## Django 1.7のリソース

<!--* Paul Hallett wrote a 
  [detailed Django 1.7 app upgrade guide](https://www.twilio.com/blog/2014/10/upgrading-your-django-reusable-app-to-support-django-1-7.html) 
  on the Twilio blog from his experience working with the django-twilio 
  package.-->

* TwilioブログでPaul Halleteが投稿した[detailed Django 1.7 app upgrade guide](https://www.twilio.com/blog/2014/10/upgrading-your-django-reusable-app-to-support-django-1-7.html)は、django-twilioパッケージを開発した経験に基づいた記事です。

<!--* [Designing Django's Migrations](http://pyvideo.org/video/2630/designing-djangos-migrations)
  covers Django 1.7's new migrations from the main programmer 
  of South and now Django's built-in migrations, Andrew Godwin.-->
* [Designing Django's Migrations](http://pyvideo.org/video/2630/designing-djangos-migrations)では、South及び、Djangoに組み込まれたマイグレーションツールのメイン開発者であるAndrew GodwinがDjango 1.7の新しいマイグレーションについて解説しています。

<!--* Real Python's [migrations primer](https://realpython.com/blog/python/django-migrations-a-primer/)
  explores the difference between South's migrations and the built-in
  Django 1.7 migrations as well as how you use them.-->
* Real Pythonの[migrations primer](https://realpython.com/blog/python/django-migrations-a-primer/)では、Southによるマイグレーションと、Django 1.7のマイグレーションの違いについて解説しています。

<!--* Andrew Pinkham's "Upgrading to Django 1.7" series is great learning
  material for understanding what's changed in this major release and
  how to adapt your Django project.
  [Part 1](http://andrewsforge.com/article/upgrading-django-to-17/part-1-introduction-and-django-releases/),
  [part 2](http://andrewsforge.com/article/upgrading-django-to-17/part-2-migrations-in-django-16-and-17/) and
  [part 3](http://andrewsforge.com/article/upgrading-django-to-17/part-3-django-17-new-features/)
  and
  [part 4](http://andrewsforge.com/article/upgrading-django-to-17/part-4-upgrade-strategies/)
  are now all available to read.-->
* Andrew Pinkhamによる"Upgrading to Django 1.7"シリーズは、Djangoの新しい機能について、そしてそれを利用する方法を学ぶことができます。[Part 1](http://andrewsforge.com/article/upgrading-django-to-17/part-1-introduction-and-django-releases/)、[part 2](http://andrewsforge.com/article/upgrading-django-to-17/part-2-migrations-in-django-16-and-17/)、[part 3](http://andrewsforge.com/article/upgrading-django-to-17/part-3-django-17-new-features/)、[part 4](http://andrewsforge.com/article/upgrading-django-to-17/part-4-upgrade-strategies/)を読むことができるようになっています。


<!-- ## Django with Angular (Djangular) resources -->
## DjangoとAngularJS(Djangular)のリソース

<!-- * [Getting Started with Django Rest Framework and AngularJS](http://blog.kevinastone.com/getting-started-with-django-rest-framework-and-angularjs.html)
  is a very detailed introduction to Djangular with example code.  -->
* [Getting Started with Django Rest Framework and AngularJS](http://blog.kevinastone.com/getting-started-with-django-rest-framework-and-angularjs.html)は、サンプルコードを交えたDjangularの詳しいイントロダクションです。

<!-- * [Building Web Applications with Django and AngularJS](https://thinkster.io/brewer/angular-django-tutorial/)
  is a very detailed guide for using Django as an API layer and AngularJS
  as the MVC front end in the browser. -->
* [Building Web Applications with Django and AngularJS](https://thinkster.io/brewer/angular-django-tutorial/)は、DjangoをAPIレイヤーとして、AngularJSをクライアントサイドMVCとして利用するための詳細なガイドです。

<!-- * This [end to end web app with Django-Rest-Framework & AngularJS part 1](http://blog.mourafiq.com/post/55034504632/end-to-end-web-app-with-django-rest-framework)
  tutorial along with 
  [part 2](http://blog.mourafiq.com/post/55099429431/end-to-end-web-app-with-django-rest-framework),
  [part 3](http://blog.mourafiq.com/post/58725341511/end-to-end-web-app-with-django-rest-framework)
  and
  [part 4](http://blog.mourafiq.com/post/58726121556/end-to-end-web-app-with-django-rest-framework)
  creates an example blog application with Djangular. There is also a
  corresponding [GitHub repo](https://github.com/mouradmourafiq/django-angular-blog)
  for the project code. -->
* [end to end web app with Django-Rest-Framework & AngularJS part 1](http://blog.mourafiq.com/post/55034504632/end-to-end-web-app-with-django-rest-framework)、及び[part 2](http://blog.mourafiq.com/post/55099429431/end-to-end-web-app-with-django-rest-framework)、[part 3](http://blog.mourafiq.com/post/58725341511/end-to-end-web-app-with-django-rest-framework)、[part 4](http://blog.mourafiq.com/post/58726121556/end-to-end-web-app-with-django-rest-framework)はDjangularでブログアプリケーションを作るチュートリアルです。コードは[GitHub](https://github.com/mouradmourafiq/django-angular-blog)でホストされています。

<!-- ## Django ORM resources -->
## Django ORMのリソース

<!-- The [Django ORM](https://docs.djangoproject.com/en/dev/topics/db/) works well
for simple and medium-complexity database operations. However, there are often
complaints that the ORM makes complex queries much more complicated than
writing straight SQL or using [SQLAlchemy](http://www.sqlalchemy.org/).  -->
[Django ORM](https://docs.djangoproject.com/en/dev/topics/db/)はシンプル〜やや複雑なデータベースの操作に適しています。場合によってORMを使うことで直接SQLを書くよりも複雑になってしまい、[SQLAlchemy](http://www.sqlalchemy.org/)を使う方法もあります。

<!-- It's technically possible to drop down to SQL but it ties the queries to a 
specific database implementation. The ORM is coupled closely with Django so
replacing the default ORM with SQLAlchemy is currently a hack workaround. Note
though that some of the Django core committers believe it is only a matter of
time before the default ORM is replaced with SQLAlchemy. It will be a large
effort to get that working though so it's likely to come in Django 1.9 or 
later. -->
SQLを直接記述することは、技術的に可能ではありますがデータベースの実装によってクエリを書き分けなければなりません。ORMはDjangoと密接につながっているので、デフォルトのORMをSQLAlchemyに置き換えるためにはDjangoをハックしなければなりません。ただDjangoのコアコミッターたちはデフォルトのORMがSQLAlchemyに置き換わるのは時間の問題だと考えています。彼らの素晴らしい仕事によりDjango 1.9、またはそれ以降のバージョンで実現するかもしれません。

<!-- Since the majority of Django projects are tied to the default ORM, it's best to
read up on advanced use cases and tools for doing your best work within the
existing framework. -->
大部分のDjangoプロジェクトではデフォルトのORMが利用されているので、現在のフレームワークでの応用的な利用方法やツールに関する資料を読んでおきましょう。

<!-- * [Django models, encapsulation and data integrity](http://www.dabapps.com/blog/django-models-and-encapsulation/)
  is a detailed article by Tom Christie on encapsulating Django models for
  data integrity. -->
*  [Django models, encapsulation and data integrity](http://www.dabapps.com/blog/django-models-and-encapsulation/)はTom Christieによる、モデルのデータ完全性をカプセル化する方法を詳細に解説しています。

<!-- * [Django Debug Toolbar](http://django-debug-toolbar.readthedocs.org/en/1.2/) 
  is a powerful Django ORM database query inspection tool. Highly recommended
  during development to ensure you're writing reasonable query code. 
  [Django Silk](http://mtford.co.uk/blog/2/) is another inspection tool and
  has capabilities to do more than just SQL inspection. -->
* [Django Debug Toolbar](http://django-debug-toolbar.readthedocs.org/en/1.2/)はDjango ORMのデータベースクエリをデバッグするための強力なツールです。開発中は適切なクエリを書いていることを確認することを強くお勧めします。[Django Silk](http://mtford.co.uk/blog/2/)のようなSQLだけにとどまらないデバッグツールもあります。 

<!-- * [Making a specific Django app faster](http://reinout.vanrees.org/weblog/2014/05/06/making-faster.html)
  is a Django performance blog post with some tips on measuring performance
  and optimizing based on the measured results. -->
* [Making a specific Django app faster](http://reinout.vanrees.org/weblog/2014/05/06/making-faster.html)はパフォーマンスの計測と最適化について解説されているポストです。

<!-- * [Why I Hate the Django ORM](https://speakerdeck.com/alex/why-i-hate-the-django-orm)
  is Alex Gaynor's overview of the bad designs decisions, some of which he
  made, while building the Django ORM. -->
* [Why I Hate the Django ORM](https://speakerdeck.com/alex/why-i-hate-the-django-orm)はAlex GaynorによるDjango ORM開発中の悪い設計について語られています。

<!-- * [Going Beyond Django ORM with Postgres](https://speakerdeck.com/craigkerstiens/going-beyond-django-orm-with-postgres)
  is specific to using PostgreSQL with Django. -->
* [Going Beyond Django ORM with Postgres](https://speakerdeck.com/craigkerstiens/going-beyond-django-orm-with-postgres)ではDjangoとPostgreSQLを利用する方法が解説されています。

<!-- * [Migrating a Django app from MySQL to PostgreSQL](http://www.calazan.com/migrating-django-app-from-mysql-to-postgresql/)
  is a quick look at how to move from MySQL to PostgreSQL. However, my guess
  is that any Django app that's been running for awhile on one relational
  database will require a lot more work to port over to another backend
  even with the power of the ORM. -->
* [Migrating a Django app from MySQL to PostgreSQL](http://www.calazan.com/migrating-django-app-from-mysql-to-postgresql/)ではMySQLからPostgreSQLに移行する方法が解説されています。しかし、著者個人の意見としては、すでに運用中のDjangoアプリケーションのデータベースを他のバックエンドに移行するのはORMのちからを借りても困難だと考えています。

<!-- * [Django Model Descriptors](http://blog.kevinastone.com/django-model-descriptors.html)
  discusses and shows how to incorporate business logic into Django models
  to reduce complexity from the views and make the code easier to reuse across
  separate views. -->
* [Django Model Descriptors](http://blog.kevinastone.com/django-model-descriptors.html)では、ビジネスロジックをモデルに取り込みビューの複雑化を回避する方法、そして各ビュー間で再利用する方法について検討しています。

<!-- ## Open source Django example projects -->
## オープンソースのサンプルプロジェクト

<!-- * [Txt 2 React](https://github.com/makaimc/txt2react) is a full Django web
  app that allows audiences to text in during a presentation with feedback
  or questions. -->
* [Txt 2 React](https://github.com/makaimc/txt2react)は、プレゼンテーション中に視聴者がフィードバックや質問を書き込めるアプリケーションです。

<!-- * [Openduty](https://github.com/ustream/openduty) is a website status checking
  and alert system similar to PagerDuty. -->
* [Openduty](https://github.com/ustream/openduty)はPagerDutyに似たウェブサイトのステータス確認、及び監視システムです。

<!-- * [Courtside](https://github.com/myusuf3/courtside) is a pick up sports web 
  application written and maintained by the author of PyCoder's Weekly. -->
* [Courtside](https://github.com/myusuf3/courtside)はPyCoder's Weeklyの作者によって開発された、スポーツイベントを探すためのアプリケーションです。

<!-- * These two Django Interactive Voice Response (IVR) system web application
  repositorities [part 1](https://github.com/phalt/twilio-django-part-1) and
  [part 2](https://github.com/phalt/twilio-django-part-2) show you how to
  build a really cool Django application. There's also an accompanying 
  [blog post](https://www.twilio.com/blog/2014/07/build-an-ivr-system-with-twilio-and-django.html)
  with detailed explanations of each step. -->
* Djangoで作られた音声による自動応答システムのレポジトリです。[part 1](https://github.com/phalt/twilio-django-part-1)と[part 2](https://github.com/phalt/twilio-django-part-2)に分けられています。[blog post](https://www.twilio.com/blog/2014/07/build-an-ivr-system-with-twilio-and-django.html)で詳細に解説されています。


<!-- ## Django project templates -->
## Djangoプレジェクトのテンプレート

<!-- * [Caktus Group's Django project template](https://github.com/caktus/django-project-template) 
  is Django 1.6+ ready. -->
* [Caktus Group's Django project template](https://github.com/caktus/django-project-template)はDjango1.6以降で利用できるプロジェクトのテンプレートです。

<!-- * [Cookiecutter Django](https://github.com/pydanny/cookiecutter-django) is a 
  project template from Daniel Greenfeld, for use with Audrey Roy's 
  [Cookiecutter](https://github.com/audreyr/cookiecutter). Heroku 
  deployment-ready. -->
* [Cookiecutter Django](https://github.com/pydanny/cookiecutter-django)はDaniel Greenfeldによるプロジェクトのテンプレートで、Audrey Royの[Cookiecutter](https://github.com/audreyr/cookiecutter)で利用されています。Herokuにデプロイすることができます。

<!-- * [Two Scoops Django project template](https://github.com/twoscoops/django-twoscoops-project)
  is also from the PyDanny and Audrey Roy. This one provides a quick scaffold
  described in the Two Scoops of Django book. -->
* [Two Scoops Django project template](https://github.com/twoscoops/django-twoscoops-project)もPyDannyとAudrey Royによる、プロジェクトテンプレートです。Two Scoopsの書籍で説明されている構成を素早く組み上げることができます。

<!-- ## Django learning checklist -->
## Djangoを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i> 
<!-- [Install Django](https://docs.djangoproject.com/en/dev/topics/install/) on
your local development machine. -->
あなたの開発マシンに[Djangoをインストール](https://docs.djangoproject.com/en/dev/topics/install/)しましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Work through the initial 
["polls" tutorial](https://docs.djangoproject.com/en/dev/intro/tutorial01/). -->
["polls"チュートリアル](https://docs.djangoproject.com/en/dev/intro/tutorial01/)をやりましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Build a few more simple applications using the tutorial resources found
in the "Django resources" section. -->
Djangoのリソースにリストされているチュートリアルで学んだ知識を使って、シンプルなアプリケーションをいくつか作ってみましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Start coding your own Django project with help from the 
[official documentation](https://docs.djangoproject.com/en/dev/) and 
resource links below. You'll make plenty of mistakes which is critical
on your path to learning the right way to build applications. -->
[公式ドキュメント](https://docs.djangoproject.com/en/dev/)や以下のリンクを読んで、自分のDjangoプロジェクトを書き始めましょう。アプリケーションを正しく構築する方法を学ぶ上で重要となる、失敗をたくさんすると思います。

<i class="fa fa-check-square-o"></i> 
<!-- Read [2 Scoops of Django](http://www.amazon.com/Two-Scoops-Django-Best-Practices/dp/098146730X/ref=sr_1_2?ie=UTF8&qid=1391562062&sr=8-2&tag=mlinar-20) 
to understand Django best practices and learn better ways of building 
Django web applications. -->
[2 Scoops of Django](http://www.amazon.com/Two-Scoops-Django-Best-Practices/dp/098146730X/ref=sr_1_2?ie=UTF8&qid=1391562062&sr=8-2&tag=mlinar-20) を読んで、Djangoのベストプラクティスと、Djangoでアプリケーションを作るためのより良い方法を理解してください。

<i class="fa fa-check-square-o"></i> 
<!-- Move on to the [deployment section](/deployment.html) to get your Django 
project on the web. -->
[デプロイの章](./deployment.html)に進み、あなたのDjangoプロジェクトを公開しましょう。


<!-- ### What do you need to learn next for your Django app? -->
### Djangoアプリケーションの次に学ぶことは？