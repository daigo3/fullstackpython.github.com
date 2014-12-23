title: Caching
category: page
slug: caching
sort-order: 0702
choice1url: ./task-queues.html
choice1icon: fa-tasks
choice1text: HTTPリクエスト・レスポンスのサイクル外でPythonを実行するには？
choice2url: ./web-analytics.html
choice2icon: fa-dashboard
choice2text: アクセス解析をすることで、ユーザの何を学ぶことができますか？
choice3url: ./web-application-security.html
choice3icon: fa-lock fa-inverse
choice3text: Webアプリケーションのセキュリティについて知っておくべきことは？
choice4url: ./configuration-management.html
choice4icon: fa-gears fa-inverse
choice4text: サーバの設定を自動化するには？

<!-- # Caching -->
# キャッシング
<!-- Caching can reduce the load on servers by storing the results of common 
operations and serving the precomputed answers to clients.  -->
キャッシングで、よくある操作の結果を保存しておいたり、クライアントへの応答を予め生成し配信することでサーバ上の負荷を減らすことができます。

<!-- For example, instead of retrieving data from database tables that rarely 
change, you can store the values in-memory. Retrieving values from an 
in-memory location is far faster than retrieving them from a database (which
stores them on a persistent disk like a hard drive.) When the cached values 
change the system can invalidate the cache and re-retrieve the updated values
for future requests. -->
例えば、ほとんど変更が加えられないようなデータベースのデータを利用せずに、そのようなデータをメモリ上に保管しておく方法が考えられます。メモリ上のデータは、ハードディスクのようなディスクを利用してデータを管理するデータベース上のデータよりも高速に処理することができます。キャッシュされたデータに変更があったら、システムはキャッシュしたデータを無効にし、以降のリクエストに備えて再度キャッシュし直します。

<!-- A cache can be created for multiple layers of the stack.  -->
キャッシュは様々なアプリケーションレイヤーで利用できます。

<!-- ## Caching backends -->
## キャッシュに利用できるシステム

<!-- * [memcached](http://memcached.org/) is a common in-memory caching system. -->
* [memcached](http://memcached.org/)は一般的に使われている、インメモリキャッシングシステムです。

<!-- * [Redis](http://redis.io/) is a key-value in-memory data store that can
  easily be configured for caching with libraries such as 
  [django-redis-cache](https://github.com/sebleier/django-redis-cache). -->
* [Redis](http://redis.io/)はキーバリュー形式のインメモリデータベースで、[django-redis-cache](https://github.com/sebleier/django-redis-cache)のようなライブラリを使って簡単に設定することができます。

<!-- ## Caching resources -->
## キャッシングを学ぶためのリソース

<!-- * "[Caching: Varnish or Nginx?](https://bjornjohansen.no/caching-varnish-or-nginx)"
  reviews some considerations such as SSL and SPDY support when choosing
  reverse proxy Nginx or Varnish. -->
* "[Caching: Varnish or Nginx?](https://bjornjohansen.no/caching-varnish-or-nginx)"では、NginxやVarnishをリバースプロキシに使う際に、SSLやSPDYをサポートする方法について考察しています。

<!-- * [Caching is Hard, Draw me a Picture](http://bizcoder.com/caching-is-hard-draw-me-a-picture)
  has diagrams of how web request caching layers work. The post is relevant
  reading even though the author is describing his Microsoft code as the 
  impetus for writing the content. -->
* [Caching is Hard, Draw me a Picture](http://bizcoder.com/caching-is-hard-draw-me-a-picture)では、リクエストのキャッシュがどのように行われているかを図式化しています。

<!-- ## Caching learning checklist -->
## キャッシングを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- Analyze your web application for the slowest parts. It's likely there are
complex database queries that can be precomputed and stored in an in-memory
data store. -->
あなたのWebアプリケーションの遅い部分を分析しましょう。それは、複雑なデータベースへのクエリで、インメモリデータストアで扱える可能性が高いです。

<i class="fa fa-check-square-o"></i>
<!-- Leverage your existing in-memory data store already used for session data
to cache the results of those complex database queries. 
A [task queue](/task-queues.html) can often be used to precompute the results 
on a regular basis and save them in the data store. -->
すでにセッションデータにインメモリデータストアを利用している場合は、複雑なデータベースへのクエリの結果をキャッシュするためにも利用しましょう。

<i class="fa fa-check-square-o"></i>
<!-- Incorporate a cache invalidation scheme so the precomputed results remain 
accurate when served up to the user. -->
キャッシュデータが正確に配信されるようにキャッシュを無効にする方法を取り入れましょう。


<!-- ### What do you want to learn now that your app is responding faster? -->
### アプリケーションを高速化したら、何を学びますか？