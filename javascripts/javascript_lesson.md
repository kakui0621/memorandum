JavaScript入門編1: JavaScriptをはじめよう (全9回)
この講座では、多くのシステム開発で使われているJavaScriptの初歩を学びます。 
最初のレッスンでは変数と計算について学んで、「サイコロ」アプリを作れるようになる事を目指します。
プログラミング学習 > JavaScript入門編 > JavaScript入門編1: JavaScriptをはじめよう




01:JavaScriptとは？ (4:40)
最初に、このコースの目的・対象者・学習の進め方を確認しましょう。 また、このコースの題材となるJavaScript（ジャバ スクリプト）の概要を説明します。
このチャプターを受講する
JavaScript
02:JavaScriptでプログラムを書いてみよう
02:JavaScriptでプログラムを書いてみよう (4:52)
ここでは実際に、JavaScriptでプログラムを書いていきます。 まずは、プログラミング言語を学ぶときに定番の「hello world」を書いてみましょう。
このチャプターを受講する
演習1：★



console.logで文字を出力する

process.stdin.resume();
process.stdin.setEncoding('utf8');
// ここに、出力するコードを書く
console.log("ハロー、paizaラーニング");



演習2：★
process.stdin.resume();
process.stdin.setEncoding('utf8');
// ここに、出力するコードを書く
console.log("hello paizaラーニング");



演習3：★
process.stdin.resume();
process.stdin.setEncoding('utf8');
// ここに、出力するコードを書く
console.log("hello paizaラーニング");



標準出力 HelloWorld JavaScript
03:コメントで、プログラムを見やすく！
03:コメントで、プログラムを見やすく！ (4:20)
ここでは、プログラムにコメントをつける方法を学びます。 コメントは、プログラムの実行時には無視されますが、人間がプログラムを読む時、理解を助けるメモとして利用できます。
このチャプターを受講する
演習1：★
演習課題「コメントアウトしてみよう！ vol.1」
右側のコードエリアにあるプログラムで、最初のconsole.log行をコメントアウトして、2番目の「モンスターがあらわれた」というメッセージだけが表示されるようにしてください。



//最初のconsole.logをコメントアウト
process.stdin.resume();
process.stdin.setEncoding('utf8');
// console.log("勇者は、荒野を歩いていた");
console.log("モンスターがあらわれた");



演習2：★
 演習課題「コメントアウトしてみよう！ vol.2」
右側のコードエリアにあるプログラムでは、console.logで出力する文字の先頭が「A:」となっている行がいくつかあります。このような行を先頭からコメントアウトして、残った行のメッセージだけが表示されるようにしてください。



//「A:」の行をコメントアウト
process.stdin.resume();
process.stdin.setEncoding('utf8');
console.log("勇者は、荒野を歩いていた");
// console.log("A:モンスターがあらわれた");
console.log("勇者は、すごい剣を手にいれた");
// console.log("A:ドラゴンがあらわれた");
// console.log("A:魔王があらわれた");
console.log("勇者は、世界を救った");



コメント・コメントアウト 複数行のコメントアウト JavaScript
04:HTMLを表示してみよう
04:HTMLを表示してみよう (4:00)
ここでは、JavaScriptを使って、HTMLを出力するプログラムを作ります。 プログラムからHTMLを出力すると、利用者の状況に応じて、Webページの内容を変化させることができます。これが、Webサービスを作る第1歩になります。
このチャプターを受講する
演習1：★
演習課題「HTMLとして出力してみよう」
右側のコードエリアにあるプログラムで、出力されるメッセージをpタグで囲んで、htmlとして表示されるようにしてください。



//文字列を<p>タグで囲む HTMLを表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');
console.log("<p>勇者は、荒野を歩いていた</p>");



演習2：★
演習課題「モンスターを太字にしてみよう」
右側のコードエリアにあるプログラムで、「モンスター」という文字を、bタグで太字にしてください。



//モンスターを<b>タグで囲む
// HTMLを表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');
console.log("勇者は、荒野を歩いていた");
console.log("<b>モンスター</b>があらわれた");

HTML JavaScript
05:変数を使えるようになろう
05:変数を使えるようになろう (4:25)
ここでは、RPGのようにメッセージを表示するプログラムを作ります。そして、文字や数字などのデータを格納する「変数」(へんすう)について学びます。変数を使うと、データが変化したとき、いちいちプログラムの複数個所を修正しなくてもよくなります。
このチャプターを受講する
演習1：★
演習課題「変数を表示してみよう」
右側のコードエリアにあるプログラムには、「は、レベルアップした」と表示するプログラムです。ここに変数を使って、「勇者は、レベルアップした」と出力してください。
// 変数を使う
process.stdin.resume();
process.stdin.setEncoding('utf8');
var player = "勇者";
console.log(player + "は、レベルアップした");



