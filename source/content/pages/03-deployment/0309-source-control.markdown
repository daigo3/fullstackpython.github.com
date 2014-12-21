title: Source Control
category: page
slug: source-control
sort-order: 0309
choice1url: ./deployment.html
choice1icon: fa-share
choice1text: 自分が作ったアプリケーションをデプロイするには？
choice2url: ./web-analytics.html
choice2icon: fa-dashboard
choice2text: 自分のアプリケーションを利用しているユーザについて知りたい。
choice3url: ./api-integration.html
choice3icon: fa-link
choice3text: 自分のアプリケーションで外部APIを使うには？
choice4url:
choice4icon:
choice4text:


<!-- # Source control -->
# ソース管理

<!-- Source control, also known as *version control*, stores software code files
with a detailed history of every modification made to those files. -->
ソース管理、または*バージョン管理*は、ソフトウェアのコードを記述したファイルを変更した履歴を管理しています。

<!-- ## Why is source control necessary? -->
## なぜソース管理が必要？

<!-- Version control systems allow developers to modify code without worrying 
about permanently screwing something up. Unwanted changes can be easily rolled
back to previous working versions of the code.  -->
バージョン管理をすることで、これまで作り上げたものを台無しにする心配をせずにコードを編集することができるようになります。コードの変更を無かったことにしたい場合も、前のバージョンのコードに巻き戻すことができます。


