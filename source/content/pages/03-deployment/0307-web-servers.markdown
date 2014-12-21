title: Web Servers
category: page
slug: web-servers
sort-order: 0307
choice1url: ./wsgi-servers.html
choice1icon: fa-play fa-inverse
choice1text: Webサーバが行わないPythonの実行を行うには？
choice2url: ./application-dependencies.html
choice2icon: fa-archive fa-inverse
choice2text: サーバにPythonライブラリをインストールするには？
choice3url: ./static-content.html
choice3icon: fa-spinner
choice3text: 静的なコンテンツを配信する他の方法は？
choice4url: ./platform-as-a-service.html
choice4icon: fa-puzzle-piece fa-inverse
choice4text: サーバはやめて、PaaSについて知りたい。


<!-- # Web servers -->
# Webサーバ
<!-- Web servers respond to 
[Hypertext Transfer Protocol](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) (HTTP)
requests from clients and send back a response containing a status code and
often content such as HTML, XML or JSON as well. -->
Webサーバは[Hypertext Transfer Protocol](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) (HTTP)リクエストに対して、クライアントへステータスコード、HTML,XML、JSONなどのコンテンツとしてレスポンスを返します。

<!-- ## Why are web servers necessary? -->
## Webサーバはなぜ必要？
<!-- Web servers are the ying to the web client's yang. The server and client speak
the standardized language of the World Wide Web. This standard language
is why an old Mozilla Netscape browser can still talk to a modern Apache or
Nginx web server, even if it cannot properly render the page design like a 
modern web browser can.  -->
Webサーバが陰なら、Webクライアントは陽です。サーバとクライアントはWWWで標準化された言語で通信を行います。この標準言語のおかげで古いNetscapeでも、ページのデザインは崩れるかもしれませんが、モダンなApacheやNginxのWebサーバと通信することができるのです。