演習2：★
演習課題「間違いを修正してみよう vol.1」
右側のコードエリアにあるプログラムは、実行するとエラーになります。
プログラムを修正して、「勇者の体力が回復した」と表示されるようにしてください。


// 変数名を一致させる・変数を使う
process.stdin.resume();
process.stdin.setEncoding('utf8');
var player = "勇者";
console.log(player + "の体力が回復した");


演習3：★
演習課題「変数の文字を出力する」
右側のコードエリアにあるプログラムで、変数を使って、console.logで出力されるメッセージの前に、すべて「勇者」という文字を表示するようにしてください。


//player変数を連結する 変数を使う
process.stdin.resume();
process.stdin.setEncoding('utf8');
var player = "勇者";

console.log(player  + "は、荒野を歩いていた");
console.log(player  + "は、モンスターと戦った");
console.log(player  + "は、モンスターをたおした");



演習4：★
演習課題「間違いを修正してみよう vol.2」
右側のコードエリアにあるプログラムは、実行するとエラーになります。プログラムを修正して、「勇者と戦士の体力が回復した」と表示されるようにしてください。


//変数名を一致させる 変数を使う
process.stdin.resume();
process.stdin.setEncoding('utf8');
var team = "勇者と戦士";
console.log(team + "の体力が回復した");



変数 JavaScript
06:サイコロを作ろう
06:サイコロを作ろう (7:15)
ここでは、出現したモンスターの数を表示するプログラムを作ります。そして、数値を表示するプログラムについて学びます。 また、いくつかの数値の中から、サイコロのようにランダムにひとつの数値を選択できるrandom関数の使い方についても説明します。
このチャプターを受講する
演習1：★
演習課題「1から6のサイコロ」
右のコードエリアのプログラムは、1から6のランダムな数値を表示するプログラムです。
このコードを修正して、「サイコロの目は**です」と出力をしてください。**のところには、1 ～ 6のランダムな数字を入れます。


//number変数の前後にテキストを連結して出力する
// 数の表示とサイコロ
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 6) + 1;
console.log("サイコロの目は" + number + "です");





乱数 ランダム関数 サイコロ ゲームプログラム JavaScript
07:演算子で計算してみよう
07:演算子で計算してみよう (5:33)
ここでは、数値や変数を使って計算する方法と、四則演算で使用する記号(演算子：えんざんし)について学習します。
このチャプターを受講する
演習1：★
演習課題「計算してみよう」
1234かける5678割る2を計算して、出力してみましょう。


// 1234 * 5678 / 2を出力する　計算する
process.stdin.resume();
process.stdin.setEncoding('utf8');
// ここに計算式を書いて、出力する
console.log(1234 * 5678 / 2);


演習2：★
右側のコードエリアにあるプログラムは、2つの変数に数値を代入しています。
このコードに続けて、次の計算をおこない、その計算結果を出力するコードを書いてください。


//a変数とb変数をかけて、結果を出力する 計算する
process.stdin.resume();
process.stdin.setEncoding('utf8');
var a = 31;
var b = 17;
// 以下に、aとbをかけ算し、結果を出力するコードを書く
console.log(a * b);


演習3：★
演習課題「余りを計算してみよう」
右側のコードエリアにあるプログラムは、2つの変数に数値を代入しています。

このコードに続けて、次の計算をおこない、その計算結果を出力するコードを書いてください。


// 計算する
process.stdin.resume();
process.stdin.setEncoding('utf8');
var x = 8;
var y = 5;
// 以下に、xをyで割ったときの余りを計算し、結果を出力するコードを書く
console.log(x % y);




演習4：★
 演習課題「カッコを付けて計算してみよう」
1234と5678を足し算して、それを3倍した結果を計算して出力してみましょう。

プログラムを実行して、正しく出力されれば演習課題クリアです！


//カッコを使って、(1234 + 5678) * 3を計算する 計算する
process.stdin.resume();
process.stdin.setEncoding('utf8');
// ここに計算式を書いて、出力する
console.log((1234 + 5678) * 3);



演算子 四則演算 代数演算子 算術演算子 JavaScript
08:値段を計算してみよう
08:値段を計算してみよう (4:41)
ここでは、ここまでの応用として、演算子とrandom関数を使って、リンゴの値段を計算する、オンラインショッピングサイトのような簡単なプログラムを作成します。
このチャプターを受講する
演習1：★
演習課題「スライムの合計体重を出力！」
右側のコードエリアのプログラムは、出現するスライムの匹数をランダムに生成します。スライムの体重は、すべて体重100キロです。そして、「体重100キロのスライムがX匹あらわれた。」と表示します。
そこで、スライムの合計体重を計算して、「スライムの合計体重はYキロです。」と表示してください。



