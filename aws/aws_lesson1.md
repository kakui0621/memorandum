AWSでのサーバ構築方法やコマンドや操作法の忘備録

[AWS入門編](https://paiza.jp/works/aws/primer/)


#AWS入門編1:Webサーバーを構築しよう


##01:Webサーバーを構築しよう

参考
・AWS アカウント作成の流れ
　https://aws.amazon.com/jp/register-flow/

解約方法
　1. ログイン
　2. アカウント > アカウント設定
　3. アカウント設定ページの一番下に「アカウントの解約」ボタンがある

 料金の確認方法
1. ログイン
2. アカウント > 請求とコスト管理



##02:AWSアカウントを作ろう

Linux仮想マシンの起動手順
1. コンソールにアクセス
2. EC2を選択
3. 東京リージョンを選択
4. Linuxディストリビューションを選択
5. インスタンスとして、t2.microを選択
6. キーペアを保存
7. インスタンスを作成
参考
・Linux 仮想マシンの起動
　https://aws.amazon.com/jp/getting-started/launch-a-virtual-machine/

・インスタンスタイプ - Amazon EC2
　https://aws.amazon.com/jp/ec2/instance-types/


##03:Linux仮想マシンを起動しよう
 Linux仮想マシンの起動手順
1. コンソールにアクセス
2. EC2を選択
3. 東京リージョンを選択
4. Linuxディストリビューションを選択
5. インスタンスとして、t2.microを選択
6. キーペアを保存
7. インスタンスを作成
無料期間内でも、停止・削除したインスタンスに割り当てたパブリックIPの設定を解除しておかないと
料金が発生してしまいますので、忘れずに解約しておきましょう


##04:パブリックIPアドレスを設定しよう
このチャプターでは、Linux仮想マシンのパブリックIPアドレスを設定していきます。
・ドメインを取得する
　https://aws.amazon.com/jp/getting-started/get-a-domain/


##05:リモートアクセスしよう
このチャプターでは、ローカル環境からAWSのLinux仮想マシンにリモートアクセスしてみます。
 ここで実行したコマンド

```console
pwd
ls
ls -a -l

mkdir .ssh

mv ~/Desktop/FirstKey.pem ~/.ssh
chmod 400 ~/.ssh/FirstKey.pem

ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

exit
```


##06:Webサイトを公開しよう
このチャプターでは、引き続き、SSHでLinux仮想マシンに接続して、HTTPサーバーのApacheをインストールしていきます。
 ここで実行したコマンド
パブリックIPアドレスなど、適時自分の環境に合わせて修正してください。

```console
コマンドをローカル環境で実行
ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)
ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

コマンドをLinux仮想マシンで実行
sudo yum -y update
sudo yum -y install httpd
sudo service httpd start
sudo chkconfig httpd on

ls /var/www/html
sudo vi /var/www/html/index.html
```


##07:ファイルを転送しよう
このチャプターでは、ローカル環境で作成したhtmlファイルをWebサーバーに転送していきます。


ここで実行したコマンド

```console

--コマンドをLinux仮想マシンで実行
scp -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP):/var/www/html/index.html ~/Desktop
（AWSに置いたhtmlファイルをデスクトップにダウンロード）

scp -i ~/.ssh/FirstKey.pem ~/Desktop/index.html ec2-user@(パブリックIP):~
（デスクトップに置いたhtmlファイルをAWSにアップロード）

ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

$$ ls
$$ sudo mv ~/index.html /var/www/html
$$ exit

--コマンドをローカル環境で実行
$ ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

--コマンドをLinux仮想マシンで実行
$$ sudo groupadd www
$$ sudo usermod -a -G www ec2-user
$$ exit

$$ groups

$$ sudo chown -R root:www /var/www
$$ sudo chmod 2775 /var/www
$$ find /var/www -type d -exec sudo chmod 2775 {} \;
$$ find /var/www -type f -exec sudo chmod 0664 {} \;
$$ exit

--コマンドをローカル環境で実行
$ scp -i ~/.ssh/FirstKey.pem ~/Desktop/index.html ec2-user@(パブリックIP):/var/www/html
```




SSHで権限を変更する

--------------------------------------------------------------------------------------
#AWS入門編2:LAMP環境を構築しよう





##01:LAMP環境を理解しよう

LAMP(ランプ)とは、Webアプリケーションの実行環境の組み合わせです。
Webアプリケーションの実行環境では、ふつう、OSとWebサーバー、データベース、スクリプト言語を組み合わせて利用します。
中でもLAMPは、Webサービスがはやり始めたころからある、オーソドックスな組み合わせです。OSにLinux(リナックス)、
WebサーバにApache(アパッチ)、データベースにMySQL(マイエスキューエル)、スクリプト言語にPHP(ピーエイチピー)という組み合わせを、
その頭文字をとって、LAMP(ランプ)と呼びます。

LAMP環境の構築手順
1. PHPをインストールする
2. MySQLをインストールする
3. サンプル掲示板を設置する
4. HTMLベースで改良する
5. PHPベースで改良する
6. PHPベースで改良する


##02:PHPをインストールしよう 
AWSに構築したWebサーバー上に、スクリプト言語のPHPをインストールしてみたいと思います。
PHPをインストールすると、Webページをプログラムによって表示したり、アクセスしてきたユーザーに合わせて、
内容を変化させてみます。

 PHPインストールの作業手順
1. Webサーバーの動作確認
2. SSHでログインする
3. 管理者権限に切り替える
4. サーバの時間設定(UTCからJST)
5. PHPのインストール
6. PHPの設定
7. Apacheの再起動
8. PHPの動作確認

ここで利用したコマンド
sshコマンドでログイン

```console
$ ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

(zero版)
$ ssh -i ~/.ssh/aws-and-infra-ssh-key.pem ec2-user@(パブリックIP)

管理者権限に切り替える
$$ sudo su

時刻の確認
## date

ローカルタイムの設定
## ln -sf /usr/share/zoneinfo/Japan /etc/localtime

PHPをインストール
## yum install -y php

PHP設定ファイルのバックアップ
## cp /etc/php.ini /etc/php.bak

Apacheの再起動
## service httpd restart

```

※記号の意味
コマンドをローカル環境で実行
$ (コマンド)

コマンドをLinux仮想マシンで実行
$$ (コマンド)

コマンドをLinux仮想マシンで管理者権限で実行
## (コマンド)

 SSHコマンドによる接続
・Linux インスタンスへの接続 - Amazon Elastic Compute Cloud
https://docs.aws.amazon.com/ja_jp/AWSEC2/latest/UserGuide/AccessingInstances.html

・SSH を使用した Linux インスタンスへの接続 - Amazon Elastic Compute Cloud
http://docs.aws.amazon.com/ja_jp/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html

・ネットワーク管理の基本Tips - ＠IT - SSHサーバーにログインするには？ sshコマンド
http://www.atmarkit.co.jp/ait/articles/1503/23/news004.html

・端末エミュレータ - Wikipedia
https://ja.wikipedia.org/wiki/%E7%AB%AF%E


##03:PHPの動作確認をしよう

簡単なPHPコードを作成し、動作を確認します。
設定ファイルのバックアップと復帰方法
設定ファイルを変更する場合、事前にバックアップを取っておくと安心です。
バックアップを取っておけば、もしも変更を間違えた場合も、すぐに復帰させることができます。
バックアップを取るには、次のように、ターミナルでファイルをコピーしておきます。
「cp」コマンドは、ファイルをコピーするコマンドです。

```console
# cp (元々のファイル名) (バックアップファイル名)

例えば、PHPの設定ファイルをバックアップするには、次のコマンドを実行します。

# cp /etc/php.ini /etc/php.bak

バックアップを復帰させるには、次のように、バックアップファイルを元のファイルに上書きします。

# cp (バックアップファイル名) (元々のファイル名)

例えば、PHPの設定ファイルのバックアップを復帰させるには、次のコマンドを実行します。

# cp /etc/php.bak /etc/php.ini
```

■viの基本コマンド
vi (ファイル名) 指定ファイルを読み込み、viを起動する
i テキストを編集できる状態にする
escキー コマンドを入力できる状態にする
:wq ファイルを保存して終了するコマンド
:q! ファイルを保存しないで終了するコマンド

:set number 行番号の表示
:行番号 行番号の行へ移動
■viの参考資料
・viの使い方/基本操作
　http://www.envinfo.uee.kyoto-u.ac.jp/user/susaki/command/vi.html
・viエディタの使い方
　http://net-newbie.com/linux/commands/vi.html
・今さら聞けない高性能エディタVim入門Code部
　https://blog.codecamp.jp/vim
■PHPの設定変更
「& ~E_NOTICE」を追加

error_reporting = E_ALL & ~E_DEPRECATED & ~E_NOTICE

OffからOnへ
display_errors = On
■PHPのテスト用ファイル
/var/www/html/index.phpに次のコードを入力

```php:index.php
<?php
echo "hello PHP!";
?>
54.250.134.180/index.php
```

##04:MySQLのインストール 

 MySQLインストールの作業手順
1. MySQLのインストール
2. MySQLの起動
3. MySQLの設定
4. 文字コードの設定
5. phpMyAdminのインストール
6. phpMyadminの設定
7. phpMyadminの動作確認
ここで利用したコマンド
sshコマンドでログイン

```console
$ ssh -i ~/.ssh/FirstKey.pem ec2-user@(パブリックIP)

管理者権限に切り替える
$$ sudo su

MySQLのインストール
## yum install -y mysql-server

追加プログラム(PHPのMySQLネイティブドライバ)のインストール
## yum install -y php-mysqlnd

MySQLの起動
## service mysqld start

MySQLの設定
## mysql_secure_installation

MySQLの文字コード設定のために、設定ファイルを開く
## vi /etc/my.cnf

MySQLの再起動
## service mysqld restart

※記号の意味
コマンドをローカル環境で実行
$ (コマンド)

コマンドをLinux仮想マシンで実行
$$ (コマンド)

コマンドをLinux仮想マシンで管理者権限で実行
## (コマンド)
```

MySQLの文字コード設定
character-set-server = utf8


##05:phpMyAdminのインストール
MySQLをWebブラウザから管理するツールであるphpMyAdminをインストールします。

ここで利用したコマンド

phpMyAdminのダウンロード先を追加

```console
## yum-config-manager --enable epel

phpMyAdminのインストール
## yum install -y phpmyadmin

phpMyAdminの設定(アクセス制限) のために、設定ファイルを開く
## vi /etc/httpd/conf.d/phpMyAdmin.conf

Apacheの再起動
## service httpd restart
```

※記号の意味
コマンドをローカル環境で実行
$ (コマンド)

コマンドをLinux仮想マシンで実行
$$ (コマンド)

コマンドをLinux仮想マシンで管理者権限で実行
## (コマンド)


##06:掲示板を設置しよう 
LAMP環境上に簡単なWeb掲示板を設置してみます。

 Web掲示板を設置手順
1. MySQL上にデータベースを作成
2. テーブルを作成する
3. カラムを作成する
4. bbs.phpをダウンロードする
5. bbs.phpをアップロードする
6. 動作確認

bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/6/bbs.php )
※Windows ：右クリック - 名前を付けてリンク先を保存
※Mac ：CTRL + クリック - リンクに名前を付けて保存