<!-- The basic language of the Web with the request and response cycle from 
client to server then server back to client remains the same as it was when
the Web was invented by 
[Tim Berners-Lee](http://www.w3.org/People/Berners-Lee/) at CERN in 1989.
Modern browsers and web servers have simply extended the language of the Web
to incorporate new standards. -->
クライアントからサーバへ送られ、サーバがクライアントへ返すというリクエストとレスポンスの仕組みとWeb上の基本的な言語は、1989年にCERNの[Tim Berners-Lee](http://www.w3.org/People/Berners-Lee/)がWebを発明した当時から変わっていません。モダンブラウザとWebサーバは新しい標準に対応するようにWebの言語を拡張してきました。

<!-- ## Client requests -->
## クライアントのリクエスト
<!-- A client that sends a request to a web server is usually a browser such 
as Internet Explorer, Firefox, or Chrome, but it can also be a -->
Webサーバへリクエストを送信するクライアントは、通常、Internet ExplorerやFirefox、Chromeのようなブラウザですが、以下もクライアントの一種です。

<!--* headless browser, commonly use for testing, such as [phantomjs](http://phantomjs.org/)
* commandline utility, for example [wget](https://www.gnu.org/software/wget/)and [curl](http://curl.haxx.se/)
* text-based web browser such as [Lynx](http://lynx.browser.org/)
* web crawler. -->

* [Phantomjs](http://phantomjs.org/)のような、一般的にテストに用いるヘッドレスブラウザ
* [wget](https://www.gnu.org/software/wget/)や[curl](http://curl.haxx.se/)のようなコマンドラインユーティリティ
* [Lynx](http://lynx.browser.org/)のようなテキストベースのWebブラウザ
* Webクローラー

<!-- Web server process requests from the above clients. The result of the web
server's processing is a 
[response code](https://developer.mozilla.org/en-US/docs/HTTP/Response_codes)
and commonly a content response. Some status codes, such as 204 (No content) 
and 403 (Forbidden), do not have content responses. -->
サーバは以上のようなクライアントからのリクエスト処理します。サーバによる処理の結果として[レスポンスコード](https://developer.mozilla.org/en-US/docs/HTTP/Response_codes)とコンテンツがレスポンスとして返されます。204 (No content)や403 (Forbidden)のような一部のコードにはコンテントは含まれません。

<!-- In a simple case, the client will request a static asset such as a picture
or JavaScript file. The file sits on the file system in a location the
web server is authorized to access and the web server sends the file
to the client with a 200 status code. If the client already requested the
file and the file has not changed, the web server will pass back a 304 
"Not modified" response indicating the client already has the latest version
of that file. -->
単純なケースとしてクライアントが画像やJavaScriptファイルのような静的なファイルをリクエストします。リクエストされたファイルはサーバのファイルシステム上にあり、アクセスが許可されるとWebサーバはクライアントへステータスコード200と一緒に返します。すでにファイルへのリクエストをしていて、ファイルにも変更がなければ304 "Not modified"を返しクライアントにはすでに最新のファイルを持っていることを知らせます。

<img src="theme/img/web-browser-server-requests.png" width="100%" class="technical-diagram" alt="Web server and web browser request-response cycle" />

<!-- A web server sends files to a web browser based on the web browser's 
request. In the first request, the browser accessed the 
"www.fullstackpython.com"
address and the server responded with the index.html HTML-formatted file. 
That HTML file contained references to other files, such as style.css and 
script.js that the browser then requested from the server. -->
Webサーバはブラウザのリクエストに応じてファイルをブラウザに送ります。最初のリクエストではぶらうざは"www.fullstackpython.com"というアドレスにアクセスし、サーバはindex.htmlというHTML形式のレスポンスを返します。そのHTMLファイルが他のファイルへの参照、例えばstyle.cssやscript.js、があればブラウザは続けてサーバへリクエストを送ります。

<!-- Sending static assets (such as CSS and JavaScript files) can eat up a 
large amount of bandwidth which is why using a Content Delivery Network 
(CDN) is important when possible (see the content delivery network 
section for a more detailed explanation). -->
CSSやJavaScriptのファイルのような静的なアセットは多くの通信を行うことがあるので、Content Delivery Network(CDN)を使うことが望ましいでしょう。（詳細はCDNの章を参照してください）

<!-- ## Web server resources -->
## Webサーバのリソース

<!-- * [HTTP/1.1 Specification](http://www.w3.org/Protocols/rfc2616/rfc2616.html) -->
* [HTTP/1.1 仕様](http://www.w3.org/Protocols/rfc2616/rfc2616.html)

* [How to set up a safe and secure Web server](http://arstechnica.com/gadgets/2012/11/how-to-set-up-a-safe-and-secure-web-server/)

* [Apache and mod\_wsgi on Ubuntu 10.04](http://library.linode.com/web-servers/apache/mod-wsgi/ubuntu-10.04-lucid)

* [Nginx web server tutorials](http://articles.slicehost.com/nginx)

* [Nginx for Developers: An Introduction](http://carrot.is/coding/nginx_introduction)

<!-- * An example of an [Nginx security configuration](http://tautt.com/best-nginx-configuration-for-security/). -->
* [Nginx security configuration](http://tautt.com/best-nginx-configuration-for-security/)の例.

<!-- * A reference with the full list of 
[HTTP status codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)
is provided by W3C. -->
* W3Cが提供している[HTTP ステータスコード](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)のリスト

<!-- * An optimization guide for 
"[battle ready Nginx](http://blog.zachorr.com/nginx-setup/)." -->
* Nginxの最適化ガイド "[battle ready Nginx](http://blog.zachorr.com/nginx-setup/)."

* [A faster Web server: ripping out Apache for Nginx](http://arstechnica.com/business/2011/11/a-faster-web-server-ripping-out-apache-for-nginx/)

* [4 HTTP Security Headers You Should Always Be Using](http://ibuildings.nl/blog/2013/03/4-http-security-headers-you-should-always-be-using)

<!-- * [Rate Limiting with Nginx](http://lincolnloop.com/blog/rate-limiting-nginx/)
  covers how to mitigate against brute force password guessing attempts using
  Nginx rate limits. -->
* [Rate Limiting with Nginx](http://lincolnloop.com/blog/rate-limiting-nginx/)では、Nginxのレート制限を使ってブルートフォース攻撃からパスワードのを守る方法が紹介されています。

<!-- ## Web servers learning checklist -->
## Webサーバを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- Choose a web server. [Nginx](http://nginx.org/en/) is recommended although 
[Apache](http://httpd.apache.org/) is also a great choice. -->
Webサーバを選択しましょう。[Nginx](http://nginx.org/en/)がお勧めですが、[Apache](http://httpd.apache.org/)も良い選択でしょう。

<i class="fa fa-check-square-o"></i>
<!-- Create an SSL certificate. For testing use a self-signed certificate and for a
production app buy one from [Digicert](http://www.digicert.com/). Configure 
the web server to serve traffic over SSL. You'll need SSL for serving only
HTTPS traffic and preventing security issues that occur with unencrypted user 
input. -->
SSL証明書を作成します。テスト目的なら自己署名の証明書、本番環境なら[Digicert](http://www.digicert.com/)などから買います。SSLを通じてWebサーバがコンテンツを配信できるように設定しましょう。SSLはHTTPSを使用する場合や、ユーザの入力を暗号化しない場合に起こるリスクを防ぐために必要です。

<i class="fa fa-check-square-o"></i>
<!-- Configure the web server to serve up static files such as CSS, JavaScript
and images. -->
CSS、JavaScript、画像などの静的ファイルを配信できるようにWebサーバを設定しましょう。

<i class="fa fa-check-square-o"></i>
<!-- Once you set up the [WSGI server](/wsgi-servers.html) you'll need to configure
the web server as a pass through for dynamic content. -->
[WSGIサーバ](/wsgi-servers.html)をセットアップしたら、Webサーバが動的なコンテンツを受け取ることができるように設定する必要があります。

<!-- ### What do you want to learn after the web server is set up? -->
### Websサーバを設定したら、次に何を学びますか？