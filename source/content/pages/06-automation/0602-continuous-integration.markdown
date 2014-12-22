title: Continuous Integration
category: page
slug: continuous-integration
sort-order: 0602
choice1url: ./logging.html
choice1icon: fa-align-left fa-inverse
choice1text: 運用中のアプリケーションで発生したイベントをロギングする方法は？
choice2url: ./web-application-security.html
choice2icon: fa-lock fa-inverse
choice2text: Webアプリケーションのセキュリティ対策は？
choice3url: ./api-integration.html
choice3icon: fa-link fa-inverse
choice3text: 外部APIを使うには？
choice4url:
choice4icon:
choice4text:

<!-- # Continuous Integration -->
# 継続的インテグレーション
<!-- Continuous integration (CI) automates building, testing and deploying
applications. -->
継続的インテグレーション（CI）はビルド、テスト、デプロイを自動化するための方法です。

<!-- ## Why is continuous integration important? -->
## 継続的インテグレーションはなぜ重要？
<!-- When CI is set up well it can dramatically reduce deployment times by
eliminating manual steps and ensure code does not have bugs that are being
checked by automated tests. Source code changes as a project evolves.
CI combined with unit and integration tests check that code modifications
do not break existing tests ensure the software works as intended. -->
CIを正しくセットアップすると、自動テストにより手動で動作確認するよりもデプロイにかかる時間を大幅に縮小できます。ソースコードはプロジェクトが進めば変わっていきます。CIをユニットテスト、インテグレーションテストと連携することで、コードの編集によりアプリケーションが壊れる心配は無くなるでしょう。

<!-- ## Continuous integration example -->
## 継続的インテグレーションの例
<!-- The following picture represents a high level perspective on how continuous
integration and deployment can work. -->
以下の図は、継続的インテグレーションとデプロイの役割を表したものです。

<img src="theme/img/continuous-integration.png" width="100%" class="technical-diagram" alt="継続的インテグレーションの一例" />

<!-- In the above diagram, when new code is commited to a source repository
there is a hook that notifies the continuous integration server that new
code needs to be built (the continuous integration server could also
poll the source code repository if a notification is not possible). -->
上の図ではレポジトリに新しいコードがコミットされたら、新しいコードをビルドするように、CIサーバに通知が送られます。（通知を送ることができないCIサーバの場合、レポジトリサーバを定期的にチェックする必要があります。）

<!-- The continuous integration server pulls the code to build and test it. If
all tests pass, the continuous integration server begins the deployment
process. The new code is pulled down to the server where the deployment is
taking place. Finally the deployment process is completed via restarting
services and related deployment activities. -->
CIサーバはコードを取り込みビルドとテストを行います。全てのテストが成功したらデプロイプロセスを始めます。デプロイが始まるとサーバへ新しいコードが取り込まれ、サービスの再起動や他のデプロイプロセスを行った後、デプロイプロセスが完了します。

<!-- There are many other ways a continuous integration server and its
deployments can be structured. The above was just one example of a
relatively simple set up. -->
CIサーバとデプロイのプロセスの構成方法は様々な形式があります。上で説明したセットアップはシンプルな構成例の一つでしかありません。


<!-- ## Open source CI projects -->
## オープンソースのCIプロジェクト

