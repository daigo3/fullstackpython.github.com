title: Task Queues
category: page
slug: task-queues
sort-order: 0703
choice1url: ./logging.html
choice1icon: fa-align-left fa-inverse
choice1text: Webアプリケーションとタスクキューのログを監視する方法は？
choice2url: ./web-analytics.html
choice2icon: fa-dashboard
choice2text: アクセス解析をすることで、ユーザの何を学ぶことができますか？
choice3url: ./monitoring.html
choice3icon: fa-bar-chart-o fa-inverse
choice3text: 運用中のWebアプリケーションをモニタリングするツールはありますか？
choice4url:
choice4icon:
choice4text:


<!-- # Task queues -->
# タスクキュー
<!-- Task queues manage background work that must be executed outside the usual
HTTP request-response cycle. -->
タスクキューは通常のHTTPリクエスト/レスポンスのサイクルの外側で実行されるバックグラウンド処理を管理します。

<!-- ## Why are task queues necessary? -->
## なぜタスクキューは必要？
<!-- Tasks are handled asynchronously either because they are not initiated by 
an HTTP request or because they are long-running jobs that would dramatically
reduce the performance of an HTTP response. -->
HTTPリクエストをきっかけに行われない、またはHTTPレスポンスを返す際のパフォーマンスを著しく低下させる恐れのある処理は非同期で扱います。

<!-- For example, a web application could poll the GitHub API every 10 minutes to
collect the names of the top 100 starred repositories. A task queue would
handle invoking code to call the GitHub API, process the results and store them
in a persistent database for later use. -->
例えば、Webアプリケーションは10分毎にGitHub APIからスターが多い順に100個のレポジトリを取得しているとします。タスクキューを使ってGitHub APIの呼び出しを管理し、APIのレスポンスを処理してデータベースに保存しておきます。

<!-- Another example is when a database query would take too long during the HTTP
request-response cycle. The query could be performed in the background on a
fixed interval with the results stored in the database. When an
HTTP request comes in that needs those results a query would simply fetch the
precalculated result instead of re-executing the longer query.
This precalculation scenario is a form of [caching](/caching.html) enabled 
by task queues. -->
他の例として、HTTPリクエスト/レスポンスのサイクルの中でデータベースへのクエリに時間がかかりすぎている場合を挙げましょう。クエリをバックグラウンドで一定時間ごとに実行し、データベースに保存することもできるでしょう。HTTPリクエストが来たら、時間のかかるクエリを発行する代わりに、事前にデータベースに保存した結果を取得するようにします。タスクキューで[キャッシング](./caching.html) のよう形式で事前に処理しておくことができます。

<!-- Other types of jobs for task queues include -->
タスクキューでは以下の様な事もできます。

<!-- * spreading out large numbers of independent database inserts over time 
  instead of inserting everything at once

* aggregating collected data values on a fixed interval, such as every
  15 minutes

* scheduling periodic jobs such as batch processes -->
* データベースへのデータの挿入を一度に全て行わずに、時間をかけて複数の独立したデータベースに行う。

* 15分毎など、一定間隔でデータの集計を行う。

* バッチ処理のような、一定の時間に行う処理をスケジュールする。

<!-- ## Task queue projects -->
## タスクキューのプロジェクト
<!-- The defacto standard Python task queue is Celery. The other task queue 
projects that arise tend to come from the perspective that Celery is overly
complicated for simple use cases. My recommendation is to put the effort into
Celery's reasonable learning curve as it is worth the time it takes to 
understand how to use the project. -->
PythonでのタスクキューのデファクトスタンダードはCeleryです。他のタスクキュープロジェクトは、Celeryが単純な用途に使うには複雑すぎるという観点から開発されている傾向があります。著者はCeleryの使い方を時間をかけて学ぶことをお勧めします。