データベースの作成情報
データベース
DB名: lesson
照合順序: utf8_general_ci

テーブルの定義
テーブル名: bbs
カラム数: 3

カラムの定義
名前: id, データ型: INT, インデックス: PRIMARY, A_I: オン
名前: content, データ型: TEXT
名前: updated_at, データ型: DATETIME
照合順序: utf8_general_ci



##07:HTMLを改良しよう 
LAMP環境上に設置したWeb掲示板をカスタマイズしていきます。

 HTML部分の変更内容
1. 見出し１のテキストを変更
2. 見出し２のテキストを変更
3. 背景色を変更
4. Bootstrap CDNを適用

```html:index.html
<!-- bootstrap CDN -->
<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"/>
<script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
 今回のチャプターの変更が適応されたbbs.phpのダウンロード
bbs.php( https://paiza-webapp.s3.amazonaws.com/
```

##08:PHPを改良しよう 
LAMP環境上に設置したWeb掲示板を、さらにカスタマイズしていきます。

 PHP部分の変更内容
1. 行番号を追加
2. 交互に色を変える
bbs.phpのダウンロード
前チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/7/bbs.php )

本チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/8/bbs.php )


※Windows ：右クリック - 名前を付けてリンク先を保存
※Mac ：CTRL + クリック - リンクに名前を付けて保存
bbs.phpの修正箇所
行番号を追加