process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 10) + 1;// 匹数 1 ～ 10
console.log("体重100キロのスライムが" + number + "匹あらわれた。");
// 合計体重 = 匹数 × 100
var total = number * 100;// 合計体重 = 匹数 × 100
console.log("スライムの合計体重は" + total + "キロです。");



演算子 四則演算 代数演算子 算術演算子 JavaScript
09:データの型を覚えよう
09:データの型を覚えよう (4:10)


演習課題「エラー箇所を正しく修正しよう」
右側のコードエリアにあるプログラムは、2つの数値を連結して表示します。
これを足し算となるように修正をしてください。


//a変数のダブルクォーテーションを削除 データの種類
process.stdin.resume();
process.stdin.setEncoding('utf8');
var a = 12345;
var b = 67890;
console.log(a + b);





---------------------------------------------------------

JavaScript入門編2: 条件によって処理を変えてみよう (全6回)
JavaScriptでプログラミングの初歩を学びます。
そして、「平成年の計算」や「おみくじ」など、簡単なプログラムを作れるようになる事を目指します。
プログラミング学習 > JavaScript入門編 > JavaScript入門編2: 条件によって処理を変えてみよう


01:数値が一致した場合、メッセージを表示 (7:12)
ここでは、数値に応じて、表示するメッセージを切り替えるプログラムを作成します。 そして、条件に応じて、処理を枝分かれさせるif文について学習します
このチャプターを受講する
演習1：★
演習課題「順位が1位だったら「おめでとう！」と表示しよう」
右側のコードエリアにあるプログラムは、実行するたびに、1から3までの数値をランダムに生成して、順位として表示します。ここにif文を追加して、1位の時には「おめでとう！」と表示するようにしてください。


// if文による条件分岐
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 3) + 1;
console.log("あなたの順位は" + number + "位です");
// ここにif文を追加する
if (number == 1) {
  console.log("おめでとう！");
}



演習2：★
演習課題「順位が2位以下だったら「あと少し！」と表示する」
右側のコードエリアにあるプログラムは、実行するたびに、1から3までの数値をランダムに生成して、順位として表示します。ここにif文を追加して、1位の時には「おめでとう！」と表示し、それ以外の時には「あと少し！」と表示するようにしてください。



// if文による条件分岐
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 3) + 1;
console.log("あなたの順位は" + number + "位です");
// ここにif文を追加する
if (number == 1) {
  console.log("おめでとう！");
} else {
  console.log("あと少し！");
}



演習3：★
演習課題「間違い探しVol.1」
右側のコードエリアのプログラムは、実行するたびに、100～300の数値を100刻みでランダムに生成して、ポイントとして表示するプログラムです。
またポイントが300であれば「おめでとう！」と表示するように書いていますが、numberが300でなくても「おめでとう！」と表示されてしまいます。
このプログラムを修正して、正しく表示されるようにしてください。


//条件式を「==」で記述する
// if文による条件分岐
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = (parseInt(Math.random() * 3) + 1) * 100;
console.log("あなたの得点は" + number + "ポイントです");
// ここにif文を追加する
if (number == 300) {
  console.log("おめでとう！");
}




演習4：★
演習課題「間違い探しVol.2」
右側のコードエリアのプログラムは、実行するたびに、100～300の数値を100刻みでランダムに生成して、ポイントとして表示するプログラムです。
またポイントが300であれば「おめでとう！」と表示し、それ以外であれば「ざんねん！」と表示するように書いていますが、エラーになってしまいます。
このプログラムを修正して、正しく表示されるようにしてください。



//波カッコ忘れ
// if文による条件分岐
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = (parseInt(Math.random() * 3) + 1) * 100;
console.log("あなたの得点は" + number + "ポイントです");
// ここにif文を追加する
if (number == 300) {
  console.log("おめでとう！");
} else {
  console.log("ざんねん！ ");
}


if文 条件分岐 JavaScript
02:複数の条件を組み合わせてみよう
02:複数の条件を組み合わせてみよう (4:02)
ここでは、条件をひとつではなく複数にして、それぞれ異なるメッセージを表示するプログラムを作成します。そして、if文で、複数の条件式を追加できる「else if」について学習します。
このチャプターを受講する
演習1：★
演習課題「順位に合わせてメッセージを表示する」
右側のコードエリアのプログラムは、実行するたびに、1から5までの数値をランダムに生成して、順位として表示します。ここにif文を追加して、次のように表示するようにしてください。

- 1位の時　「おめでとう！」と表示する
- 2位の時　「あと少し！」と表示する
- その他の時「よくがんばったね」と表示する


// if文による条件分岐　else if文
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 5) + 1;
console.log("あなたの順位は" + number + "位です");
// ここにif文を追加する
if (number == 1) {
  console.log("おめでとう！");
} else if (number == 2) {
  console.log("あと少し！");
} else {
  console.log("よくがんばったね");
}


