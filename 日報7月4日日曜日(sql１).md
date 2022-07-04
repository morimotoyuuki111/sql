# 本日やったこと
- データベース 
- データベースの仕組み
- クエリ
- SELECT
- FROM
- 複数カラム
- WHERE
- データ型
- 比較演算子
- LIKE演算子
- ワイルドカード
- NOT演算子
- NULL
- AND演算子
- OR演算子
- 昇順と降順
- ORDER BY
- LIMIT
- ORDER BYとLIMITの組み合わせ

- # 詳細

# データベース
```go
データを入れておく箱
データのまとまり
整理されたデータのまとまり
```
<a href="https://codezine.jp/article/detail/13504">データベース 参考サイト</a><br>
<a href="https://wa3.i-3-i.info/word133.html">データベース 参考サイト</a><br>

# データベースの仕組み
```go
表のことを「テーブル」と呼びます。
また、縦の列のことを「カラム」、横の行のことを「レコード」と呼びます。
データベースでは、必要に応じて複数のテーブルを作成することが可能です。
```
<a href="https://wa3.i-3-i.info/word1264.html">テーブルについてはこちら</a><br>
<a href="https://codezine.jp/article/detail/3685">詳しくは参考サイト</a><br>
<a href="https://wa3.i-3-i.info/word1174.html">カラム</a><br>
<a href="https://wa3.i-3-i.info/word1265.html">レコード</a><br>
<a href="https://wa3.i-3-i.info/word1264.html">テーブル</a><br>

# クエリ
```go
データを取得してください」といったようにデータベースに送る命令（クエリ）が必要
SQL(エスキューエル)とはクエリを書くための言語
データベースに対する命令文
検索エンジンに入力する検索キーワード
```
<a href="https://wa3.i-3-i.info/word11290.html">クエリ</a><br>

- SELECT
```go
データベースから、データを取得するためには「SELECT」を用います。
このSELECTを用いて、「どのカラムのデータを取得するか」を選びます。
データベースさんに対する「これ、探してこい」な命令文
```
```go
SELECT name //name カラム
```
<a href="https://wa3.i-3-i.info/word15083.html">select文</a><br>

- FROM
```go
データベースには複数のテーブルが存在する場合があります。
FROM」を用いて、SELECTで選んだカラムが「どのテーブルのカラムか」を指定する必要があります。
```
```go
SELECT name //②どのカラムのデータを?
FROM purchases //①どのデータを?
```
```go
SELECT name 
FROM purchases; //ここまでがクエリ ;（セミコロン必須）
```

- 複数カラムからデータを取得する
```go
複数のカラムからデータを取得する場合は、図のようにカラム名をコンマ（ , ）で区切ります。
```
```go
SELECT name,price //SELECT　①取得します　②name,priceどのカラムデータを？
```

全カラムのデータを取得する場合は「＊」の記号を用います。
```go
SELECT * //全てのカラムを選択可能
FROM purchases;
```
# WHERE
```go
特定のデータを取得するためには、「どこの」という意味を持つ「WHERE」を用います。
SELECT」と「FROM」で「どのテーブルのどのカラムのデータを取得するか」までは決まっていますので、
「WHERE」が意味するのは、「どこのレコード（横の行）を取得するか。

どこのレコード（横の行）のデータを取得するか」を指定するためには、「＝」を用いて、
「〇〇カラムが〇〇であるレコード」といった意味になるように条件を指定します。
```
```go
WHERE category=〇〇 //categoryが〇〇であるレコードを
```

# データ型
```go
データベースに保存されているデータには、「データ型」と呼ばれるルールがあります。
「データ型」とは、テキストデータや数値データ、さらには日付データと
いったように「データの種類」を示すものです。

文字列型とか数値型とかin型とかString型とかのこと
```
<a href="https://wa3.i-3-i.info/word1173.html">データ型</a><br>

- 数値データ型
```go
「数値データ」はクォーテーション『””』で囲んではいけないため、注意
```
```go
SELECT *
FROM purchases
WHERE price = 1000;
```

- 日付データ型
```go
日付データはダブルクォーテーション『””』またはシングルクォーテーション『’』で囲む必要
```
```go
SELECT *
FROM purchases
WHERE purchasesd_at ="2017-07-01";
```

# 比較演算子
```go
WHEREの条件では「＝」の他にも比較演算子と呼ばれる
```
<a href="https://tech.pjin.jp/blog/2020/11/30/%E3%80%90sql%E5%85%A5%E9%96%80%E3%80%91%E6%AF%94%E8%BC%83%E6%BC%94%E7%AE%97%E5%AD%90%E3%81%AB%E3%82%88%E3%82%8B%E6%9D%A1%E4%BB%B6%E6%8C%87%E5%AE%9A/">比較演算子</a><br>
