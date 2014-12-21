title: Operating Systems
category: page
slug: operating-systems
sort-order: 0306
choice1url: ./web-servers.html
choice1icon: fa-cloud
choice1text: LinuxをOSとして採用したら、どのWebサーバを使えば良いですか？
choice2url: ./application-dependencies.html
choice2icon: fa-archive fa-inverse
choice2text: 新しいOSにPythonのライブラリをインストールする方法は？
choice3url: ./platform-as-a-service.html
choice3icon: fa-puzzle-piece fa-inverse
choice3text: サーバはやめて、PaaSについて知りたい。
choice4url:
choice4icon:
choice4text:


<!-- # Operating Systems -->
# オペレーティングシステム
<!-- An operating system runs on the server or virtual server and controls access 
to computing resources. The operating system also includes a way to install
programs necessary for running your Python web application. -->
サーバや仮想サーバ上で動作するオペレーティングシステムは、コンピュータのリソースへのアクセスを管理しています。また、オペレーティングシステムはPythonのWebアプリケーションを動作させるために必要なプログラムをインストールする方法も提供します。

<!-- ## Why are operating systems necessary? -->
## なぜオペレーティングシステムが必要？
<!-- An operating system makes many of the computing tasks we take for granted easy.
For example, the operating system enables writing to files, 
communicating over a network and running multiple programs at once. 
Otherwise you'd need to control the CPU, memory, network, graphics card, 
and many other components with your own low-level implementation. -->
オペレーティングシステムは様々な演算処理を簡単に行えるようにしてくれます。例えば、ファイルへの書き込みやネットワーク越しの通信、一度に複数のプログラムを実行といったことです。さもなければ、あなた自身がCPU、メモリ、ネットワーク、グラフィックカードなどの低レベルな実装を行わなければなりません。

<!-- Without using an existing operating system like Linux, Mac OS X, or Windows,
you'd be forced to write a new operating system as part of your web 
application.  It would be impossible to write features for your Python 
web application because you'd be too busy hunting down a memory leak in 
your assembly code, if you even were able to get that far. -->
LinuxやMac OS X、Windowsのような既存のオペレーティングシステムを使う場合を除けば、Webアプリケーションの一部として、新しいオペレーティングシステムを書かなくてはなりません。これではPythonのWebアプリケーションの処理を書くことは不可能です。アセンブラのコードのメモリリークを探すのに忙しくそんな暇はありません。

<!-- Fortunately, the open source community provides Linux to the Python world 
as a rock solid free operating system for running our applications. -->
幸運にも、Pythonの世界にはオープンソースのコミュニティによって、Webアプリケーションを動かすために使用することができるLinuxが提供されています。

<!-- ## Recommended operating systems -->
## お勧めのオペレーティングシステム
<!-- The only recommended operating system for production Python web stack 
deployments is Linux. There are several Linux distributions commonly used 
for running production servers. Ubuntu Long Term Support (LTS) releases, 
Red Hat Enterprise Linux, and CentOS are all viable options.  -->
本番環境でPythonのWebアプリケーションを動かすためのオペレーティングシステムとしておすすめするのはLinuxです。Linuxにはいくつかのディストリビューションがあり、本番サーバを稼働するのに一般的に使われています。Ubuntu Long Term Support(LTS)リリースや、Red Hat Enterprise Linux、CentOSが良い選択肢でしょう。

<!-- Mac OS X is fine for development activities. Windows and Mac 
OS X are not appropriate for production deployments unless there is a 
major reason why you must use them in lieu of Linux. -->
Mac OS Xは開発環境に向いています。Linuxではなく、WindowsやMac OS Xを使わなければならない明確な理由が無い限り、本番環境にはLinuxを利用すことをお勧めします。

