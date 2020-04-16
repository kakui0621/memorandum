SQL入門編の忘備録

paizaでSQLを復習したので忘備録を書いてみる。

SQLの使いかたを思い出したし、これを見ると思い出せるけど、
別の言語と組み合わせてクエリー文書くとかしないと忘れちゃうだろうね、これは。


◆SQL入門編1: SQLの基本文法を学ぶ (全7回)



02:データベースを準備しよう 
データベースとSQLを学習するため、MySQLとphpMyAdminを使って、簡単なデータベースを作成していきます。
そして、phpMyAdminでSQLを実行する基本的な操作手順を学んでいきます。

 簡単に手に入るLAMP環境
・就活パック LAMP環境を構築しよう - AWS編
https://paiza.jp/works/aws/primer

・XAMPP：ローカルPCにインストールできるLAMP環境
https://www.apachefriends.org/jp/index.html

XAMPPに収録されているMariaDBは、MySQLプロジェクトから分岐して開発されているデータベースです。

 phpMyAdminの参考資料
・phpMyAdminの使い方
http://www.dbonline.jp/phpmyadmin/


 サンプルデータベースを作成するSQL文

CREATE TABLE players (
  id INT NOT NULL PRIMARY KEY,
  name VARCHAR(32),
  level INT,
  job_id INT
);

CREATE TABLE jobs (
  id INT NOT NULL PRIMARY KEY,
  job_name VARCHAR(10),
  vitality INT,
  strength INT,
  agility INT,
  intelligence INT,
  luck INT
);

INSERT
  INTO players(id,name,level,job_id)
  VALUES
    (1,"パイザ",12,6),
    (2,"ケン",7,2),
    (3,"リン",1,1),
    (4,"ユウ",3,3),
    (5,"クレア",10,4),
    (6,"ショウ",5,2),
    (7,"さくら",7,1),
    (8,"ジャック",5,4),
    (9,"ロック",12,6),
    (10,"じゅん",1,NULL);

INSERT
  INTO jobs(id, job_name, vitality, strength, agility, intelligence, luck)
  VALUES
    (1,"戦士",8,8,4,4,3),
    (2,"盗賊",3,3,8,5,7),
    (3,"狩人",5,5,7,5,4),
    (4,"魔法使い",3,2,6,8,6),
    (5,"僧侶",5,5,3,7,5),
    (6,"勇者",10,10,10,10,10);



＃03:テーブルの中身を見てみよう 
初歩的なSQL文を作成して、サンプルデータベースの中身を見ていきます。
データベースに対してSQLを実行するため、先ほどのチャプターで作成したpaizaデータベースの「players」テーブルを使います。

 今回取り上げたSQL文の例
 WHERE句の条件指定
 SQLの参考資料
 データベース/SQLのコーディング規約
プログラミング学習 > DB/SQL > DB/SQL入門編 > SQL


今回取り上げたSQL文の例

-- 全てのデータを取り出す
SELECT * FROM players;

-- 一部のカラムだけ取得する
SELECT name, level FROM players;

-- 一部の行だけ取得する
SELECT * FROM players WHERE level >= 7;

-- 複数の条件を組み合わせる
SELECT * FROM players WHERE level >= 7 AND job_id <> 6;

--条件指定とカラム選択を組み合わせる
SELECT name, level FROM players WHERE level >= 7;


 WHERE句の条件指定
構文	意味	例
a = b	a と b が等しい	level = 10
a < b	a が b よりも小さい	level < 15
a > b	a が b よりも大きい	level > 7
a <= b	a が b 以下である	level >= 15
a >= b	a が b 以上である	level >= 7
a <> b	a と b が等しくない	level <> 1


条件をつなげるキーワード	意味
AND	両方の条件が成立した場合
OR	どちらか一方の条件が成立した場合



＃04:いろいろな情報を取り出そう 
SQLのSELECT命令を使って、サンプルデータベースから色々な情報を取り出してみます。
今回は、データの件数や、並び替え、集計といった機能について学習しましょう。

 今回取り上げたSQL文の例

-- データ件数を表示する
SELECT COUNT(*) FROM players;


--条件に合ったデータの件数を表示する
SELECT COUNT(*) FROM players WHERE job_id = 6;


-- データを並び替えて取得する
SELECT * FROM players ORDER BY level;


-- データを並び替えて取得する 逆順
SELECT * FROM players ORDER BY level DESC;


--上位3件だけ表示す
SELECT * FROM players ORDER BY level DESC LIMIT 3;


-- 職業ごとに人数を集計する
SELECT job_id, COUNT(*) FROM players GROUP BY job_id;



＃05:データを追加・更新・削除しよう 
データベースにデータを追加・更新・削除する方法を学んでいきます。
たとえば、この機能を使うことで、RPGのプレイヤーに新しいメンバーを追加したり、名前を変更したり、削除したりできます。

 今回取り上げたSQL文の例

-- データを追加する
INSERT INTO players(id,name,level,job_id) VALUES(11, "霧島1号", 1, 1);