演習2：★
演習課題「間違い探し」
右のコードは、実行するたびに、1から5までの数値をランダムに生成して、順位として表示します。
順位ごとに下記のメッセージを表示しますが、このまま実行しても、エラーになってしまいます。
このプログラムを修正して、正しく表示されるようにしてください。

- 1位の時 「おめでとう！」と表示する
- 2位の時 「あと少し！」と表示する
- その他の時 「よくがんばったね」と表示する


//elseifをelse ifに変える
// if文による条件分岐　else if文
process.stdin.resume();
process.stdin.setEncoding('utf8');
var number = parseInt(Math.random() * 5) + 1;
console.log("あなたの順位は" + number + "位です");
// ここにif文を追加する
if (number == 1) {
  console.log("おめでとう！");
} else if (number == 2) {
  console.log("あと少し！");
} else {
  console.log("よくがんばったね");
}



if文 条件分岐 複数条件 else文 JavaScript
03:比較演算子で条件分岐してみよう
03:比較演算子で条件分岐してみよう (5:41)
ここでは、数値が一定以上だったら、メッセージを表示するプログラムを作成します。
そして、if文で、数値が大きかったら、小さかったらといった場合の条件式を作る、
比較演算子について学習します。
このチャプターを受講する
演習1：★
 演習課題「飲酒可能な年齢か判定する！」
右側のコードエリアのプログラムをもとに、プログラムを完成させてください。

age変数には、飲酒可能か判定する人の年齢として、18〜22才までのランダムな数値を代入しています。
例）19才だったら、19が代入されているとします。

20才未満の場合は「○才は飲酒不可」と表示し
20才以上だったら「○才は飲酒可能」と表示するプログラムを書きましょう。


//ageが20未満の場合、飲酒不可と表示する
// if文による条件分岐　比較演算子
process.stdin.resume();
process.stdin.setEncoding('utf8');
var age = parseInt(Math.random() * 5) + 18;
process.stdout.write (age + "才は");
// ここにif文を追加
if (age < 20) {
  console.log("飲酒不可");
} else {
  console.log("飲酒可能");
}





演習2：★
演習課題「入賞圏内か判別する」
右側のコードエリアのプログラムは、実行しても期待通りの動きをしていません。if文を追加してプログラムを完成させてください。

place変数には、入賞判別したいレースの順位として、1〜12位までのランダムな数値を代入しています
例）5位だったら、5が代入されているものとします。

6位以上の場合は「●位入賞」と表示し、
7位以下だったら「●位入賞圏外」と表示するプログラムを書きましょう。



//7未満だったら、入賞と表示する
// if文による条件分岐　比較演算子
process.stdin.resume();
process.stdin.setEncoding('utf8');
var place = parseInt(Math.random() * 12) + 1;
process.stdout.write (place + "位");
// ここにif文を追加する
if (place < 7) {
  console.log("入賞");
} else {
  console.log("入賞圏外");
}


if文 条件分岐 比較演算子 else文 JavaScript
04:おみくじを作ってみよう
04:おみくじを作ってみよう (6:10)
このチャプターでは、これまでに覚えたif文による条件分岐とrandom関数を使って、実行するたびに結果が変わる「おみくじプログラム」を作成してみましょう。
このチャプターを受講する
演習1：★
演習課題「大吉が出る確率を上げてみよう」
右のコードを完成させて、「大吉」か「大凶」を出力する、次のようなおみくじプログラムを作成してください。

- omikuji変数には、1から100までの値がランダムに代入されます。
- omikuji変数の値が30から100の場合は、「omikujiの中身は○○なので大吉」と表示
- omikuji変数の値が29以下の場合は、「omikujiの中身は○○なので大凶」と表示

例1: omikujiの中身は32なので大吉
例2: omikujiの中身は12なので大凶




// おみくじを作る
process.stdin.resume();
process.stdin.setEncoding('utf8');
var omikuji = parseInt(Math.random() * 100) + 1;
if (omikuji > 30) {
  console.log("omikujiの中身は" + omikuji  + "なので大吉");
} else {
  console.log("omikujiの中身は" + omikuji  + "なので大凶");
}



if文 条件分岐 乱数 ランダム関数 おみくじ ゲームプログラム JavaScript
05:RPGのクリティカルヒットを再現
05:RPGのクリティカルヒットを再現 (3:09)
このチャプターでは、これまでに覚えたif文による条件分岐と、random関数を使って、
RPGの戦闘シーンに出てくるようなクリティカルヒットをメッセージとして表示します。
このチャプターを受講する
演習1：★
 演習課題「攻撃を回避させてみよう」
