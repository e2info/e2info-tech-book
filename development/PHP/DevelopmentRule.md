# システム開発の考え方

## 対象読者

* [イーツー・インフォ](https://www.e2info.co.jp/)でPHP言語およびLaravelフレームワークを利用して開発をおこなうエンジニア

## 概要

* システムを開発する上での姿勢、考え方を記載します
* コーディングについては[PHP/コーディングの方針](development/PHP/CodingRule.md) を参照

## なんのために策定するか

* システム開発において、最低限遵守したい箇所は独自のルールで運用しないようにする

## 前提

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

### Gitへのコミット／PUSHは早ければ早いほどよい（MUST）

一般的に言われているように、Gitへのコミット／PUSHは早ければ早いほどよいです。

以下の前提を守った上で細かくリポジトリにPUSHしてください
* テストケースがエラーにならないこと
* システム全体がエラーにならないこと
    * 一部の機能が動作しない状態での開発ブランチへのPUSHはOKです

理由

* PC故障の際にリカバリできない
* 担当者不在のときのロスが大きい
* 後になればなるほどマージのコストが増大する

---
    
![イーツー・インフォロゴ](https://raw.githubusercontent.com/e2info/e2info-warehouse/master/images/logo/logo100x100_transparent.png)

