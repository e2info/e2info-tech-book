# コーディングの方針

## 対象読者

* [イーツー・インフォ](https://www.e2info.co.jp/)でPHP言語およびLaravelフレームワークを利用して開発をおこなうエンジニア

## 概要

コーディングを行う上での指針、ルール、留意する点を記載します

## なんのために策定するか

* 会社としてコード基準を統一することでコード品質をあげる
* 迷ったときの判断材料とする

## 前提

### 考え方について（トレンドや状況に合わせて柔軟に）

基準は時代や背景・前提条件によってかわり、考え方も複数あります。
記載してある内容を守れば良いというわけではなく、常に考えながら設計・実装してください。

たとえば、2008年に発売された書籍Clean Codeでは、[FluentInterface](https://www.martinfowler.com/bliki/FluentInterface.html)について以下のような記載がありますが、

> こうした呼び出しチェインは、一般には、あぶなっかしいやり方で、避けるべきと考えられています。

最近では広く利用されています。

### 要請の程度について

要請の程度については、[RFC 2119:RFC において要請の程度を示すために用いるキーワード ](https://www.ipa.go.jp/security/rfc/RFC2119JA.html)に従います。

* 「しなければならない（ MUST ）」
* 「してはならない（ MUST NOT ）」
* 「要求されている（ REQUIRED ）」
* 「することになる（ SHALL ）」
* 「することはない（ SHALL NOT ）」
* 「する必要がある（ SHOULD ）」
* 「しないほうがよい（ SHOULD NOT ）」
* 「推奨される（ RECOMMENDED ）」
* 「してもよい（ MAY ）」
* 「選択できる（ OPTIONAL ）」

## 内容

### 基本的な考え方

* 「どちらでもよい」場合、より良い方を選択します。より良いの基準は状況により異なりますが、大抵の場合、シンプルな方です。
* 「将来こういうことがおきたときのために、こうしておいたほうが良い。このほうが汎用的。」という判断はしない。 多くの場合、それは必要とならず、ただ複雑さが増すだけになります。(YAGNIの法則)

### ベースとする規約

* PSR-1/2に準拠する (MUST)
    * 変数名はlowerCamelCaseとする
    * 補足：Laravel以外のフレームワークを利用する必要がある場合、当資料の基準より各フレームワークの基準を優先します。
    
### 注意すること

#### スカラー型宣言

* 「しなければならない（ MUST ）」

PHP7より、スカラー型宣言が利用できるようになりました。
http://php.net/manual/ja/migration70.new-features.php

型を厳密に判断できるようになるため、積極的に利用して下さい。

~~~
<?php
declare(strict_types=1);
~~~

#### 型の宣言

* 「しなければならない（ MUST ）」

PHP7より、いままで可能であった引数の型宣言にくわえて戻り値の型宣言もできるようになりました。
http://php.net/manual/ja/migration70.new-features.php

型を厳密に判断できるようになるため、積極的に利用して下さい。

~~~
function arraysSum(array ...$arrays): array
{
    // logic
}
~~~

※ [PHPマニュアル／新機能](http://php.net/manual/ja/migration70.new-features.php)より引用


#### 不要なコメントは削除する。

* 「しなければならない（ MUST ）」

実装途中などの理由により残す必要がある場合、必ずTODOコメントを記載してまとめて検索できるようにします。

例：以下の例では最終行がコメントになっていますが、どのような意図でコメントになっているかわかりません。

~~~
if ($this->temp_file[$cnt] != '') {
    $objImage->deleteImage($this->temp_file[$cnt], $this->temp_dir);
}
$this->temp_file[$cnt] = '';
// $this->save_file[$cnt] = '';
~~~


---
    
![イーツー・インフォロゴ](https://raw.githubusercontent.com/e2info/e2info-warehouse/master/images/logo/logo100x100_transparent.png)