右のプログラムでは出目が1から6のサイコロをふっています。
サイコロの出目によってスライムからの攻撃を回避するプログラムを書いてみましょう。

出目が4から6ならば、「スライムの攻撃をかわした」と表示してください。
そうでなければ、「スライムから10のダメージを受けた」と表示してください。


//if 文と比較演算子の組み合わせを確認してください
process.stdin.resume();
process.stdin.setEncoding('utf8');
var dice = parseInt(Math.random() * 6) + 1;
console.log("サイコロは" + dice);
if (dice >= 4) {
    console.log("スライムの攻撃をかわした");
} else {
    console.log("スライムから10のダメージを受けた");
}


if文 条件分岐 乱数 ランダム関数 RPG ゲームプログラム JavaScript
06:西暦から平成何年か求めてみよう
06:西暦から平成何年か求めてみよう (5:17)
このチャプターでは、入力しておいた西暦に応じて、平成何年かを計算するプログラムを作成してみます。

演習課題「西暦年から昭和年を計算する」
右のコードは、実行するたびに1926年から1988年までの西暦年をランダムに選んで表示します。ここにコードを追加して、昭和年を計算し「西暦XXXX年は昭和YY年です」と表示してください。

なお、昭和年は、「seireki - 1925」で求めることができます。



// 西暦年から昭和年を求める
// 西暦年から昭和年を求める
process.stdin.resume();
process.stdin.setEncoding('utf8');
var seireki = parseInt(Math.random() * 63) + 1926;
process.stdout.write ("西暦" + seireki + "年は");

// 昭和年を計算
var showa = seireki - 1925;
console.log("昭和" + showa + "年です");



---------------------------------------------------------

JavaScript入門編3: ループ処理を学ぶ (全8回)
JavaScriptを使って、同じ手順を繰り返すループ処理の基本を学びます。
ループ処理は、大量のデータを処理するためには、欠かせないテクニックです。
また、プログラムの外部からデータを入力する方法についても取り上げます。
プログラミング学習 > JavaScript入門編 > JavaScript入門編3: ループ処理を学ぶ




01:条件によるくり返し処理1 - while
01:条件によるくり返し処理1 - while (5:47)
このチャプターでは、数字を0から5まで表示させます。条件によって処理を繰り返すwhileという命令について学習しましょう。
このチャプターを受講する
演習1：★
演習課題「「ハローpaizaラーニング」と10回表示する」
右のコードは、「ハローpaizaラーニング」と表示するプログラムです。
whileを使って、「ハローpaizaラーニング」と10回出力するよう修正してください。



//whileで10回繰り返す
// 「ハローpaizaラーニング」と10回表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var count = 0;
while (count < 10) {
    console.log('ハローpaizaラーニング');
    count = count + 1;
}


演習2：★
演習課題「数値を0から15まで表示する」
while命令を使って、0から15まで、数値を一行ずつ表示するプログラムを作成してください。



//whileで0から15まで繰り返す
// 数値を0から15まで表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var count = 0;
while (count <= 15) {
    console.log(count);
    count = count + 1;
}


ループ while文 JavaScript
02:条件によるくり返し処理2 - while
02:条件によるくり返し処理2 - while (5:19)
whileを使った繰り返し処理について、もう少し学習します。そして、初期値や条件式を変更するとどうなるのか試してみましょう。
このチャプターを受講する
演習1：★
 演習課題「1から10までの偶数を表示する」
whileを使って、1から10までの偶数を一行ずつ表示するプログラムを作成してください


//増分を2にして、2から10まで繰り返す
// 1から10までの偶数を表示する

process.stdin.resume();
process.stdin.setEncoding('utf8');

var count = 2;
while(count <= 10) {
    console.log(count);
    count = count + 2;
}



ループ while文 JavaScript
03:RPGの攻撃シーンを作る
03:RPGの攻撃シーンを作る (7:00)
数値を5から1までカウントダウンさせるプログラムを作ります。whileを使って、RPGの攻撃シーンのようなプログラムを作ってみましょう。
このチャプターを受講する
演習1：★
演習課題「数値を10から1までカウントダウン表示する」
whileを使って、10から1まで、数値を一行ずつカウントダウン表示するプログラムを作成してください。



//初期値を10、条件を1以上、増分を-1にする
// 数値を10から1までカウントダウン表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var count = 10;
while (count >= 1) {
    console.log(count);
    count -= 1;
}



演習2：★
演習課題「数値を20から10までカウントダウン表示する」
whileを使って、20から10まで、数値を一行ずつカウントダウン表示するプログラムを作成してください。


//初期値を20、条件を10以上、増分を-1にする
// 数値を20から10までカウントダウン表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var count = 20;
while (count >= 10) {
    console.log(count);
    count -= 1;
}

演習3：★
 演習課題「20から10までの奇数を表示する」
