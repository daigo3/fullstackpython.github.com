title: Deployment
category: page
slug: deployment
sort-order: 0301
choice1url: ./servers.html
choice1icon: fa-sort-amount-asc fa-inverse
choice1text: ベアメタルサーバ、仮想化サーバ、IaaS(Infrastructure as a Service)毎のオプションを知りたい。
choice2url: ./platform-as-a-service.html
choice2icon: fa-puzzle-piece fa-inverse
choice2text: PaaS(Platform as a Service)にPythonアプリケーションをデプロイする方法は？
choice3url: ./operating-systems.html
choice3icon: fa-linux
choice3text: サーバを持っているので、OSをセットアップする方法を知りたい。
choice4url:
choice4icon:
choice4text:


<!-- # Deployment -->
# デプロイメント
<!-- Deployment involves packaging up your web application and putting it in a 
production environment that can run the app. -->
デプロイはWebアプリケーションをパッケージングし、アプリケーションを動かすための本番環境に配置することです。


<!-- ## Why is deployment necessary? -->
## なぜデプロイが必要？
<!-- Your web application must live somewhere other than your own desktop or 
laptop. A production environment is the canonical version of your current 
application and its associated data. -->
Webアプリケーションを作ったのであれば、あなたのデスクトップやラップトップで動かしているだけではいけません。本番環境に置くことで、あなたのアプリケーションは正式なバージョンを持ち、データと交信することになります。

<!-- ## Deployment topics map -->
## デプロイに関するテーマのマップ
<!-- Python web application deployments are comprised of many pieces that need to
be individually configured. Here is a map that visually depicts how each
deployment topic relates to each other. Click the image to pull up a PDF 
version. -->
PythonのWebアプリケーション開発は、それぞれ設定が必要な部品で構成されています。以下の図はデプロイの各テーマの関係を図式化したものです。クリックするとPDF版を見ることができます。

<a href="./full-stack-python-map.pdf" target="_blank" style="border: none;"><img src="theme/img/full-stack-python-map.png" width="100%" alt="Full Stack Python site map." class="technical-diagram" /></a>


<!-- ## Deployment hosting options -->
## デプロイホスティングの選択肢
<!-- There are four options for deploying and hosting a web application: -->
Webアプリケーションをデプロイしホスティングするには4つの選択肢があります。

<!-- 1. ["Bare metal" servers](/servers.html) -->
1. [ベアメタルサーバ](./servers.html)

<!-- 2. [Virtualized servers](/servers.html) -->
2. [仮想化サーバ](./servers.html)

<!-- 3. [Infrastructure-as-a-service](/servers.html) -->
3. [IaaS(Infrastructure as a Service)](./servers.html)

<!-- 4. [Platform-as-a-service](/platform-as-a-service.html) -->
4. [PaaS(Platform as a Service)](./platform-as-a-service.html)

<!-- The first three options are similar. The deployer needs to provision one or
more servers with a Linux distribution. System packages, a web server, 
WSGI server, database and the Python environment are then installed. Finally
the application can be pulled from source and installed in the environment. -->
1~3の選択肢は似たような特徴を持っています。Webアプリケーションを配置するために一つ以上のLinuxディストリビューションサーバを準備します。システムパッケージ、Webサーバ、WSGIサーバ、データベース、Pythonの実行環境をインストールします。最後にアプリケーションのソースを配置し、サーバに配置します。

<!-- Note that there are other ways of installing a Python web application through
system-specific package management systems. We won't cover those in this
guide as they are considered advanced deployment techniques. -->
また、PythonのWebアプリケーションをサーバに配置する方法として、システム特有のパッケージ管理システムを利用する方法もありますが、応用的な方法のため触れません。

<!-- ## Deployment resources -->
## デプロイのリソース

<!-- * [Thoughts on web application deployment](http://omniti.com/seeds/thoughts-on-web-application-deployment)
  walks through stages of deployment with source control, planning, 
  continuous deployment and monitoring the results. -->
* [Thoughts on web application deployment](http://omniti.com/seeds/thoughts-on-web-application-deployment)は、ソース管理、プランニング、継続的開発、モニタリングなど各ステージの外観を学べます。

<!-- * [Practical continuous deployment](http://blogs.atlassian.com/2014/04/practical-continuous-deployment/)
  defines delivery versus deployment and walks through a continuous deployment
  workflow. -->
* [Practical continuous deployment](http://blogs.atlassian.com/2014/04/practical-continuous-deployment/)は、アプリケーションの配信とデプロイを比較し、継続的開発のワークフローについて解説しています。

<!-- * If you're using Flask this 
  [detailed post on deploying it to Ubuntu](https://realpython.com/blog/python/kickstarting-flask-on-ubuntu-setup-and-deployment/)
  is a great way to familiarize yourself with the deployment process. -->
* Flaskを使っているのであれば[Ubuntuへのデプロイ](https://realpython.com/blog/python/kickstarting-flask-on-ubuntu-setup-and-deployment/)が、デプロイのプロセスに関する良いリソースとなります。

<!-- ## Deployment learning checklist -->
## デプロイについて学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- If you're tight on time look at the 
[platform-as-a-service (PaaS)](/platform-as-a-service.html) options. You can
deploy a low traffic project web app for free or low cost. You won't have to
worry about setting up the operating system and web server compared to going
the traditional server route. In theory you should be able to get your 
application live on the web sooner with PaaS hosting. -->
時間が限られた状況ならば[PaaS](./platform-as-a-service.html)の利用を検討してください。アクセスの少ないプロジェクトであれば無料、あるいは安く運用できます。伝統的なサーバーと比べ、OSやWebサーバをセットアップする手間を省くことができます。PaaSでホスティングすることで、素早くアプリケーションをWebで公開することができるでしょう。

<i class="fa fa-check-square-o"></i>
<!-- [Traditional server options](/servers.html) are your best bet for learning
how the entire Python web stack works. You'll often save money with a virtual
private server instead of a platform-as-a-service as you scale up. -->
[伝統的なサーバ](./servers.html)を使うことは、PythonのWebスタックが動作する仕組みを学ぶのに最適な選択肢です。スケールアップしたPaaSを使うよりVPSを使うほうが経済的なケースが多いです。

<i class="fa fa-check-square-o"></i>
<!-- Read about servers, [operating systems](/operating-systems.html), 
[web servers](/web-servers.html) and [WSGI servers](/wsgi-servers.html) to get
a broad picture of what components need to be set up to run a Python web 
application. -->
サーバ、[OS](./operating-systems.html)、[Webサーバ](./web-servers.html)、[WSGIサーバ](./wsgi-servers.html)の章を読み、各コンポーネントがPythonのWebアプリケーションを動作させるために何の役割を持っているかを理解してください。

<!-- ### How would you like to deploy your web app? -->
### どの方法でWebアプリケショーンをデプロイしますか？