-- データを追加して表示する
INSERT INTO players(id,name,level,job_id) VALUES(12, "霧島2号", 1, 1);
SELECT * FROM players;


-- 一度に複数のデータを追加する
INSERT INTO players(id,name,level,job_id)
VALUES
(13, "霧島3号", 1, 1),
(14, "霧島4号", 1, 1)
;
SELECT * FROM players;


-- データを更新する
UPDATE players SET level = 10 WHERE id = 11;
SELECT * FROM players;


-- データを更新する。1増加
UPDATE players SET level = level + 1 WHERE id = 12;
SELECT * FROM players;


-- データを削除する
DELETE FROM players WHERE id = 13;
SELECT * FROM players;


-- データを削除する
DELETE FROM players WHERE id >= 11;
SELECT * FROM players;

＃06:2つのテーブルを結合しよう 
データベースで、複数のテーブルを結合して扱う方法を学んでいきます。
リレーショナルデータベースでは、重複したデータのテーブルを分割しておいて、
必要に応じて、仮想的な1つの表として扱うことができます。

 テーブルの関連付けとは
 今回取り上げたSQL文の例

-- テーブルを結合して表示する（内部結合）
SELECT * FROM players INNER JOIN jobs ON jobs.id = players.job_id;


-- テーブルを結合して表示する(左結合)
SELECT * FROM players LEFT JOIN jobs ON jobs.id = players.job_id;


-- テーブルを結合して表示する(右結合)
SELECT * FROM players RIGHT JOIN jobs ON jobs.id = players.job_id;




＃07:結合したテーブルを操作しよう 
結合したテーブルでも、データベースに対する基本操作を実行できます。
ここでは、特定のカラムだけ表示したり、条件に合った行だけ表示したりというように、
結合したテーブルで、いくつかの基本操作を試してみましょう。

 今回取り上げたSQL文の例

-- 結合したテーブルを操作する
SELECT * FROM players INNER JOIN jobs ON jobs.id = players.job_id;


-- 結合したテーブルで、指定カラムだけ表示
SELECT name, level, vitality FROM players INNER JOIN jobs ON jobs.id = players.job_id;


-- 結合したテーブルで、条件に合った行だけ表示
SELECT name, level, strength FROM players INNER JOIN jobs ON jobs.id = players.job_id WHERE strength >= 5;


-- 職業ごとに人数を集計する
SELECT job_id, job_name, COUNT(*) FROM players INNER JOIN jobs ON jobs.id = players.job_id GROUP BY job_id;



◆SQL入門編2: SQLを仕事に使おう (全11回)

＃01:仕事にもSQLを使おう 
このレッスンでは、データベース操作言語のSQLの基本的なテクニックを学習します。
今回は、エンジニアだけでなく、Webサービスにたずさわる人たちにも役立つように、ログ解析を題材にしていきます。

まず最初は、SQLの実行方法と間違いやすいポイントを理解しましょう。

 参考になるWebサイト
3分動画と練習問題で学ぶプログラミング学習サービス「paiza動画ラーニング」

AWS入門編1:Webサーバを構築しよう
https://paiza.jp/works/aws/primer/aws1

AWS入門編2:LAMP環境を構築しよう
https://paiza.jp/works/aws/primer/aws2

SQL入門編1: SQLの基本文法を学ぶ
https://paiza.jp/works/sql/primer/beginner-sql1


＃02:SQLの書き方のポイント 
ここでは、SQLの書き方のポイントについて学習します。
そこで、SQLの読みやすいコードの書き方や、間違いやすいポイントについて取り上げます。

 SQLで間違いやすいポイント
- SELECTのカンマ忘れ、カンマ多すぎ
- テーブル連結時のテーブル名不足
- WHEREでAND忘れ


演習問題：
右側のコードエリアのSQLは、サンプルデータベースのeventlogテーブルを10行だけ表示します。
ここに、usersテーブルをINNER JOINで連結して、表示させてください。
なお、eventlogテーブルとusersテーブルは、userIDで連結します。

回答：
-- logIDが10以下のイベントログを表示
SELECT * FROM eventlog
	INNER JOIN users ON users.userID = eventlog.userID
WHERE logID <= 10;


＃03:ログ解析してみよう 
ここでは、SQLを使ったログ解析にチャレンジしてみたいと思います。題材として、データベースに格納された、オンラインRPGの行動ログを取り上げて、日次と月次のアクセス数を調べます。

 日次アクセス数の基本形

-- 日次のアクセス数を求める
SELECT DATE(startTime), COUNT(logID)
FROM eventlog
GROUP BY DATE(startTime);

特定の範囲の日次アクセス数の基本形

-- 日次のアクセス数を求める
SELECT DATE(startTime), COUNT(logID)
FROM eventlog
WHERE DATE(startTime) BETWEEN "2015-04-01" AND "2015-04-30"
GROUP BY DATE(startTime);

月次アクセス数の基本形