whileを使って、20から10までの奇数を一行ずつカウントダウン表示するプログラムを作成してください。



//初期値を19、条件を10以上、増分を-2にする
// 20から10までの奇数を表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');
var count = 19;
while (count >= 10) {
    console.log(count);
    count -= 2;
}



ループ while文 JavaScript
04:条件によるくり返し処理3 - for
04:条件によるくり返し処理3 - for (5:07)
このチャプターでは、数字を0から5まで表示させます。forという命令について学習しましょう。
このチャプターを受講する
演習1：★
演習課題「「ハローpaizaラーニング」を10回表示する」
右のコードは、「ハローpaizaラーニング」と表示するプログラムです。
for命令を使って、「ハローpaizaラーニング」と10回出力するよう修正してください。



//for命令で、10回繰り返す
// 「ハローpaizaラーニング」を10回表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

for (i = 0; i < 10; i++) {
    console.log("ハローpaizaラーニング");
}



演習2：★
演習課題「数値を0から15まで表示する」
for命令を使って、0から15まで、数値を一行ずつ表示する出力するプログラムを作成してください。



//forで0から15まで繰り返す
// 数値を0から15まで表示する
process.stdin.resume();
process.stdin.setEncoding('utf8');

for (i = 0; i < 16; i ++) {
    console.log(i);
}


演習3：★
演習課題「1月から12月まで表示する」
for命令を使って、1月から12月まで、一行ずつ表示する出力するプログラムを作成してください。

// 1月から12月まで表示する

process.stdin.resume();
process.stdin.setEncoding('utf8');

for (i = 1; i < 13; i++) {
    console.log(i + "月");
}

ループ for文 JavaScript
05:データの入力方法を理解しよう
05:データの入力方法を理解しよう (3:15)
このチャプターでは繰り返し処理から少し離れて、プログラムの外部からデータを入力する、標準入力について学習します。
このチャプターを受講する
標準入力 JavaScript
06:標準入力で1行データを受け取ってみよう
06:標準入力で1行データを受け取ってみよう (7:09)
標準入力からデータを受け取るプログラムを作成します。標準入力を使うと、プログラムの実行時にデータを受け取ることができるようになります。
このチャプターを受講する
演習1：★


演習課題「標準入力からテキストを取得する」
標準入力から文字列を1行取得して、テキストを出力するプログラムを作成してください。
読み込む文字列には、空白やタブは含まれません。


// 標準入力からテキストを取得する
//process.stdin.onで標準入力のイベントを取得する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var input_string = "";
var reader = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});
reader.on('line', (line) => {
    // ここで入力を処理する
    input_string = line;
});
reader.on('close', () => {
    // ここで出力する
    console.log(input_string);
});


標準入力 JavaScript
07:標準入力で複数行データを受け取ってみよう
07:標準入力で複数行データを受け取ってみよう (4:35)
標準入力から複数行のデータを受け取った場合の動きを確認します。
このチャプターを受講する
演習1：★
演習課題「複数行の標準入力を取得する」
入力エリアに3行のデータが示されています。
入力エリアからデータを取得して、すべての行の文字列データを出力するプログラムを作成してください。



// 複数行の標準入力を取得する
//split('\n')を使って改行区切りで配列に格納する
process.stdin.resume();
process.stdin.setEncoding('utf8');

var lines = [];
var reader = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});
reader.on('line', (line) => {
    // ここで入力を処理する
    lines.push(line);
});
reader.on('close', () => {
    // ここで出力する
    console.log(lines[0]);
    console.log(lines[1]);
    console.log(lines[2]);
});




標準入力 JavaScript
08:西暦年と平成年の対応表を作る
08:西暦年と平成年の対応表を作る (4:34)
繰り返し処理を使って、西暦年と平成年の対応表を作ります。ひとつの年だけではなく、1989年から2018年まで全ての年を出力しましょう。

演習課題「西暦年と昭和年の対応表を作ろう」
西暦年と昭和年の対応表を作成してください。対応表は、「西暦X年は昭和Y年です」と表示します。なお、昭和年は、西暦1926年から西暦1988年までの期間で、「西暦年 - 1925」で求めることができます。


//1926から1988まで繰り返して、昭和年を求める
// 西暦年と昭和年の対応表を作ろう
process.stdin.resume();
process.stdin.setEncoding('utf8');

for (seireki = 1926; seireki < 1989; seireki++) {
    var syouwa = seireki - 1925;

    console.log("西暦" + seireki + "年は昭和" + syouwa + "年です");
}
-----------------------------------------------------
JavaScript入門編4: 配列の基礎 (全9回)
JavaScriptでの配列の基礎について学び、より高度で柔軟性の高い
ランダムくじ引きが作れるようになる事を目指します。