### Ubuntu
<!-- Ubuntu is a Linux distribution packaged by the 
[Canonical Ltd](http://www.canonical.com/) company. Ubuntu uses the
Debian distribution as a base for packages, including the 
[aptitude package manager](http://wiki.debian.org/Apt). For desktop versions 
of Ubuntu, GNOME (until the 11.04 release) or Unity (11.10 through current)
is bundled with the distribution to provide a user interface. -->
Ubuntuは[Canonical Ltd](http://www.canonical.com/)社によって開発されているLinuxディストリビューションです。Ubuntuは[aptitude package manager](http://wiki.debian.org/Apt)を含むDebianディストリビューションのパッケージをベースに使用しています。

<!-- Ubuntu [Long Term Support](https://wiki.ubuntu.com/LTS) (LTS) releases
are the recommended versions to use for deployments. LTS versions receive
five years of post-release updates from Canonical. Every two years, Canonical 
creates a new LTS release, which allows for an easy upgrade path as well 
as flexibility in skipping every other LTS release if necessary. As of
November 2014, [14.04 Trusty Tahr](http://releases.ubuntu.com/14.04/)
is the latest Ubuntu LTS release. -->
Ubuntu [LTS](https://wiki.ubuntu.com/LTS)は開発向けにお勧めのバージョンです。LTS版はCanonicalによるポストリリース更新が5年間続きます。2年毎にCanonicalは新しいLTSをリリースし、簡単にアップグレードが行え、また必要であれば更新をスキップすることも柔軟にできます。2014年11月時点で[14.04 Trusty Tahr](http://releases.ubuntu.com/14.04/)が最新のUbuntu LTSです。

<!-- #### Ubuntu Python Packages -->
#### Ubuntu Pythonパッケージ
<!-- There are several 
[Aptitude](https://help.ubuntu.com/12.04/serverguide/aptitude.html)
packages found on Linux servers running a Python stack. These packages are:  -->
LinuxsサーバでPythonアプリケーションを運用するには複数の[Aptitude](https://help.ubuntu.com/12.04/serverguide/aptitude.html)パッケージがあります。

<!-- * [python-dev](http://packages.ubuntu.com/precise/python-dev) for header
  files and static library for Python -->
* [python-dev](http://packages.ubuntu.com/precise/python-dev)はPythonのためのヘッダファイルとスタティックライブラリです。

<!-- * [python-virtualenv](http://packages.ubuntu.com/precise/python-virtualenv)
  for creating and managing Python 
  [virtualenvs](http://www.virtualenv.org/en/latest/) to isolate library
  dependencies -->
* [python-virtualenv](http://packages.ubuntu.com/precise/python-virtualenv)は、ライブラリの依存関係を独立して管理するためのPythonの[virtualenvs](http://www.virtualenv.org/en/latest/)を作ったり管理するためのパッケージです。

<!-- ### Red Hat and CentOS -->
### Red HatとCentOS
<!-- [Red Hat Enterprise Linux](http://www.redhat.com/products/enterprise-linux/)
(RHEL) and [Community ENTerprise Operating System](http://www.centos.org/)
(CentOS) are the same distribution. The primary difference between the two 
is that CentOS is an open source, liberally licensed free derivative of RHEL. -->
[Red Hat Enterprise Linux](http://www.redhat.com/products/enterprise-linux/)
(RHEL)と[Community ENTerprise Operating System](http://www.centos.org/)
(CentOS)は同じディストリビューションです。大きな違いはCentOSはオープンソースでRed Hatの派生物を無償で利用します。

<!-- RHEL and CentOS use a different package manager and command-line interface 
from Debian-based Linux distributions: RPM Package Manager (RPM) and the 
Yellowdog Updater, Modified (YUM). RPM has a specific .rpm file format
to handle the packaging and installation of libraries and applications. YUM
provides a command-line interface for interacting with the RPM system. -->
Red HatとCentOSはDebianベースのLinuxディストリビューションとは異なるパッケージマネージャとコマンドラインインタフェースを利用します。RPMパッケージマネージャとYellowdog Updater, Modified(YUM)です。RPMは`.rpm`ファイルを使ってパッケージングの管理とライブラリやアプリケーションのインストールを行います。YUMはRPMシステムをコマンドラインで利用するためのツールです。

<!-- ## Operating System Resources -->
## オペレーティングシステムのリソース
<!-- * [What is a Linux distribution and how do I choose the right one?](http://www.linux.org/threads/selecting-a-linux-distribution.4087/) -->
* [What is a Linux distribution and how do I choose the right one?](http://www.linux.org/threads/selecting-a-linux-distribution.4087/)

<!-- * Lifehacker's [guide to choosing a Linux distro](http://lifehacker.com/5889950/how-to-find-the-perfect-linux-distribution-for-you). -->
* Lifehackerの[guide to choosing a Linux distro](http://lifehacker.com/5889950/how-to-find-the-perfect-linux-distribution-for-you).

* [Choosing a Linux Distribution](http://www.rackspace.com/knowledge_center/article/choosing-a-linux-distribution)

* [First 5 Minutes on a Server](http://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers)

<!-- * Digital Ocean has a detailed 
  [walkthrough for setting up Python web applications on Ubuntu](https://www.digitalocean.com/community/articles/how-to-set-up-ubuntu-cloud-servers-for-python-web-applications). -->
* Digital Oceanの[walkthrough for setting up Python web applications on Ubuntu](https://www.digitalocean.com/community/articles/how-to-set-up-ubuntu-cloud-servers-for-python-web-applications).


<!-- ## Operating systems learning checklist -->
## オペレーティングシステムを学ぶためのチェックリスト

<i class="fa fa-check-square-o"></i>
<!-- Choose either a Debian-based Linux distribution such as Ubuntu or a 
Fedora-based distribution like CentOS. -->
UbuntuのようなDebianベースか、CentOSのようなFedoraベースのLinuxディストリビューションのいずれかを選択します。

<i class="fa fa-check-square-o"></i>
<!-- Harden the security through a few basic steps. Install basic security 
packages such as [fail2ban](http://www.fail2ban.org/wiki/index.php/Main_Page) 
or its equivalent. Create a new user account with sudo privileges and disable
root logins. Disable password-only logins and use a public-private keypair 
instead. Read more about hardening systems in the resources listed below. -->
基本的なセキュリティを固めましょう。[fail2ban](http://www.fail2ban.org/wiki/index.php/Main_Page)や、それに類似する基本セキュリティパッケージをインストールします。sudo権限を持つ新しいユーザを作成し、ルートでのログインは禁止します。パスワードでのログインを禁止し、公開鍵・非公開鍵の鍵交換方式によるログインを設定します。システムのセキュリティに関しての詳細は以下も読んでください。

<i class="fa fa-check-square-o"></i>
<!-- Install Python-specific packages to prepare the environment for running a
Python application. Which packages you'll need to install depends on the 
distribution you've selected. -->
Pythonアプリケーションを動作させるために必要な環境を用意します。これは選択したディストリビューションによって必要なパッケージは異なります。

<i class="fa fa-check-square-o"></i>
<!-- Read up on [web servers](/web-servers.html) as installing one will be the 
next step in the deployment process. -->
[Webサーバ](./web-servers.html)の章を読み、インストールを行ったら開発プロセスの次のステップに進みます。

<!-- ### What topic do you need to learn to keep going? -->
### 続いて何を学びますか？
