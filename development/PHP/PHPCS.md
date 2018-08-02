# PHP_CodeSniffer(PHPCS)

## 対象読者

* [イーツー・インフォ](https://www.e2info.co.jp/)でPHP言語を利用して開発をおこなうエンジニア

## 概要

[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) は、PHPプログラムがコーディング基準に沿って正しくコーディングされているかチェックをおこなうツールです。


## なんのために実施するか

* コード品質の統一
* コードレビューで低レベルな指摘を避け、本来レビューすべき箇所に注力できるようにする

## Laravelプロジェクトへの導入

### インストール

composerでインストールします。

composer.jsonのrequire-devに以下の依存関係を記入した後、composer updateを実行します。

~~~
"require-dev": {
    "squizlabs/php_codesniffer": "*"
},
~~~

~~~
# composer update
~~~

vendor/bin配下にphpcs, phpcbfがインストールされます。

![laravel/vendor](https://raw.githubusercontent.com/e2info/e2info-tech-book/master/images/phpcs_phpcbf.png)

phpcs設定ファイルを任意の場所に設置します。

ここでは、/ci/phpcs.xml とします。

~~~
<?xml version="1.0"?>
<ruleset name="Custom Standard">
    <rule ref="PSR2">
        <!-- "PSR2" の中で除外するルール -->
        <exclude name="Generic.Files.LineLength"/>
    </rule>
    <!-- 追加するルール -->
    <!-- 除外するファイル・ディレクトリ -->
</ruleset>
~~~

### 実行

プロジェクトルート配下で以下のコマンドを実行します。

#### ソースコードのチェック

~~~
 .\vendor\bin\phpcs  --standard=../ci/phpcs.xml app
~~~

#### ソースコードの自動整形

~~~
 .\vendor\bin\phpcbf  --standard=../ci/phpcs.xml app
~~~

---
    
![イーツー・インフォロゴ](https://raw.githubusercontent.com/e2info/e2info-warehouse/master/images/logo/logo100x100_transparent.png)