```php:index.php
// 取得したデータをテーブルで表示
?>
<table class="table">
<tr>
  <th>No.</th>
  <th>日時</th>
  <th>投稿内容</th>
</tr>
<?php
while ($row = $stmt -> fetch(PDO::FETCH_ASSOC)) {
  $i++;
?>
<tr>
  <td><?php echo "$i"; ?></td>
  <td><?php echo "$row[updated_at]"; ?></td>
  <td><?php echo "$row[content]"; ?></td>
</tr>
<?php
}
?>



交互に色を変える

// 取得したデータをテーブルで表示
?>
<table class="table">
  <tr>
    <th>No.</th>
    <th>日時</th>
    <th>投稿内容</th>
  </tr>
<?php
  while ($row = $stmt -> fetch(PDO::FETCH_ASSOC)) {
    $i++;
    if ($i % 2 == 1) {
?>
  <tr bgcolor="#cccccc">
<?php
  } else {
?>
 <tr>
<?php
  }
?>
    <td><?php echo "$i"; ?></td>
    <td><?php echo "$row[updated_at]"; ?></td>
    <td><?php echo "$row[content]"; ?></td>
 </tr>
<?php
  }
?>
</table>
```

ここで利用したコマンド
ファイルの転送

$ scp -i ~/.ssh/FirstKey.pem ~/Desktop/bbs.php ec2-user@(パブリックIP):/var/www/html