<!-- * The [Celery](http://www.celeryproject.org/) distributed task queue is the
  most commonly used Python library for handling asynchronous tasks and 
  scheduling. -->
* The [Celery](http://www.celeryproject.org/)は非同期タスクとスケジューリングを扱うための、最も利用されているPythonライブラリです。

<!-- * The [RQ (Redis Queue)](http://python-rq.org/) is a simple Python
  library for queueing jobs and processing them in the background with workers.
  RQ is backed by Redis and is designed to have a low barrier to entry.
  The [intro post](http://nvie.com/posts/introducing-rq/) contains information
  on design decisions and how to use RQ. -->
* The [RQ (Redis Queue)](http://python-rq.org/)はジョブをキューイングしたり、バックグラウンドで処理を行うためのシンプルなPythonライブラリです。Redisがベースになっていて、入門の敷居も低くなっています。[イントロダクション](http://nvie.com/posts/introducing-rq/)はRQの使い方と設計に関する説明がされています。

<!-- * [Taskmaster](https://github.com/dcramer/taskmaster) is a lightweight simple
  distributed queue for handling large volumes of one-off tasks.  -->
* [Taskmaster](https://github.com/dcramer/taskmaster)は一度だけ行われる巨大なタスクを管理するための軽量でシンプルなタスクキューライブラリです。

<!-- ## Hosted message and task queue services -->
## メッセージキューとタスクキューのホスティングサービス
<!-- Task queue third party services aim to solve the complexity issues that arise
when scaling out a large deployment of distributed task queues. -->
サードパーティのタスクキューサービスは、タスクキューのデプロイを大規模にスケールアウトする際に生じる複雑な問題を回避します。

<!-- * [Iron.io](http://www.iron.io/) is a distributed messaging service platform 
  that works with many types of task queues such as Celery. It also is built
  to work with other IaaS and PaaS environments such as Amazon Web Services
  and Heroku. -->
* [Iron.io](http://www.iron.io/)はCeleryを含めた様々なタスクキューシステムをサポートしているメッセージングサービスプラットフォームです。Amazon Web ServiceやHerokuなど、他のIaaSやPaaSと連携することもできます。

<!-- * [Amazon Simple Queue Service (SQS)](http://aws.amazon.com/sqs/) is a
  set of five APIs for creating, sending, receiving, modifying and deleting
  messages. -->
* [Amazon Simple Queue Service (SQS)](http://aws.amazon.com/sqs/)はメッセージの作成・送信・受信・変更・削除のためのAPIが用意されています。

<!-- * [CloudAMQP](http://www.cloudamqp.com/) is at its core managed servers with
  RabbitMQ installed and configured. This service is an option if you are 
  using RabbitMQ and do not want to maintain RabbitMQ installations on your 
  own servers. -->
* [CloudAMQP](http://www.cloudamqp.com/)はRabbitMQが利用できるサーバを管理するのが本来のサービスです。自分のサーバでRabbitMQを使いたいが、インストールや管理が面倒という場合に利用することができます。

<!-- ## Task queue resources -->
## タスクキューを学ぶためのリソース

<!-- * [Getting Started Scheduling Tasks with Celery](http://www.caktusgroup.com/blog/2014/06/23/scheduling-tasks-celery/)
  is a detailed walkthrough for setting up Celery with Django (although
  Celery can also be used without a problem with other frameworks). -->
* [Getting Started Scheduling Tasks with Celery](http://www.caktusgroup.com/blog/2014/06/23/scheduling-tasks-celery/)はDjangoでCeleryを利用するためのガイドです。(Celelyは他のフレームワークでも問題なく利用できます。)

<!-- * [Distributing work without Celery](http://justcramer.com/2012/05/04/distributing-work-without-celery/)
  provides a scenario in which Celery and RabbitMQ are not the right tool
  for scheduling asynchronous jobs. -->
* [Distributing work without Celery](http://justcramer.com/2012/05/04/distributing-work-without-celery/)は、CeleryとRabbitMQが非同期処理のスケジュールに向かないケースについて説明しています。

<!-- * [Evaluating persistent, replicated message queues](http://www.warski.org/blog/2014/07/evaluating-persistent-replicated-message-queues/)
  is a detailed comparison of Amazon SQS, MongoDB, RabbitMQ, HornetQ and
  Kafka's designs and performance. -->
* [Evaluating persistent, replicated message queues](http://www.warski.org/blog/2014/07/evaluating-persistent-replicated-message-queues/)はAmazon SQS、MongoDB、RabbitMQ、HornetQ、Kafkaの設計とパフォーマンスを比較しています。

<!-- * [Queues.io](http://queues.io/) is a collection of task queue systems with
  short summaries for each one. The task queues are not all compatible with
  Python but ones that work with it are tagged with the "Python" keyword. -->
* [Queues.io](http://queues.io/)はタスクキューシステムの一覧とその概要を見ることができます。Pythonで利用できるもの以外のシステムもリストされていますが、Pythonで利用できるものは"Python"というキーワードでタグ付けされています。

<!-- * [Why Task Queues](http://www.slideshare.net/bryanhelmig/task-queues-comorichweb-12962619) 
  is a presentation for what task queues are and why they are needed.  -->
* [Why Task Queues](http://www.slideshare.net/bryanhelmig/task-queues-comorichweb-12962619)はタスクキューとは何なのか、そしてなぜ必要なのかを説明しているプレゼンテーションです。

<!-- * Flask by Example [Implementing a Redis Task Queue](https://realpython.com/blog/python/flask-by-example-implementing-a-redis-task-queue/)
  provides a detailed walkthrough of setting up workers to use RQ with
  Redis. -->
* [Implementing a Redis Task Queue](https://realpython.com/blog/python/flask-by-example-implementing-a-redis-task-queue/)は、FlaskとRQを使う例です。

<!-- * [How to use Celery with RabbitMQ](https://www.digitalocean.com/community/articles/how-to-use-celery-with-rabbitmq-to-queue-tasks-on-an-ubuntu-vps)
  is a detailed walkthrough for using these tools on an Ubuntu VPS. -->
* [How to use Celery with RabbitMQ](https://www.digitalocean.com/community/articles/how-to-use-celery-with-rabbitmq-to-queue-tasks-on-an-ubuntu-vps)はUbuntuをインストールしているVPS上でCeleryとRabbitMQを使う例です。

<!-- * Heroku has a clear walkthrough for using 
  [RQ for background tasks](https://devcenter.heroku.com/articles/python-rq). -->
* [RQ for background tasks](https://devcenter.heroku.com/articles/python-rq)では、バックグラウンドタスクにRQを使う方法を解説しています。

<!-- * [Introducing Celery for Python+Django](http://www.linuxforu.com/2013/12/introducing-celery-pythondjango/) 
  provides an introduction to the Celery task queue. -->
* [Introducing Celery for Python+Django](http://www.linuxforu.com/2013/12/introducing-celery-pythondjango/)はCeleryによるタスクキューの入門記事です。

<!-- * [Celery - Best Practices](https://denibertovic.com/posts/celery-best-practices/)
  explains things you should not do with Celery and shows some underused 
  features for making task queues easier to work with. -->
* [Celery - Best Practices](https://denibertovic.com/posts/celery-best-practices/)では、Celeryでやってはいけないこと、タスクキューを簡単に活用するための方法が紹介されています。

<!-- * The "Django in Production" series by 
  [Rob Golding](https://twitter.com/robgolding63) contains a post 
  specifically on [Background Tasks](http://www.robgolding.com/blog/2011/11/27/django-in-production-part-2---background-tasks/). -->
* [Rob Golding](https://twitter.com/robgolding63)による"Django in Production"シリーズに、[Background Tasks](http://www.robgolding.com/blog/2011/11/27/django-in-production-part-2---background-tasks/)という記事があります。

<!-- * [Asynchronous Processing in Web Applications Part One](http://blog.thecodepath.com/2012/11/15/asynchronous-processing-in-web-applications-part-1-a-database-is-not-a-queue/) 
  and [Part Two](http://blog.thecodepath.com/2013/01/06/asynchronous-processing-in-web-applications-part-2-developers-need-to-understand-message-queues/)
  are great reads for understanding the difference between a task queue and
  why you shouldn't use your database as one. -->
* [Asynchronous Processing in Web Applications Part One](http://blog.thecodepath.com/2012/11/15/asynchronous-processing-in-web-applications-part-1-a-database-is-not-a-queue/)と[Part Two](http://blog.thecodepath.com/2013/01/06/asynchronous-processing-in-web-applications-part-2-developers-need-to-understand-message-queues/)は、タスクキューとデータベースを利用して同等のことを行うことの違いについて理解するための素晴らしい記事です。

<!-- * [Celery in Production](http://www.caktusgroup.com/blog/2014/09/29/celery-production/)
  on the Caktus Group blog contains good practices from their experience 
  using Celery with RabbitMQ, monitoring tools and other aspects not often
  discussed in existing documentation. -->
* Cuktus Gruopのブログの[Celery in Production](http://www.caktusgroup.com/blog/2014/09/29/celery-production/)はCeleryとRabbitMQを利用した体験を基にした、監視ツールや他のドキュメントでは触れられることが少ない話題について言及している記事です。

<!-- * [A 4 Minute Intro to Celery](https://www.youtube.com/watch?v=68QWZU_gCDA) is
  a short introductory task queue screencast. -->
* [A 4 Minute Intro to Celery](https://www.youtube.com/watch?v=68QWZU_gCDA)はタスクキューに関する入門的なスクリーンキャストです。

<!-- * Heroku wrote about how to 
  [secure Celery](https://engineering.heroku.com/blogs/2014-09-15-securing-celery)
  when tasks are otherwise sent over unencrypted networks. -->
* Herokuは[secure Celery](https://engineering.heroku.com/blogs/2014-09-15-securing-celery)で、暗号化されていないネットワークでタスクを送信する際のCeleryをセキュアに運用する方法を解説しています。


<!-- ## Task queue learning checklist -->
## タスクキューを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i> 
<!-- Pick a slow function in your project that is called during an HTTP request. -->
あなたのWebアプリケーションの中で、HTTPリクエストに対する処理が遅い関数を探してください。

<i class="fa fa-check-square-o"></i> 
<!-- Determine if you can precompute the results on a fixed interval instead of
during the HTTP request. If so, create a separate function you can call
from elsewhere then store the precomputed value in the database. -->
HTTPリクエストを受け取った際に処理を始める代わりに、一定間隔で事前に処理ができるかを検討します。できるのであれば、他の場所から呼び出し可能な別の関数を書いて、データベースに前もって処理結果を格納しておきましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Read the Celery documentation and the links in the resources section below
to understand how the project works. -->
Celeryのドキュメントを読み、どのように利用できるのかを上記のリソースから学びましょう。

<i class="fa fa-check-square-o"></i>
<!-- Install a message broker such as RabbitMQ or Redis and then add Celery to your 
project. Configure Celery to work with the installed message broker. -->
RabbitMQやRedisのようなメッセージブローカーをインストールし、Celeryを導入してみましょう。インストールしたメッセージブローカーとCeleryが動作するように設定してみましょう。

<i class="fa fa-check-square-o"></i> 
<!-- Use Celery to invoke the function from step one on a regular basis. -->
最初のステップとしてCeleryで関数を実行してみましょう。

<i class="fa fa-check-square-o"></i>
<!-- Have the HTTP request function use the precomputed value instead of the 
slow running code it originally relied upon. -->
HTTPリクエストを受け取る関数で事前に処理されたデータを利用するようにしてみましょう。

<!-- ### What's next after task queues? -->
### タスクキューの次は？