<!-- Source control also makes team software development easier. One developer 
can combine her code modifications with other developers' code through 
[diff](http://en.wikipedia.org/wiki/Diff) views that show line-by-line 
changes then merge the appropriate code into the main code branch. -->
また、ソース管理はチームでの開発を簡単に行えるようになります。ある開発者が他の開発者のコードを[diff](http://ja.wikipedia.org/wiki/Diff)によって1行づつ見比べることができるので、メインのコードブランチにマージすることができます。

<!-- Version control is a necessity on all software projects regardless of 
development time, codebase size or the programming language used. Every
project should immediately begin by using a version control system such
as Git or Mercurial. -->
バージョン管理は開発期間、規模、言語に関わらず必須です。すべてのプロジェクトで直ちにGitやMercurialの様なバージョン管理システムを導入するべきです。

<!-- ## Source control during deployment -->
## 開発中のソース管理

<!-- Pulling code during a deployment is a potential way source control systems fit
into the deployment process.  -->
開発段階において、開発中のコードを取り出すのがソース管理システムの用途です。

<img src="theme/img/app-source-control.png" width="100%" class="technical-diagram" alt="ソース管理システムからコードを取り出すためのサーバを利用する">

<!-- Note that some developers recommend deployment pipelines package the source 
code to deploy it and never have a production environment touch a source 
control system directly. However, for small scale deployments it's often
easiest to pull from source code when you're getting started instead of 
figuring out how to wrap the Python code in a system installation package. -->
デプロイにはソースコードをパッケージングし、プロダクション環境には一切ソース管理システムを利用しないというケースもあります。しかし、初学者にとってはシステムのインストールパッケージにPythonコードをパッケージングする方法を学び始めるよりも、小規模のデプロイにはソースコードを取り出して行うほうが簡単でしょう。

<!-- ## Source control projects -->
## ソース管理プロジェクト
<!-- Numerous source control systems have been created over the past several
decades. In the past, proprietary source control software offered features
tailored to large development teams and specific project workflows. However,
open source systems are now used for version control on the largest and most
complicated software projects in existence. There's no reason why your project
should use anything other than an open source version control system in
today's Python development world. The two primary choices are: -->
この2~30年の間様々なソース管理システムが作られてきました。過去にはプロプライエタリなソース管理ソフトウェアが大規模なプロジェクトチームのために作られたり、特定のプロジェクトに対応してきました。しかし、今日では最も巨大で複雑なプロジェクトが実際にオープンソースのバージョン管理システムを利用しています。今日のPythonプロジェクトでオープンソースのバージョン管理システムを使わない理由はありません。主な選択肢は2つです。

<!-- * [Git](http://git-scm.com/) is a free and open source distributed version
  control system. -->
* [Git](http://git-scm.com/)はフリーでオープンソースのバージョン管理システムです。

<!-- * [Mercurial](http://mercurial.selenic.com/) is similar to Git, also a free
  and open source distributed version control system. -->
* [Mercurial](http://mercurial.selenic.com/)はGitに似た、フリーでオープンなバージョン管理システムです。


<!-- ## Hosted source control services -->
## ソース管理のホスティング

<!-- Git and Mercurial can be downloaded and run on your own server. However,
it's easy and cheap to get started with a hosted version control service.
You can transition away from the service at a later time by moving your 
repositories if your needs change. A couple of recommended hosted version
control services are: -->
GitやMercurialはあなたのサーバにインストールして利用することができますが、ソース管理のホスティングサービスを使うほうが、扱いやすく経済的です。必要に応じて利用するサービスは変更できます。お勧めのホスティングサービスは2つです。

<!-- * [GitHub](https://github.com/) is currently the most commonly used source
  control platform for using Git. -->
* [GitHub](https://github.com/)は、現時点で最も利用されているGitホスティングサービスです。

<!-- * [BitBucket](https://bitbucket.org/) provides free Git and Mercurial 
  repositories for open projects and private repositories for up to five
  users. Users pay for hosting private repositories with more than five users. -->
* [BitBucket](https://bitbucket.org/)はGitとMercurialに対応し、5人までのチームであれば公開・非公開のレポジトリを無料でホスティングすることができます。

<!-- ## General source control resources -->
## 一般的なソース管理のリソース

<!-- * [Staging Servers, Source Control & Deploy Workflows, And Other Stuff Nobody Teaches You](http://www.kalzumeus.com/2010/12/12/staging-servers-source-control-deploy-workflows-and-other-stuff-nobody-teaches-you/) 
  is a comprehensive overview by Patrick McKenzie of why you need source 
  control. -->
* [Staging Servers, Source Control & Deploy Workflows, And Other Stuff Nobody Teaches You](http://www.kalzumeus.com/2010/12/12/staging-servers-source-control-deploy-workflows-and-other-stuff-nobody-teaches-you/)はPatrick McKenzieによる、なぜソース管理が必要なのかを解説した記事です。

<!-- * [Version control best practices](https://blog.rainforestqa.com/2014-05-28-version-control-best-practices/)
  is a good write up of how to work with version control systems. The post is 
  part of an ongoing deployment guide written by the folks at 
  [Rainforest](https://www.rainforestqa.com/). -->
* [Version control best practices](https://blog.rainforestqa.com/2014-05-28-version-control-best-practices/)は、バージョン管理システムの利用方法について書かれています。記事は[Rainforest](https://www.rainforestqa.com/)によってフォークされ、継続しています。

<!-- * This lighthearted guide to the 
  [ten astonishments in version control history](http://www.flourish.org/blog/?p=397) 
  is a fun way to learn how systems developed over the past several decades. -->
* [ten astonishments in version control history](http://www.flourish.org/blog/?p=397)は、ソフトウェア開発の歴史について楽しく学ぶことができます。

<!-- * [A visual guide to version control](http://betterexplained.com/articles/a-visual-guide-to-version-control/) 
  is a detailed article with real-life examples for why version control is
  necessary in software development. -->
* [A visual guide to version control](http://betterexplained.com/articles/a-visual-guide-to-version-control/)は、なぜバージョン管理が必要なのかということが実践的なバージョン管理とともに解説されています。

<!-- * [An introduction to version control](http://guides.beanstalkapp.com/version-control/intro-to-version-control.html) 
  shows the basic concepts behind version control systems. -->
* [An introduction to version control](http://guides.beanstalkapp.com/version-control/intro-to-version-control.html)では、バージョン管理の基本的なコンセプトについて解説されています。

<!-- * [What Is Version Control? Why Is It Important For Due Diligence?](http://oss-watch.ac.uk/resources/versioncontrol) 
  explains the benefits and necessity of version control systems. -->
* [What Is Version Control? Why Is It Important For Due Diligence?](http://oss-watch.ac.uk/resources/versioncontrol)ではバージョン管理システムの恩恵と必要性について解説されています。

<!-- * [About version control](http://git-scm.com/book/en/Getting-Started-About-Version-Control) 
reviews the basics of distributed version control systems. -->
* [About version control](http://git-scm.com/book/en/Getting-Started-About-Version-Control)では、分散型バージョン管理システムの基礎について解説されています。


<!-- ## Git resources -->
## Gitのリソース

<!-- * [Pro Git](http://git-scm.com/book) is a free open source book that walks 
  through all aspects of using the version control system. -->
* [Pro Git](http://git-scm.com/book)はバージョン管理システムを利用に関して、すべてを網羅したオープンな書籍です。

<!-- * [A Hacker's Guide to Git](http://wildlyinaccurate.com/a-hackers-guide-to-git)
  covers the basics as well as more advanced Git commands while explaining each
  step along the way. -->
* [A Hacker's Guide to Git](http://wildlyinaccurate.com/a-hackers-guide-to-git)は、Gitコマンドの基礎と応用を学ぶことができます。

<!-- * [A practical git introduction](http://mrchlblng.me/2014/09/practical-git-introduction/)
  is exactly what the title says it is. This is a well written guide with 
  plenty of code snippets to get you up to speed with Git. -->
* [A practical git introduction](http://mrchlblng.me/2014/09/practical-git-introduction/)はタイトル通り、実践的なGitガイドです。Gitの使用を加速する豊富なコードとともに詳細な解説が掲載されています。

<!-- * [git ready](http://gitready.com/) has a nice collection of blog posts based on
  beginner, intermediate and advanced Git use cases. -->
* [git ready](http://gitready.com/)は初心者向けから中級者、上級者向けに分けれられたGitの利用方法について解説しているブログです。

<!-- * [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) details
  a Git branching model for small teams. -->
* [git-flow](http://nvie.com/posts/a-successful-git-branching-model/)は、小規模なチームに最適なブランチモデルについて解説しています。

<!-- * [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html) builds on
  git-flow, goes over some of the issues that arise with it and presents a
  few solutions to those problems. -->
* [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)はgit-flowをベースに構築され、その問題点と解決方法を紹介しています。

<!-- * [Git Workflows That Work](http://blog.endpoint.com/2014/05/git-workflows-that-work.html)
  is a helpful post with diagrams to show how teams can create a Git workflow
  that will help their development process. -->
* [Git Workflows That Work](http://blog.endpoint.com/2014/05/git-workflows-that-work.html)は、チームでGitを使う際に参考となる、ワークフローのダイアグラムを紹介しています。

<!-- * "[Our Git Workflow](http://www.braintreepaymentsolutions.com/devblog/our-git-workflow)"
  by Braintree goes over how this payments company uses Git for development
  and merging source code. -->
* "[Our Git Workflow](http://www.braintreepaymentsolutions.com/devblog/our-git-workflow)"はBraintreeがGitを使いソースコードをマージするためのノウハウを紹介しています。


<!-- ## Source control learning checklist -->
## ソース管理を学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- Pick a version control system. Git is recommended because on the web there 
are a significant number of tutorials to help both new and advanced users. -->
バージョン管理システムを選択しましょう。Web上のリソース、チュートリアルの数、様々なレベルのユーザ層の数からすると、Gitがお勧めです。

<i class="fa fa-check-square-o"></i>
<!-- Learn basic use cases for version control such as committing changes, rolling 
back to earlier file versions and searching for when lines of code were 
modified during development history. -->
変更のコミット、変更の取り消し、履歴から変更箇所を探す方法など、基本的な使い方を学びましょう。

<i class="fa fa-check-square-o"></i>
<!-- Ensure your source code is backed up in a central repository. A central
repository is critical not only if your local development version is corrupted
but also for the deployment process. -->
あなたのソースコードが中央のレポジトリにパックアップされているかを確認して下さい。中央レポジトリは、ローカルの開発バージョンが壊れた場合だけでなく、開発段階でも重要なものです。

<i class="fa fa-check-square-o"></i>
<!-- Integrate source control into your deployment process in three ways. First,
pull the project source code from version control during deployments. Second, 
kick off deployments when code is modified by using webhooks or polling on 
the repository. Third, ensure you can roll back to a previous version if a 
code deployment goes wrong. -->
3つの方法であなたの開発プロセスにソース管理を組み込みましょう。まずはデプロイ時にバージョン管理システムからソースコードを取り出します。次にコードが変更されたらデプロイが起こるようにwebhookやレポジトリのポーリングをしてみます。最後に開発が間違ったら以前のバージョンに巻き戻すことができることを確認しましょう。


<!-- ### Now that your source code is versioned, what's next? -->
### あなたのソースコードはバージョン管理されました。次は？