※記号の意味
コマンドをローカル環境で実行
$ (コマンド)


##09:DBを改良しよう - 投稿の削除 
Web掲示板を、さらにカスタマイズしていきます。

 データベース操作の修正手順
1. デバッグ用にidを表示
2. 削除ボタンを追加
3. 削除ボタンで送信されたidを表示
4. 受信したidのデータを削除
5. デバッグ用コードをコメントアウト

 bbs.phpのダウンロード
前チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/8/bbs.php )

本チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/9/bbs.php )


※Windows ：右クリック - 名前を付けてリンク先を保存
※Mac ：CTRL + クリック - リンクに名前を付けて保存
bbs.phpの修正箇所
送信されたid

```console
// 変数の設定
$content = $_POST["content"];
$delete_id = $_POST["delete_id"];


データを削除する
// データベースのデータの削除
$sql = "DELETE FROM bbs WHERE id = :delete_id;";
$stmt = $pdo->prepare($sql);
$stmt -> bindValue(":delete_id", $delete_id, PDO::PARAM_INT);
$stmt -> execute();
```


```php:index.php
発言リストのテーブル
// 取得したデータをテーブルで表示
// echo "del_id:".$delete_id;
?>
<table class="table">
    <tr>
        <th>No.</th>
        <!-- <th>id</th> -->
        <th>日時</th>
        <th>投稿内容</th>
    </tr>
<?php
while ($row = $stmt -> fetch(PDO::FETCH_ASSOC)) {
    $i++;
    if ($i % 2 == 1) {
?>
    <tr bgcolor="#cccccc">
<?php
  } else {
?>
    <tr>
<?php
  }
?>
    <td><?php echo "$i"; ?></td>
    <!-- <td><?php // echo "$row[id]"; ?></td> -->
    <td><?php echo "$row[updated_at]"; ?></td>
    <td><?php echo "$row[content]"; ?></td>
    <td>
      <form action="bbs.php" method="post" role="form">
        <button type="submit" class="btn btn-danger">削除</button>
        <div class="form-group">
			<input type="hidden" name="delete_id" value="<?php echo $row[id]; ?>" class="form-control"/>
		</div>
      </form>
    </td>
    </tr>
<?php
}
?>
</table>
```

