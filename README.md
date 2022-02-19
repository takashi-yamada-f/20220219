# MySQL最新版のMySQL8と最近リリースされたAmazon Aurora3について

## 【０】TOPIC
* Amazon Aurora MySQL 3 with MySQL 8.0 compatibility is now generally available
<br>by Aditya Samant and Vlad Vlasceanu | on 18 NOV 2021
<br>https://aws.amazon.com/jp/blogs/database/amazon-aurora-mysql-3-with-mysql-8-0-compatibility-is-now-generally-available/

## 【１】MySQL8.0

* MySQLの歴史が面白い - Qiita
<br>https://qiita.com/nom_bom/items/75d409b303f4814143c8

* MySQL :: MySQL 8.0: MySQL 5.7よりも最大2倍高速
<br>https://www.mysql.com/jp/products/enterprise/database/

* MySQL8.0になって変わったこと - Qiita
<br>https://qiita.com/kota-miyasaka/items/65a6a1b7bed24771c01d
<br>※簡単に言うとこんな感じです。

* MySQL :: MySQL 8.0 リファレンスマニュアル :: 13.2.15 WITH (共通テーブル式)
<br>https://dev.mysql.com/doc/refman/8.0/ja/with.html

* MySQL :: MySQL 8.0 リファレンスマニュアル :: 12.21.1 Window 関数の説明
<br>https://dev.mysql.com/doc/refman/8.0/ja/window-function-descriptions.html

* 【SQL基礎】ウィンドウ関数とは | TECH PROjin
<br>https://tech.pjin.jp/2021/07/31/%E3%80%90sql%E5%85%A5%E9%96%80%E3%80%91%E3%82%A6%E3%82%A3%E3%83%B3%E3%83%89%E3%82%A6%E9%96%A2%E6%95%B0%E3%81%A8%E3%81%AF/
<br>※もう少し分かりやすく

* MySQL 8.0 : クエリーキャッシュのサポート終了 | Yakst
<br>https://yakst.com/ja/posts/4612
<br>※クエリーキャッシュを廃止して大丈夫？という方向けの記事です。

* 漢(オトコ)のコンピュータ道:　MySQL 8.0登場！立ち止まることを知らない進化はこれからも続く。
http://nippondanji.blogspot.com/2018/05/mysql-80.html
<br>※もう少し詳しく。
<br>※文字コードの扱いが変わっているのでカナソートしていると順番が拗音、長音、濁音の優先順序が変わります。
<br>※レプリケーションが変更されています。

## 【２】AWS Aurora MySQL

* Amazon Aurora の特徴: MySQL 互換エディション
<br>https://aws.amazon.com/jp/rds/aurora/mysql-features/

* Amazon RDSとAuroraの違いをまとめてみた - サーバーワークスエンジニアブログ
<br>https://blog.serverworks.co.jp/rds-aurora-difference

* Aurora/RDS MySQL Latest Update　2022/02/08（Amazon Web Services Japan 公式）
<br>https://www.youtube.com/watch?v=GDnugugdemk

```
3:40 Amazon Aurora
4:14 Introducing Aurora MySQL version3
※以前より要望が多かったMySQL8.0互換。
5:33 Current Aurora MySQL version options
8:08 Instant DDL
※「ALGORITHM=INSTANT」。従来の「COPY」や「INPLACE」と異なり、メタデータの更新だけ行うことで高速かつ負荷をかけずにカラムの追加などが行えるようになりました。
11:24 Common table expressions
12:19 Window functions
13:00 Role-based access control
16:30 Binary log enhancements
21:53 And more
```

* Amazon Aurora MySQL 3 (MySQL 8.0 互換) がリリースされました。 | DevelopersIO
<br>https://dev.classmethod.jp/articles/amazon-aurora-mysql-3-ga/
<br>※こんな風に選択できるようになりました。

## 【３】MySQL8、Aws Aurora MySQL ver3 への移行

* MySQL 8.0 への移行が完了しました ～さようなら全ての MySQL 5.7～ - Cybozu Inside Out | サイボウズエンジニアのブログ
<br>https://blog.cybozu.io/entry/2021/05/24/175000

* MySQL :: MySQL 8.0 リファレンスマニュアル :: 5.1.11 サーバー SQL モード
<br>https://dev.mysql.com/doc/refman/8.0/ja/sql-mode.html#sql-mode-setting
<br>※sql_modeの設定が増えたことで、sql文が厳密にチェックされるようになりました。（変更は非推奨）

* MySQL :: MySQL 8.0 リファレンスマニュアル :: 9.3 キーワードと予約語
<br>https://dev.mysql.com/doc/refman/8.0/ja/keywords.html
<br>※予約語は「`」で囲んで使ってください。設計時にも注意です。

以上です。