01:配列とは何かを学ぼう
01:配列とは何かを学ぼう (4:14)
ここでは、複数の値をまとめて扱うことができる配列について、基本的な考え方を学習します。
このチャプターを受講する
配列 JavaScript
02:配列を作ろう
02:配列を作ろう (4:58)
ここでは、配列の基本操作について学びます。 配列の作成、表示、要素の追加といった操作を試してみましょう。
このチャプターを受講する
演習1：★
演習課題「配列の中身を出力してみよう」
右のコードには、配列が定義されています。この配列をそのまま標準出力に出力してください。


// 配列の中身を出力してみよう

process.stdin.resume();
process.stdin.setEncoding('utf8');

var party = ["戦士", "侍", "僧侶", "魔法使い"];

// ここで配列を出力する
console.log(party);




演習2：★
 演習課題「指定の文字を配列にしてみよう」
item という配列に、下記の要素をこの並び順で追加して、
そのまま標準出力で出力してください
「ロングソード」「ブレードソード」「エクスカリバー」



// 指定の文字を配列にしてみよう
process.stdin.resume();
process.stdin.setEncoding('utf8');

// ここで配列を定義する
var item = ["ロングソード", "ブレードソード", "エクスカリバー"];

// ここで配列を出力する
console.log(item);



演習3：★
演習課題「変数を配列に代入しよう」
右のコードには、player_1, player_2, player_3という変数に、文字列が代入されています。
このplayer_1 ~ 3を、この順番で配列に追加して、そのまま標準出力に出力してください。
プログラムを実行して、正しく出力されれば演習課題クリアです！


//配列時に変数を指定する
// 変数を配列に代入しよう

process.stdin.resume();
process.stdin.setEncoding('utf8');

var player_1 = '勇者';
var player_2 = '魔法使い';
var player_3 = '戦士';

// ここで配列を定義する
var jobs = [player_1, player_2, player_3];

// ここで出力する
console.log(jobs);



配列 JavaScript
03:配列の要素を取り出してみよう
03:配列の要素を取り出してみよう (4:51)
ここでは、配列の要素をいろいろな方法で取り出してみます。 配列は、各要素に割り当てられたインデックスと呼ばれる番号を使って要素を取り出します。 また、インデックスは変数で指定したり、計算して指定することができます。
このチャプターを受講する
演習1：★
演習課題「配列の最初の要素を取り出してみよう」
右のコードエリアには、5つの要素を持つ配列が定義されています。
この配列の1番目の要素を標準出力に出力してください。


//配列の添字は0から数える
// 配列の最初の要素を取り出してみよう
process.stdin.resume();
process.stdin.setEncoding('utf8');

team = ["勇者", "戦士", "侍", "忍者", "魔法使い"];

// ここで最初の要素を出力する
console.log(team[0]);




配列 JavaScript
04:配列を操作しよう
04:配列を操作しよう (7:06)
ここでは、配列を操作し、要素の追加、変更といった処理をしてみましょう。
このチャプターを受講する
演習1：★
演習課題「配列に要素を追加してみよう」
右のコードエリアには、4つの要素を持つweapon配列が定義されています。
この配列の末尾に「石斧」という要素を追加してください。


//weaponに.pushで要素を追加する
// 配列に要素を追加してみよう

process.stdin.resume();
process.stdin.setEncoding('utf-8');

var weapon = ["木の棒", "鉄の棒", "鉄の剣", "鋼の剣"];

// ここで要素を追加する
weapon.push("石斧");

console.log(weapon);





演習2：★
演習課題「配列の要素を上書きしてみよう」
右のコードエリアには、4つの要素を持つweapon配列が定義されています。
この配列のインデックス3の要素を、「石斧」に書き換えてください。
配列は0番から始まることに注意してください。

//weapon[3]に代入する
// 配列の要素を上書きしてみよう

process.stdin.resume();
process.stdin.setEncoding('utf-8');

var weapon = ["木の棒", "鉄の棒", "鉄の剣", "鋼の剣"];

// ここで配列の要素を上書きする
weapon[3] = "石斧";

console.log(weapon);




配列 JavaScript
05:ループで配列の要素を処理しよう1
05:ループで配列の要素を処理しよう1 (7:46)
ここでは、繰り返し処理を使って、配列の要素を順番に処理します。
このチャプターを受講する
演習1：★
演習課題「配列の中身を1行ずつ表示してみよう」
右のコードエリアには、モンスターがenemy配列で定義されています。
この配列から要素を順に取り出して、出力してください。


//forで配列から要素を取り出す
// 配列の中身を1行ずつ表示してみよう

process.stdin.resume();
process.stdin.setEncoding('utf-8');

var enemy = ["スライム", "モンスター", "ゾンビ", "ドラゴン", "魔王"];