##10:DBを改良しよう - 投稿者名の追加 
LAMP環境上に設置したWeb掲示板を、さらにカスタマイズしていきます。

 掲示板の機能追加の手順
1. 投稿フォームに、名前欄を追加
2. 発言リストに、名前欄を追加
3. データベースにuser_nameカラムを追加
4. 名前情報を挿入するコードを追加

bbs.phpのダウンロード
前チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/9/bbs.php )

本チャプターの完成版コード
bbs.php( https://paiza-webapp.s3.amazonaws.com/files/learning/bbs/10/bbs.php )


※Windows ：右クリック - 名前を付けてリンク先を保存
※Mac ：CTRL + クリック - リンクに名前を付けて保存

bbs.phpの修正箇所
投稿フォームに名前欄を追加

```php:bbs.php
<h2>投稿フォーム</h2>
<form action="bbs_41.php" method="post" role="form">
  <div class="form-group">
    <label class="control-label">名前</label>
    <input type="text" name="user_name" class="form-control" placeholder="名前"/>
  </div>
  <div class="form-group">
    <label class="control-label">投稿内容</label>
    <input type="text" name="content" class="form-control" placeholder="投稿内容"/>
  </div>
  <button type="submit" class="btn btn-primary">送信</button>
</form>
```

送信された名前情報
// 変数の設定
$content = $_POST["content"];
$user_name = $_POST["user_name"];
$delete_id = $_POST["delete_id"];


名前情報をデータベースに挿入
// データベースへのデータの挿入
$sql  = "INSERT INTO bbs (content, updated_at, user_name) VALUES (:content, NOW(), :user_name);";
$stmt = $pdo->prepare($sql);
$stmt -> bindValue(":content", $content, PDO::PARAM_STR);
$stmt -> bindValue(":user_name", $user_name, PDO::PARAM_STR);
$stmt -> execute();


```php:bbs.php
発言リストに名前欄を追加
// 取得したデータをテーブルで表示
// echo "del_id:".$delete_id;
?>
<table class="table">
    <tr>
        <th>No.</th>
        <!-- <th>id</th> -->
        <th>名前</th>
        <th>日時</th>
        <th>投稿内容</th>
	<th></th>
    </tr>
<?php
while ($row = $stmt -> fetch(PDO::FETCH_ASSOC)) {
    $i++;
    if ($i % 2 == 1) {
?>
    <tr bgcolor="#cccccc">
<?php
  } else {
?>
    <tr>
<?php
  }
?>
    <td><?php echo "$i"; ?></td>
    <td><?php echo "$row[user_name]" ?></td>
    <!-- <td><?php // echo "$row[id]"; ?></td> -->
    <td><?php echo "$row[updated_at]"; ?></td>
    <td><?php echo "$row[content]"; ?></td>
    <td>
      <form action="bbs_41.php" method="post" role="form">
        <button type="submit" class="btn btn-danger">削除</button>
        <div class="form-group">
			<input type="hidden" name="delete_id" value="<?php echo $row[id]; ?>" class="form-control"/>
		</div>
      </form>
    </td>
    </tr>
<?php
}
?>
</table>
```

