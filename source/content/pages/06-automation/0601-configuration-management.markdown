title: Configuration Management
category: page
slug: configuration-management
sort-order: 061
choice1url: ./continuous-integration.html
choice1icon: fa-refresh
choice1text: 自分のプロジェクトのコードを継続的に統合するには？
choice2url: ./web-analytics.html
choice2icon: fa-dashboard
choice2text: Web解析でユーザについて知るには？
choice3url: ./api-integration.html
choice3icon: fa-link fa-inverse
choice3text: 自分のアプリケーションから外部APIを利用するには？
choice4url: ./web-application-security.html
choice4icon: fa-lock fa-inverse
choice4text: Webアプリケーションのセキュリティについて知っておくべきことは？


<!-- # Configuration Management -->
# 構成管理
<!-- Configuration management involves modifying servers from an existing state to 
a desired state and automating how an application is deployed. -->
構成管理とはサーバの状態を必要な状態に変更し、アプリケーションのデプロイを自動化することです。

<!-- ## Configuration management tools -->
## 構成管理ツール
<!-- Numerous tools exist to modify server state in a controlled 
way, including [Puppet](http://puppetlabs.com/puppet/what-is-puppet), 
[Chef](http://www.getchef.com/chef/), 
[SaltStack](http://www.saltstack.com/), and Ansible. Puppet and Chef are
written in Ruby, while SaltStack and Ansible are written in Python. -->
サーバの状態を設定することを管理するためのツールには、[Puppet](http://puppetlabs.com/puppet/what-is-puppet)、[Chef](http://www.getchef.com/chef/)、[SaltStack](http://www.saltstack.com/)やAnsibleがあります。PuppetとChefはRubyで書かれていますが、SaltStackとAnsibleはPythonで書かれています。

<!-- ## Ad hoc tasks -->
## アドホックなタスク
<!-- Configuration management tools such as Chef, Puppet, Ansible, and SaltStack
are not useful for performing ad hoc tasks that require interactive responses.
[Fabric](http://docs.fabfile.org/en/1.8/) and 
[Invoke](http://docs.pyinvoke.org/en/latest/) are used for interactive 
operations, such as querying the database from the Django manage.py shell. -->
Chef、Puppet、SaltStack、Ansibleのような構成管理ツールは、インタラクティブな応答を必要とするアドホックなタスクには向いていません。[Fabric](http://docs.fabfile.org/en/1.8/)や[Invoke](http://docs.pyinvoke.org/en/latest/)では、Djangoのmanage.pyによるShellでデータベースを操作するような対話的な操作が可能です。

<!-- ## Configuration management tool comparisons -->
## 構成管理ツールの比較

<!-- * [Moving away from Puppet: SaltStack or Ansible?](http://ryandlane.com/blog/2014/08/04/moving-away-from-puppet-saltstack-or-ansible/)
  is an openly biased but detailed post on why to choose SaltStack over 
  Ansible in certain situations. -->
* [Moving away from Puppet: SaltStack or Ansible?](http://ryandlane.com/blog/2014/08/04/moving-away-from-puppet-saltstack-or-ansible/)では、バイアスがかかっているものの、特定の状況でAnsibleよりもSaltStackを選ぶ理由について、詳細に述べられています。
  
<!-- * [Ansible vs. Shell Scripts](http://devopsu.com/blog/ansible-vs-shell-scripts/)
  provides some perspective on why a configuration management tool is better
  than old venerable shell scripts. -->
* [Ansible vs. Shell Scripts](http://devopsu.com/blog/ansible-vs-shell-scripts/)では、由緒正しいShellScriptよりも構成管理ツールを使うべき理由についての意見が述べられています。

* [Ansible and Salt: A Detailed Comparison](http://missingm.co/2013/06/ansible-and-salt-a-detailed-comparison/)


## Ansible
<!-- [Ansible](http://www.ansibleworks.com/) is an open source configuration
management and application deployment tool built in Python. -->
[Ansible](http://www.ansibleworks.com/)は、Pythonで書かれたオープンソースの構成管理、デプロイメントツールです。

<!-- ### Ansible Resources -->
### Ansibleのリソース

* [Official Ansible documentation](http://docs.ansible.com/index.html)

<!-- * [An Ansible tutorial](https://serversforhackers.com/editions/2014/08/26/getting-started-with-ansible/)
  is a fantastically detailed introduction to using Ansible to set up
  servers. -->
* [An Ansible tutorial](https://serversforhackers.com/editions/2014/08/26/getting-started-with-ansible/)は、サーバのセットアップにAnsibleを利用するための詳細な入門記事です。

* [Ansible Weekly Newsletter](http://devopsu.com/newsletters/ansible-weekly-newsletter.html)

* [Python for Configuration Management with Ansible slides](http://www.insom.me.uk/post/pycon-talk.html) 
from PyCon UK 2013

* [First Steps with Ansible](http://labs.qandidate.com/blog/2013/11/15/first-steps-with-ansible/)

* [Red Badger on Ansible](http://red-badger.com/blog/2013/06/29/ansible/)

* [Getting Started with Ansible](http://lowendbox.com/blog/getting-started-with-ansible/)

<!-- * [Ansible Text Message Notifications with Twilio SMS](https://www.twilio.com/blog/2014/05/ansible-text-messages-notifications-with-twilio-sms.html)
  is my blog post with a detailed example for using the Twilio module in
  core Ansible 1.6+. -->
* [Ansible Text Message Notifications with Twilio SMS](https://www.twilio.com/blog/2014/05/ansible-text-messages-notifications-with-twilio-sms.html)は、Ansible1.6以上でTwilioモジュールを利用したサンプルを紹介した、著者のブログです。

* [Ansible and Linode](http://softwareas.com/ansible-and-linode-what-i-learned-about-controlling-linodes-from-ansible)

* [Multi-factor SSH authentication with Ansible and Duo Security](http://jlafon.io/ansible-duo-security.html)

* [Introducing Ansible into Legacy Projects](http://benlopatin.com/getting-started-with-ansible/)

* [Automating your development environment with Ansible](http://www.nickhammond.com/automating-development-environment-ansible/)

* [Post-install steps with Ansible](http://devopsu.com/guides/ansible-post-install.html) 

* [First Five (and a half) Minutes on a Server with Ansible](http://lattejed.com/first-five-and-a-half-minutes-on-a-server-with-ansible) 

* [(Detailed) Introduction to Ansible](http://davidwinter.me/articles/2013/11/23/introduction-to-ansible/)

* [6 practices for super smooth Ansible experience](http://hakunin.com/six-ansible-practices)

<!-- * [Shippable + Ansible + Docker + Loggly for awesome deployments](http://www.hiddentao.com/archives/2014/06/03/shippable-ansible-docker-loggly-for-awesome-deployments/)
  is a well written detailed post about using Docker and Ansible together with
  a few other pieces. -->
* [Shippable + Ansible + Docker + Loggly for awesome deployments](http://www.hiddentao.com/archives/2014/06/03/shippable-ansible-docker-loggly-for-awesome-deployments/)はDockerとAnsible、その他ツールを利用方法が書かれた詳細な記事です。

* [Create a Couchbase Cluster with Ansible](http://blog.couchbase.com/create-couchbase-cluster-with-ansible)

* [Idempotence, convergence, and other silly fancy words we often use](https://groups.google.com/forum/#!msg/Ansible-project/WpRblldA2PQ/lYDpFjBXDlsJ)

* [How to Write an Ansible Role for Ansible Galaxy](http://probablyfine.co.uk/2014/03/27/how-to-write-an-ansible-role-for-ansible-galaxy/)

* [Testing with Jenkins, Docker and Ansible](http://blog.mist.io/post/82383668190/move-fast-and-dont-break-things-testing-with)


<!-- ## Application dependencies learning checklist -->

<i class="fa fa-check-square-o"></i>
<!-- Learn about configuration management in the context of deployment automation
and infrastructure-as-code. -->
デプロイの自動化、コードによるインフラ管理との関連として構成管理を学びましょう。

<i class="fa fa-check-square-o"></i>
<!-- Pick a configuration management tool and stick with it. My recommendation is
Ansible because it is by far the easiest tool to learn and be productive with. -->
構成管理ツールを選びましょう。簡単に学び、使うことができるのでAnsibleがお勧めです。

<i class="fa fa-check-square-o"></i>
<!-- Read your configuration management tool's documentation and, when necessary,
the source code. -->
選択した構成管理ツールのドキュメントと、必要であればソースコードを読みましょう。

<i class="fa fa-check-square-o"></i>
<!-- Automate the configuration management and deployment for your project. Note
that this is by far the most time consuming step in this checklist but will
pay dividends every time you deploy your project. -->
構成管理とデプロイを自動化してみましょう。このチェックリストの項目の中で、最も時間がかかると思いますが、デプロイをする度に恩恵を受けることができます。

<i class="fa fa-check-square-o"></i>
<!-- Hook the automated deployment tool into your existing deployment process. -->
既存のデプロイプロセスにデプロイの自動化を組み込みましょう。

<!-- ### What's next after automating your app configuration? -->
### アプリケーションの構成を自動化した次は？