// for文で配列の要素を1つずつ出力する
for (var monster of enemy) {
    console.log(monster);
}



配列 JavaScript
06:ループで配列の要素を処理しよう2
06:ループで配列の要素を処理しよう2 (3:16)
ここでは、forEachメソッドで繰り返し配列の要素を出力します。 
ここまでくりかえし処理では、forやfor in、whileを使ってきましたが、
forEachメソッドも幅広く使われているんですよ。
このチャプターを受講する
演習1：★
演習課題「forEachで配列の要素を出力してみよう」
右のコードエリアには、5つの要素を持つcities配列が定義されています。
この配列からforEach文を使って、要素を順に取り出して出力してください。


//forEachで配列から要素を取り出す
// forEachで配列の要素を出力してみよう
process.stdin.resume();
process.stdin.setEncoding('utf-8');

var cities = ["Tokyo", "Kanagawa", "Chiba", "Shizuoka", "Saitama"];


// forEachで配列の要素を1行ずつ出力する
cities.forEach(city => {
    console.log(city);
});




配列 JavaScript
07:splitで文字列を分割しよう
07:splitで文字列を分割しよう (4:57)
ここでは、標準入力から取得したデータを配列に変換する方法を学習します。
カンマで区切られた1行のデータを、カンマごとに分割して配列に格納しましょう。
このチャプターを受講する
演習1：★
演習課題「文字列をカンマで分割してみよう」
右のコードエリアでは、team_strという文字列に、RPGのプレイヤーが、カンマで区切られて代入されています。
この文字列を、splitメソッドを使ってカンマのところで分割し配列に格納してください。
また、その配列をそのまま標準出力に出力してください。


//文字列を .split(",")で分割する
// 文字列をカンマで分割してみよう

process.stdin.resume();
process.stdin.setEncoding('utf-8');

var team_str = "勇者,戦士,忍者,魔法使い";

// splitで分割し配列に格納、標準出力に出力する
var team = team_str.split(",");
console.log(team);


演習2：★
演習課題「標準出力をカンマで分割してみよう」
標準入力からカンマ区切りの文字列が与えられます。
この文字列を、splitメソッドを使ってカンマのところで分割し配列に格納してください。
また、その配列をそのまま標準出力に出力してください。

//標準入力を .split(",")で分割する
// 文字列をカンマで分割してみよう

process.stdin.resume();
process.stdin.setEncoding('utf-8');

var input_string = "";
var reader = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});

reader.on('line', (line) => {
    input_string = line;
});

reader.on('close', () => {
    var array = [];

    // ここでカンマで区切って配列に格納する
    array = input_string.split(",");

    console.log(array);
});


配列 標準入力 JavaScript
08:複数行のデータを読み取ろう
08:複数行のデータを読み取ろう (2:44)
ここでは、標準入力から受け取った複数行のデータを配列に格納します。
読み込む行数が事前に分からなくても、すべての行を取得できるようにしましょう。



演習課題「標準入力から複数行を読み込もう」
標準入力からモンスターの名前が複数行データとして与えられます。
この文字列を、「＊＊が現れた」という形式で出力してください。
プログラムを実行して、正しく出力されれば演習課題クリアです！


process.stdin.resume();
process.stdin.setEncoding('utf-8');

var lines = [];
var reader = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});

reader.on('line', (line) => {
    // 配列に標準入力を追加する
    lines.push(line);
});

reader.on('close', () => {
    // 配列の要素を繰り返し出力する
    lines.forEach(line => {
        console.log(line + "が現れた");
    });
});




このチャプターを受講する
演習1：★
標準入力 JavaScript
09:配列を使ったランダムくじ
09:配列を使ったランダムくじ (6:25)
ここでは、配列を使って、RPGの戦闘シーンを表現したメッセージを表示するプログラムを作ります。



演習課題「じゃんけんプログラムを作ろう」
入力エリアに、じゃんけんの手(例：グー,チョキ,パー)が用意してあります。
右のコードエリアのコメントを参考にして、じゃんけんプログラムを作ってください。
じゃんけんの手は、標準入力から読み込んだ文字列をカンマで分割して、そのうち1つをランダムに出力します。
このとき、カンマで分割した配列をそのまま出力して、それからじゃんけんの結果を出力してください。



// じゃんけんプログラムを作ろう

process.stdin.resume();
process.stdin.setEncoding('utf8');

var input_string = "";
var reader = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout
});

reader.on('line', (line) => {
    input_string = line;
});

reader.on('close', () => {
    var values = input_string.split(",");

    // 配列をそのまま出力する
    console.log(values);

    // 生成するランダムな数値の範囲を調べる
    var hands = values.length;

    // ランダムにインデックスを生成する
    var target = Math.floor(Math.random() * hands);

    // 選ばれた手を出力する
    console.log(values[target]);
});
