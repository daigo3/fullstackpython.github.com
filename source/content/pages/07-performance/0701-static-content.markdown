title: Static Content
category: page
slug: static-content
sort-order: 0701
choice1url: ./caching.html
choice1icon: fa-repeat
choice1text: 繰り返し行われる操作をキャッシュしてパフォーマンスを改善するには？
choice2url: ./web-analytics.html
choice2icon: fa-dashboard
choice2text: アクセス解析をすることで、ユーザの何を学ぶことができますか？
choice3url: ./web-application-security.html
choice3icon: fa-lock fa-inverse
choice3text: Webアプリケーションのセキュリティについて知っておくべきことは？
choice4url: ./configuration-management.html
choice4icon: fa-gears fa-inverse
choice4text: サーバの設定を自動化するには？


<!-- # Static content -->
# 静的コンテンツ
<!-- Some content on a website does not change and therefore should be served
up either directly through the web server or a content delivery network (CDN).
Examples include JavaScript, image, and CSS files. -->
Webサイトのいくつかのコンテンツには、それ自体に変更を行わない種類のものがあり、直接WebサーバやContent Delivery Network(CDN)から配信することがあります。例えば、JavaScriptや画像、CSSのようなファイルです。

<!-- ## Types of static content -->
## 静的コンテンツの種類
<!-- Static content can be either assets created as part of your development
process such as images on your landing page or user-generated content. The 
Django framework calls these two categories *assets* and *media*. -->
静的コンテンツにはランディンページに利用する画像や、ユーザが作成するコンテンツなど、開発プロセス中に生成されるものもあります。Djangoではこれらを*assets*、*media*と呼びます。

<!-- ## Content delivery networks -->
## Content Delivery Network
<!-- A content delivery network (CDN) is a third party that stores and serves 
static files. [Amazon CloudFront](http://aws.amazon.com/cloudfront/),
[Akamai](http://www.akamai.com/), and 
[Rackspace Cloud Files](http://www.rackspace.com/cloud/public/files/) 
are examples of CDNs. The purpose of a CDN is to remove the load of static
file requests from web servers that are handling dynamic web content. For
example, if you have an nginx server that handles both static files and 
acts as a front for a Green Unicorn WSGI server on a 512 megabyte 
virtual private server, the nginx server will run into resource 
constraints under heavy traffic. A CDN can remove the need to serve static
assets from that nginx server so it can purely act as a pass through for 
requests to the Green Unicorn WSGI server. -->
Content Delivery Network(CDN)は静的コンテンツを保管し、配信するためのサービスです。[Amazon CloudFront](http://aws.amazon.com/cloudfront/)、[Akamai](http://www.akamai.com/)や[Rackspace Cloud Files](http://www.rackspace.com/cloud/public/files/)などがあります。CDNの目的は動的なWebコンテンツが扱う静的コンテンツへのリクエストの読み込みを無くすことです。例えば、512MBのVPSで静的コンテンツの配信と、Gunicorn WSGIサーバのフロントとしてNGINXを利用した場合、アクセスが多くなると圧迫した状態で動作することになります。CDNを利用することで静的コンテンツの配信をGunicornへのリクエストのパフォーマンスが下がること無く、静的コンテンツの配信を行うことができるようになります。

<!-- CDNs send content responses from data centers with the closest proximity to the requester. -->
CDNはリクエスト元に近いデータセンターからレスポンスが送られるようになっています。

<!-- ## Static Content Resources -->
## 静的コンテンツを学ぶためのリソース

<!-- * [The super stupid idiot's guide to getting started with Django, Pipeline, and S3](http://blog.iambob.me/the-super-stupid-idiots-guide-to-getting-started-with-django-pipeline-and-s3/)
  shows how to host static content on S3 and use those files with Django. -->
* [The super stupid idiot's guide to getting started with Django, Pipeline, and S3](http://blog.iambob.me/the-super-stupid-idiots-guide-to-getting-started-with-django-pipeline-and-s3/)では、S3で静的コンテンツをホストし、Djangoで利用する方法を解説しています。

<!-- * [Crushing, caching and CDN deployment in Django](http://tech.marksblogg.com/crushing-caching-cdn-django.html)
  shows how to use django-compressor and a CDN to scale static and media
  file serving.-->
* [Crushing, caching and CDN deployment in Django](http://tech.marksblogg.com/crushing-caching-cdn-django.html)では、Django Compressorの使い方、静的コンテンツとメディアファイルの配信のスケールにCDNを利用する方法を解説しています。

* [Using Amazon S3 to host your Django static files](http://blog.doismellburning.co.uk/2012/07/14/using-amazon-s3-to-host-your-django-static-files/)

* [CDNs fail, but your scripts don't have to](http://www.hanselman.com/blog/CDNsFailButYourScriptsDontHaveToFallbackFromCDNToLocalJQuery.aspx)

<!-- * [django-storages](http://django-storages.readthedocs.org/en/latest/) is 
a Django library for managing static and media files on services such as
Amazon S3 and other content delivery networks. -->
* [django-storages](http://django-storages.readthedocs.org/en/latest/)は、静的コンテンツ、メディアファイルをAmazonS3などのCDN上で管理するためのDjangoライブラリです。

<!-- ## Static content learning checklist -->
## 静的コンテンツを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- Identify a content delivery network to offload serving static content files
from your local web server. I recommend using Amazon S3 with CloudFront as 
it's easy to set up and will scale to high bandwidth demands. -->
ローカルのWebサーバの代わりに、静的コンテンツを配信するために利用するCDNを決めましょう。Amazon S3とCloundFrontを使うと、セットアップやスケールアップを簡単にできます。

<i class="fa fa-check-square-o"></i>
<!-- Update your web application deployment process so updated static files are
uploaded to the CDN.  -->
Webアプリケーションの開発プロセスで、静的コンテンツを更新したらCDNにアップロードされるようにしてみましょう。

<i class="fa fa-check-square-o"></i>
<!-- Move static content serving from the www subdomain to a static (or similarly
named) subdomain so browsers will load static content in parallel to www
HTTP requests. -->
静的コンテンツをwwwサブドメインで提供する代わりに、static(または類似した名前）サブドメインで配信し、wwwサブドメインへのHTTPリクエストと分散するように静的コンテンツが読み込まれるようにしましょう。


<!-- ### What's next for building your app? -->
### Webアプリケーションを構築するために、次にすることは？