<!-- * [Jenkins](http://jenkins-ci.org/) is a common CI server for building and
  deploying to test and production servers.
  [Jenkins source code is on GitHub](https://github.com/jenkinsci/jenkins). -->
* [Jenkins](http://jenkins-ci.org/)はテストと本番環境のデプロイを構築するCIサーバの中でも一般的なソフトウェアです。[GitHub](https://github.com/jenkinsci/jenkins).

<!-- * [Go CD](http://www.go.cd/) is a CI server by
  [ThoughtWorks](http://www.thoughtworks.com/) that was designed with best
  practices for the build and test & release cycles in mind.
  [Go CD source code is on GitHub](https://github.com/gocd/gocd). -->
* [Go CD](http://www.go.cd/)は、[ThoughtWorks](http://www.thoughtworks.com/)によるベストプラクティスを基に設計されたCIサーバです。[GitHub](https://github.com/gocd/gocd)]

<!-- * [Strider](http://stridercd.com/) is a CI server written in node.js.
  [Strider source code is on GitHub](https://github.com/Strider-CD/strider). -->
* [Strider](http://stridercd.com/)はNode.js製のCIサーバです。[GitHub](https://github.com/Strider-CD/strider)

<!-- * [BuildBot](http://buildbot.net/) is a continuous integration **framework**
  with a set of components for creating your own CI server. It's written in
  Python and intended for development teams that want more controller over
  their build and deployment pipeline.
  [BuildBot source code is on GitHub](https://github.com/buildbot/buildbot). -->
* [BuildBot](http://buildbot.net/)はCI**フレームワーク**です。コンポーネントを組み合わせて、自分のCIサーバを作ることができます。Pythonで書かれていて、ビルドとデプロイプロセスをより柔軟にコントロールしたい場合に使用します。[GitHub](https://github.com/buildbot/buildbot)

<!-- ## Hosted CI services -->
## CIサービスのホスティング

<!-- * [Travis CI](https://travis-ci.org/) provides free CI for open source
  projects and has a [commercial version](https://travis-ci.com/) for
  private repositories. -->
* [Travis CI](https://travis-ci.org/)はオープンソースプロジェクトであれば無料で利用できます。プライベートリポジトリには[商用版](https://travis-ci.com/)を利用できます。

<!-- * [Bamboo](https://www.atlassian.com/software/bamboo) is
  [Atlassian](https://www.atlassian.com/)'s hosted continuous integration that
  is also free for open source projects. -->
* [Bamboo](https://www.atlassian.com/software/bamboo)は[Atlassian](https://www.atlassian.com/)がホスティングするCIサービスです。こちらもオープンソースプロジェクトであれば無料で利用できます。

<!-- * [Circle CI](https://circleci.com/) works with open or closed source projects
  on GitHub and can deploy them to Heroku if builds are successful. -->
* [Circle CI](https://circleci.com/)はGitHub上のオープン、クローズドなプロジェクトをHerokuにデプロイすることができます。

<!-- * [Shippable](https://www.shippable.com/) uses Docker containers to speed
  the build and integration process. It's free for public repositories. -->
* [Shippable](https://www.shippable.com/)はDockerコンテナを利用しビルドとインテグレーションプロセスを高速化することができます。パブリックレポジトリであれば無料で利用できます。

<!-- * [Drone](https://drone.io/) is another CI service that also provides free
  builds for open source projects. -->
* [Drone](https://drone.io/)もオープンソースプロジェクトが無料で利用できるCIサービスです。

<!-- * [Codeship](https://www.codeship.io/) provides continuous integration for
  Python 2.7. -->
* [Codeship](https://www.codeship.io/)はPython2.7対応のCIを提供しています。

<!-- * [Snap](https://snap-ci.com/) is a CI server and build pipeline tool for
  both integrating and deploying code. -->
* [Snap](https://snap-ci.com/)はCIサーバとビルドツールを提供しているサービスです。

<!-- ## Continuous integration resources -->
## CIを学ぶためのリソース

<!-- * [What is continuous integration?](http://martinfowler.com/articles/continuousIntegration.html)
  is a classic detailed article by Martin Fowler on the concepts behind CI
  and how to implement it. -->
* [What is continuous integration?](http://martinfowler.com/articles/continuousIntegration.html)はMartin FowlerによるCIのコンセプトと実装方法に関する記事です。

<!-- * [Continuous Deployment For Practical People](http://www.airpair.com/continuous-deployment/posts/continuous-deployment-for-practical-people)
  is not specific to Python but a great read on what it entails. -->
* [Continuous Deployment For Practical People](http://www.airpair.com/continuous-deployment/posts/continuous-deployment-for-practical-people)はPythonでの例ではありませんが、有用な記事です。

<!-- * [Continuous Integration & Delivery - Illustrated](http://bitcubby.com/continuous-integration-delivery-illustrated/)
  uses well done drawings to show how continuous integration and delivery
  works for testing and managing data. -->
* [Continuous Integration & Delivery - Illustrated](http://bitcubby.com/continuous-integration-delivery-illustrated/)はCIとデリバリーについてイラストで説明されている良記事です。

<!-- * [Diving into continuous integration as a newbie](http://www.rackspace.com/blog/diving-into-continuous-integration-as-a-newbie/)
  is a retrospective on learning CI from a Rackspace intern on how she learned
  the subject. -->
* [Diving into continuous integration as a newbie](http://www.rackspace.com/blog/diving-into-continuous-integration-as-a-newbie/)はRackspaceのインターン生が学んだことをまとめた記事です。

<!-- * [StackShare's Continuous Integration tag](http://stackshare.io/continuous-integration)
  lists a slew of hosted CI services roughly ranked by user upvotes. -->
* [StackShare's Continuous Integration tag](http://stackshare.io/continuous-integration)はユーザ投票によるCIホスティングサービスのランキングです。

<!-- ### What do you want to add to your application next? -->
### 次にアプリケーションへ何を追加しますか？
