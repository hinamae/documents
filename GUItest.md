# 試験自動化最強システム構成図(?)

クラウドでは再現が難しい他社の(?)エミュレータを使用しているため、CI/CDを実践するのは割と難しい(?)
逆にテストに必要になるデータだけを補うとか、その小規模版エミュレータみたいなものがあれば、CI/CDは可能？

# スマホ試験自動化
# BDD
behavier driven development
ふるまい駆動開発

[https://www.atmarkit.co.jp/ait/articles/1403/25/news033_2.html](https://www.atmarkit.co.jp/ait/articles/1403/25/news033_2.html)

### JGiven

[https://qiita.com/hatai/items/7868996e3eb5fa55f11a](https://qiita.com/hatai/items/7868996e3eb5fa55f11a)

Junitと互換性があるBDDフレームワーク。

[http://blueskyarea.hatenablog.com/entry/2018/11/27/234144](http://blueskyarea.hatenablog.com/entry/2018/11/27/234144)


### specflow
テストケースを自然言語で記述しておき、それに対応するテストコードを先に書いてしまう。
そのテストをクリアするような実装をする。

[https://corgi-lab.com/windows/specflow-bdd/](https://corgi-lab.com/windows/specflow-bdd/)



## 

# TDD
テスト駆動開発

## Junit

# CI/CD
continous integration & continuous delivery

＝ソフトウェアの変更を常にテストして、自動で本番環境にリリース可能な状態にしておくドフトウェアの開発手法。(CI/CDに伴う自動試験システムの構成はオンプレミスかクラウドかの違いこそあれ、。)


## 有名なもの
- オンプレミス版
     - jenkins
- クラウド版
    - Travis CI
    - Circle CI

## jenkins

gitと連携させることで、jenkinsのジョブに成功したマージリクエストのみ承認できるようにするなど可能になる。

試験の際には、異なる環境で実行したいという要望が生まれがち。
その時は、Dockerと連携させて、より容易に異なる環境でのビルドとテストを繰り返すことができるようになる。

##  Travis CI

git hub連携させる試験自動化ツール。
Tracvis CI上のサーバでビルド・実行される。

[https://knowledge.sakura.ad.jp/3754/](https://knowledge.sakura.ad.jp/3754/)

公開しているリポジトリと連携させるなら無料。

## Circle CI

git hub,bit bucketと連携させる試験自動化ツール。
1コンテナまでなら無料。privateリポジトリでも。


[https://qiita.com/noboru_i/items/7d300eb63ae667bf8dc2](https://qiita.com/noboru_i/items/7d300eb63ae667bf8dc2)