-- 月次のアクセス数を求める
SELECT DATE_FORMAT(startTime, '%Y-%m'), COUNT(logID)
FROM eventlog
GROUP BY DATE_FORMAT(startTime, '%Y-%m');


問題：
右側のコードエリアのSQLは、サンプルデータベースのeventlogテーブルで、日時とlogIDを表示します。
COUNT関数とGROUP BYを追加して、日次のアクセス数を表示させてください。
-- 日次のアクセス数を求める

SELECT DATE(startTime), logID
FROM eventlog;
↓
SELECT DATE(startTime), COUNT(logID)
FROM eventlog
GROUP BY DATE(startTime);



＃04:アクティブユーザーを調べよう 
ここでは、SQLを使って、オンラインRPGに登録したままのアクティブユーザー数を求めます。
また、このようなログ解析に役立つ、いくつかのテクニックも紹介します。

 カラム名を別名で表示する (AS)

SELECT userID AS "アクティブユーザー"
FROM users;




＃05:データを集計しよう 
ここでは、SQLを使って、獲得経験値の合計や平均を集計する方法を学習します。
さらに、ユーザーのプレイ開始日とプレイ最終日を調べてみましょう。

 SELECT文の処理順
- 1. FROM 対象テーブルからデータを取り出す
- 2. WHERE 条件に一致するレコードを絞り込み
- 3. GROUP BY グループ化
- 4. HAVING 集計結果から絞り込み
- 5. SELECT 指定したカラムだけを表示

重複した行を省いて表示する (DISTINCT)

SELECT DISTINCT userID AS "アクティブユーザー"
FROM users;
 空のカラムの行を表示する (IS NULL)

SELECT userID AS "アクティブユーザー"
FROM users
WHERE deleted_at IS NULL;



＃06:ユーザーの年齢を計算をしよう 
ここでは、ユーザーのプレイ期間を計算したり、生年月日から年齢を計算したりといった、
日付に関するデータを計算してみたいと思います。
そのために、今回はSQL上で簡単な四則演算を利用してみましょう。

・ SQLの四則演算
足し算 「30 + 10」は、「40」
引き算 「30 - 10」は、「20」
掛け算 「30 * 10」は、「300」
割り算 「30 / 10」は、「3」

カッコの中を先に計算 「10 * (2 + 3)」は、「60」
・現在の日時を求める

CURRENT_DATE()) AS 現在日時
・2つの日時の間の期間を整数で求める

TIMESTAMPDIFF(YEAR, (誕生日), (現在の日時))

＃07:テキストを検索しよう 
ここでは、オンラインRPGで、誰が、いつ、どのイベントに参加したのか
調べるSQLを作ってみたいと思います。そのために、テキスト検索について学習してみましょう。

 テキストに部分的に一致するレコードを取り出す

-- テキスト検索
SELECT
	events.event_summary
FROM
	eventlog
	INNER JOIN events ON events.eventID = eventlog.eventID
WHERE  events.event_summary LIKE '%との闘い'
＃08:サブクエリでアクティブユーザー数を求めよう 
ここでは、サブクエリを使って、日次のアクティブユーザー数を求めてみたいと思います。
サブクエリは、複数のクエリを組み合わせるSQLの機能です。
この他に、サブクエリを利用して、平均以上のユーザーを求める方法も紹介します。

 サブクエリの基本形

-- FROM句に書く場合
SELECT *
FROM (サブクエリ) AS (サブクエリ名);
＃09:グループ分けしよう 
ここでは、すでに分類されたデータを別の基準でグループ分けしてみます。
たとえば、オンラインRPGでユーザーのレベルを初級・中級・上級に分けて集計する、
都道府県を関東や関西といった地域にまとめて集計する、といった操作が可能になります。
そのために、SQLのCASE(ケース)命令を紹介します。

 CASEの基本形

-- データを分類し直す
SELECT
	userID,
	level,
	CASE
		WHEN (条件式1) THEN (出力1)
		WHEN (条件式2) THEN (出力2)
		ElSE (出力3)
	END
FROM
	users



＃10:クロス集計してみよう 
ここでは、オンラインRPGのイベントログから、クロス集計表を作ります。SQLでクロス集計を作るには、これまで学習してきた、サブクエリやCASEといった、いくつかのテクニックを組み合わせる必要があります。

 クロス集計表を作る手順
1. クロス集計の元になるデータを用意する
2. サブクエリとして読み込む
3. CASEで、特定の値だったら1にする。このとき別名を、特定の値と同じにする


CASE WHEN クラス = "初級" THEN 1 ELSE NULL END AS "初級",
CASE WHEN クラス = "中級" THEN 1 ELSE NULL END AS "中級",
CASE WHEN クラス = "上級" THEN 1 ELSE NULL END AS "上級"


4. SUM関数とGROUP BYで集計する
参考になるWebサイト
MySQLでクロス集計してみた | トーハム紀行
http://torhamzedd.blogspot.jp/2010/06/mysql.html




https://propoko.com/blog/techacademy-free