# PHP

## 対象読者

* [イーツー・インフォ](https://www.e2info.co.jp/)でPHP言語を利用して開発をおこなうエンジニア
* スクラッチ開発プロジェクトの担当者

## 概要

PHPのプロジェクトの開発プロセスや技術などの情報を記載します。

### 開発フロー

原則として[GitHub Flow](https://gist.github.com/Gab-km/3705015)を採用しています。

第三者へのプルリクエストによるレビュー依頼は推奨していますが、実施は任意です。
複数クライアントからの受託開発を進めるにあたり、前提条件がプロジェクトごとに異なるため、QCDのうちQが必ずしも優先とはならないためです。

### PHPバージョン

新規開発においては、PHP7.1以上を利用します。
過去のプロジェクトや保守継続中のクライアントでは、PHP5系を利用しているプロジェクトも多数存在しています。

### 利用ツール

以下のツールを利用しています

* 必須
    * Backlog
        * git（ソースコード管理）
        * 課題管理
    * Chatwork（コミュニケーション）
    * PhpStorm
* 任意
    * 上記以外のツールの導入は任意とする（例：Slack/Google ハングアウト/Skype/Sourcetree）
    
### 利用技術

#### 一覧

主に利用するフレームワークやミドルウェアの情報を記載します。

* ウェブアプリケーションフレームワーク
    * [Laravel](https://laravel.com/)
        * 一択
* フロントエンド
    * オリジナルデザイン
    * [Laravel-admin](http://laravel-admin.org/docs/)
    * [AdminLTE2](https://adminlte.io/themes/AdminLTE/)
    * [jQuery](https://jquery.com/)
* データベース
    * [MySQL](https://www.mysql.com/)
    * [MariaDB](https://mariadb.org/)
* インフラ
    * 開発環境
        * [XAMPP](https://www.apachefriends.org/)
        * [Docker](https://www.docker.com/)
        * [Vagrant](https://www.vagrantup.com/)
    * 本番環境
        * [AWS](https://aws.amazon.com/)
        * [さくらのクラウド](https://cloud.sakura.ad.jp/)
        * （その他必要に応じて選定）
