# jdk8

# Java8の日時APIはとりあえずこれだけ覚えとけ

Javaで日付/時間を扱うには従来はDate/Calendar/DateFormat等のクラスを使っていたが(以下、旧API)、Java8からはjava.timeパッケージに新しくAPIが追加された(以下、新API)。

しかし新APIはパッケージ数が5、クラス数は69もあり最初はどれをどう使うのか戸惑ってしまう。

そこで最低限これだけ覚えておけば旧APIと同じ事ができるという程度の情報をまとめてみた。

# 新APIの特徴

- 旧APIとは全く別のAPI。
- データを格納するクラスは、日時/日付のみ/時間のみなど保持する要素やタイムゾーンの有無などで、複数のクラスから選べるようになった。
- データ保持と日付操作(年/月/日フィールドの取得/変更など)が1クラスで出来るようになった。
- (旧APIではデータ保持はDateクラス、日付操作はCalendarクラスと分かれていた)
- 日時クラスはImmutableなオブジェクトになった。既存インスタンスの値を変更する際は新しくインスタンスを作成する事になる。
- 旧APIで月の値は0-11だったが、新APIでは1-12になった。