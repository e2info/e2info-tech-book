# E2info Tech Book

[株式会社イーツー・インフォ](https://www.e2info.co.jp/)で用いている技術を公開するためのドキュメントです。

## 対象読者

* イーツー・インフォのエンジニア
* イーツー・インフォにこれから入社するエンジニア

## 前提条件

イーツー・インフォは受託開発をメインでやっている会社です。そのため、自社サービス開発・運用の会社とは、技術選定条件や環境が異なる可能性があります。
当資料に記載している技術は現時点のもので、常にアップデートされます。

### 技術選定の指針

* 技術に対して保守的にならない。現状この業界では、進歩しないことは退化することと同意であると考えています。
* [デジタルエコシステム](https://en.wikipedia.org/wiki/Digital_ecosystem)の推進。自社に設備を導入するオンプレミスによるシステム運用は、主に人的コストが大きな負担となるため、出来る限り避けるようにしています。

### 目次

* プロジェクト管理
    * 必ず利用するもの
        * バックログ（タスク管理、git）
        * G Suite（メール、カレンダー、ドライブ）
        * Chatwork（社内外のコミュニケーション）
    * 任意
        * 各種チャットツール（Slack, Googleハングアウト、skype, Tencent QQ）
        * GitHub/Bitbucket（SCM）
        * Jenkins/CircleCI（CI）
* システム開発
    * [システム開発の知識](development/Knowledge.md) - 必ず知っておく必要がある知識について
    * メインで利用している開発言語はPHPとJavaです。それぞれの言語により開発プロセスやデプロイ方法などが異なります。
        * PHPのプロジェクト
            * [PHP](development/PHP/PHP.md)
            * [PHP/システム開発の考え方](development/PHP/DevelopmentRule.md) 
            * [PHP/コーディングの方針](development/PHP/CodingRule.md) 
            * [PHP/PHP_CodeSniffer(PHPCS)](development/PHP/PHPCS.md) 
        * Javaのプロジェクト
            * @TODO
* 運用・保守
    * @TODO システム死活監視


![イーツー・インフォロゴ](https://raw.githubusercontent.com/e2info/e2info-warehouse/master/images/logo/logo100x100_transparent.png)
