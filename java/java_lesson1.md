Java入門編1:プログラミングを学ぶ (全9回)
Javaでプログラミングの初歩を学びます。第一回では変数と計算について学びます。「サイコロ」Webアプリを作れるようになる事を目指します。
プログラミング学習 > Java入門編 > Java入門編1:プログラミングを学ぶ



01:Javaとは？ (2:51)
このコースの目的、対象者、学習方法についての解説と、Javaの概要について解説をします。
このチャプターを受講する
Java
02:Javaでプログラムを書いてみよう
02:Javaでプログラムを書いてみよう (6:12)
オンラインエディタを使って実際にJavaプログラムを書いていきます。まずは各言語を学ぶときのお約束のHello world!を書いてみよう！
このチャプターを受講する

演習1：helloworld


public class Main {
	public static void main(String[] args) {
		System.out.println("hello world");//末尾にセミコロン
	}
}


標準出力 HelloWorld Java
03:コメントでプログラムを見やすく！
プログラムを読む際に何をやっているか解りやすいように、コードにコメントを付ける方法を学びます。
このチャプターを受講する
演習：HelloWorld Java★


public class Main {
	public static void main(String[] args) {
		// System.out.println("勇者は、荒野を歩いていた");
		System.out.println("モンスターがあらわれた");
	}
}


コメント・コメントアウト 複数行のコメントアウト Java
04:HTMLを表示してみよう
04:HTMLを表示してみよう (3:03)
JavaでHTMLを出力する方法を学びます。H1や太字などにしてみましょう！
このチャプターを受講する

演習：HTML出力★


// HTMLを表示する
public class Main {
	public static void main(String[] args) {
		System.out.println("<p>勇者は、荒野を歩いていた</p>");
	}
}



HTML Java
05:変数を使えるようになろう
05:変数を使えるようになろう (4:18)
文字や数字などのデータを格納する変数(へんすう)について学びます。変数を使うと、データが変化したとき、いちいちプログラムの複数個所を修正しなくてもよくなります。

模範解答1
player変数と文字列を連結する


public class Main {
	public static void main(String[] args) {
		String player = "勇者";
		System.out.println(player + "は、レベルアップした");
	}
}


変数 Java
06:サイコロを作ろう
06:サイコロを作ろう (7:45)
Javaで、実行するたびに数字が変わるWebサイコロを作ってみよう！
このチャプターを受講する
演習1：★

number変数の前後にテキストを連結して出力する

// 数の表示とサイコロ
public class Main {
	public static void main(String[] args) {
		double rand = Math.random() * 6 + 1;
		int number = (int)rand;
		System.out.println("サイコロの目は" + number + "です");
	}
}


演習2：★

public class Main {
	public static void main(String[] args) {
		double rand = Math.random() * 50 + 50;
		int number = (int)rand;
		System.out.println("モンスターに、" + number + "のダメージを与えた");
	}
}



乱数 ランダムメソッド サイコロ ゲームプログラム Java
07:演算子で計算してみよう
07:演算子で計算してみよう (5:05)
演算子を使えるようになると、プログラムで色々な計算ができるようになります。
このチャプターを受講する
演習1：★

1234 * 5678 / 2を出力する
//計算する
public class Main {
	public static void main(String[] args) {
		// 以下に計算式を書いて、結果を出力する
		System.out.println(1234 * 5678 / 2);
	}
}

演習2：★

a変数とb変数をかけて、結果を出力する
//計算する
public class Main {
	public static void main(String[] args) {
		int a = 31;
		int b = 17;
		// 以下に、aとbのかけ算し、結果を出力するコードを書いてください
		System.out.println(a * b);
	}
}
演習3：★

//計算する
public class Main {
	public static void main(String[] args) {
		int x = 8;
		int y = 5;
		// 以下に、xとyを割ったときの余りを計算し、結果を出力するコードを書いてください
		System.out.println(x % y);
	}
}
演習4：★

カッコを使って、(1234 + 5678) * 3を計算する
//計算する
public class Main {
	public static void main(String[] args) {
		// 以下に計算式を書いて、結果を出力する
		System.out.println((1234 + 5678) * 3);
	}
}


演算子 四則演算 代数演算子 算術演算子 Java
08:値段を計算してみよう
08:値段を計算してみよう (4:22)
オンラインショッピングのように、単価と個数に応じて合計金額を計算するプログラムを作成します。
このチャプターを受講する
演習1：★
演習課題「スライムの合計体重を出力！」
右側のコードエリアのプログラムは、出現するスライムの匹数をランダムに生成します。スライムの体重は、すべて体重100キロです。そして、「体重100キロのスライムが、X匹あらわれた。」と表示します。
そこで、スライムの合計体重を計算して、「スライムの合計体重は、Yキロです。」と表示してください。


public class Main {
	public static void main(String[] args) {
		int number =(int)(Math.random() * 10 + 1);	// 匹数 1 ～ 10
		System.out.println("体重100キロのスライムが、" + number + "匹あらわれた。");
		int total = number * 100;	// 合計体重 =匹数 × 100
		System.out.println("スライムの合計体重は、" + total + "キロです。");
	}
}


演算子 四則演算 代数演算子 算術演算子 Java
09:データの型を覚えよう
09:データの型を覚えよう (3:46)
Javaで扱う基本的なデータの種類（型）について学びます。



// データの種類
public class Main {
	public static void main(String[] args) {
		int x = 50;
		System.out.println(x - 10);
	}
}


// データの種類
public class Main {
	public static void main(String[] args) {
		String a = "モンスターが";
		String b = "あらわれた";
		System.out.println(a + b);
	}
}



public class Main {
	public static void main(String[] args) {
		String a = "01234";
		int b = 56789;
		System.out.println(a + b);
	}
}



Java入門編2:条件によって処理を変えてみよう (全11回)
Javaでプログラミングの初歩を学びます。「平成年度の計算」や「おみくじ」など、簡単なWebアプリケーションを作れるようになる事を目指します。
プログラミング学習 > Java入門編 > Java入門編2:条件によって処理を変えてみよう

01:IF文による条件分岐 (4:37)
ここでは、数値に応じて、表示するメッセージを切り替えるプログラムを作成します。そして、条件に応じて、処理を枝分かれさせるif文について学習します。
このチャプターを受講する
演習1：★
 演習課題「順位が1位だったら「おめでとう！」と表示しよう」
右側のコードエリアにあるプログラムは、実行するたびに、1から3までの数値を
ランダムに生成して、順位として表示します。ここにif文を追加して、
1位の時には「おめでとう！」と表示するようにしてください。


// if文による条件分岐
public class Main {
	public static void main(String[] args) {
		int number =(int)(Math.random() * 3 + 1);
		System.out.println("あなたの順位は" + number + "位です");
		// ここにif文を追加する
		if (number == 1) {
			System.out.println("おめでとう！");
		}
	}
}


演習2：★
演習課題「順位が2位以下だったら「あと少し！」と表示する」
右側のコードエリアにあるプログラムは、実行するたびに、1から5までの数値をランダムに生成して、
順位として表示します。ここにif文を追加して、1位の時には「おめでとう！」と表示し、
それ以外の時には「あと少し！」と表示するようにしてください。


// if文による条件分岐
public class Main {
	public static void main(String[] args) {
		int number =(int)(Math.random() * 5 + 1);
		System.out.println("あなたの順位は" + number + "位です");
		// ここにif文を追加する
		if (number == 1) {
			System.out.println("おめでとう！");
		} else {
			System.out.println("あと少し！");
		}
	}
}


演習3：★
右側のコードエリアのプログラムは、実行するたびに、100～300の数値を100刻みでランダムに生成して、ポイントとして表示するプログラムです。

// if文による条件分岐
public class Main {
	public static void main(String[] args) {
		int number =((int)(Math.random() * 3 + 1)) * 100;
		System.out.println("あなたの得点は" + number + "ポイントです");
		// ここにif文を追加する
		if (number == 300) {
			System.out.println("おめでとう！");
		}
	}
}



演習4：★

演習課題「間違い探し Vol.2」
右側のコードエリアのプログラムは、実行するたびに、100～300の数値を100刻みでランダムに生成して、ポイントとして表示するプログラムです。
またポイントが300であれば「おめでとう！」と表示し、それ以外であれば「ざんねん！」と表示するように書いていますが、エラーになってしまいます。

// if文による条件分岐
public class Main {
	public static void main(String[] args) {
		int number =((int)(Math.random() * 3 + 1)) * 100;
		System.out.println("あなたの得点は" + number + "ポイントです");
		// ここにif文を追加する
		if (number == 300) {
			System.out.println("おめでとう！");
		} else {
			System.out.println("ざんねん！");
		}
	}
}

if文 条件分岐 Java
02:複数の条件を組み合わせてみよう
02:複数の条件を組み合わせてみよう (3:18)
ここでは、条件をひとつではなく複数にして、それぞれ異なるメッセージを表示するプログラムを作成します。そして、if文で、複数の条件式を指定する「else if」について学習します。
このチャプターを受講する
演習1：★
演習課題「順位に合わせてメッセージを表示する」
右側のコードエリアのプログラムは、実行するたびに、1から5までの数値をランダムに生成して、順位として表示します。ここにif文を追加して、次のように表示するようにしてください。

- 1位の時　「おめでとう！」と表示する
- 2位の時　「あと少し！」と表示する
- その他の時「よくがんばったね」と表示する


// if文による条件分岐　else if
public class Main {
	public static void main(String[] args) {
		int number = (int)(Math.random() * 5 + 1);
		System.out.println("あなたの順位は" + number + "位です");
		if (number == 1) {
			System.out.println("おめでとう！");
		} else if (number == 2) {
			System.out.println("あと少し！");
		} else {
			System.out.println("よくがんばったね");
		}
	}
}




if文 条件分岐 複数条件 else文 Java
03:比較演算子で条件分岐してみよう
03:比較演算子で条件分岐してみよう (4:51)
if文で、数値が大きかったら、小さかったらといった場合に対応する、比較演算子について学習します。
このチャプターを受講する
演習1：★
 演習課題「飲酒可能な年齢か判定する！」
右側のコードエリアのプログラムをもとに、プログラムを完成させてください。

age変数の中には、飲酒可能か判定する人の年齢が、18〜22才までランダムに数値が代入されています。
例）19才だったら、19が代入されているとします。

20才未満の場合は「○才は飲酒不可」と表示し
20才以上だったら「○才は飲酒可能」と表示する


//ageが20未満の場合、飲酒不可と表示する
// if文による条件分岐　比較演算子
public class Main {
	public static void main(String[] args) {
		int age = (int)(Math.random() * 5 + 18);
		System.out.print(age + "才は");
		// ここにif文を追加する
		if (age < 20) {
			System.out.print("飲酒不可");
		} else {
			System.out.print("飲酒可能");
		}
	}
}

演習2：★
演習課題「間違い修正：入賞圏内か判別する」
右側のコードエリアのプログラムは、実行しても期待通りの動きをしていません。間違いの箇所を見つけてプログラムを完成させてください。

place の中には入賞判別したい人のレースの順位が、1〜12位までランダムな数値で代入されています。
例）5位だったら、5が代入されているものとします。

6位以上の場合は「●位入賞」と表示し、
7位以下だったら「●位入賞圏外」と表示するプログラムを書きましょう。


//7未満だったら、入賞と表示する
// if文による条件分岐　比較演算子
public class Main {
	public static void main(String[] args) {
		int place = (int)(Math.random() * 12+ 1);
		System.out.print(place + "位");
		// ここにif文を追加する
		if (place < 7) {
			System.out.println("入賞");
		} else {
			System.out.println("入賞圏外");
		}
	}
}


if文 条件分岐 比較演算子 else文 Java
04:おみくじを作ってみよう
04:おみくじを作ってみよう (5:03)
ここまで覚えたif文による条件分岐と、randomメソッドを使って、実行するたびに結果が変わる「おみくじプログラム」を作成してみましょう。
このチャプターを受講する
演習1：★
演習課題「大吉の確率を上げてみよう」
右のコードを完成させて、「大吉」か「大凶」を出力する、次のようなおみくじプログラムを作成してください。

- omikuji変数には、1から100までの値がランダムに代入されます。
- omikuji変数の値が30から100の場合は、「omikujiの中身は○○なので大吉」と表示
- omikuji変数の値が29以下の場合は、「omikujiの中身は○○なので大凶」と表示

例1: omikujiの中身は32なので大吉
例2: omikujiの中身は12なので大凶


// おみくじを作る
public class Main {
	public static void main(String[] args) {
		int omikuji = (int)(Math.random() * 100 + 1);  // randomメソッドについては次のチャプターで説明します
		if (omikuji >= 30) {
			System.out.println("omikujiの中身は" + omikuji + "なので大吉");
		} else {
			System.out.println("omikujiの中身は" + omikuji + "なので大凶");
		}
	}
}




if文 条件分岐 乱数 ランダムメソッド おみくじ ゲームプログラム Java
05:RPGのクリティカルヒットを再現
05:RPGのクリティカルヒットを再現 (2:24)
これまで覚えたif文による条件分岐と、randomメソッドを使って、RPGの戦闘シーンに出てくるようなクリティカルヒットをメッセージとして表示します。
このチャプターを受講する
演習1：★
 演習課題「追加攻撃の機能を実現しよう」
今回のチャプターで作成したプログラムに、次の機能を追加してください。

- 1か2が出目となる追加のサイコロをふる。
- 「追加のサイコロはX」と表示する。Xはサイコロの出目です。
- 追加のサイコロが1ならば、「追加攻撃!スライムに、10のダメージを与えた!!!」と表示する。
- 追加のサイコロが2ならば、「追加攻撃に失敗!」と表示する。


// RPGのクリティカルヒットを再現
// 比較演算子 == > < >= <= !=


// スライムと戦っている。
// 1から10のサイコロをふって、
// 6未満：サイコロの目だけダメージを与えたと表示。
// 6以上：クリティカルヒットとして、100のダメージを与えたと表示。
// さらに、1から2のサイコロをふって、
// 1：追加攻撃として、10のダメージを与えたと表示。
// 2：追加攻撃に失敗したと表示。
public class Main {
	public static void main(String[] args) {
		int hit = (int)(Math.random() * 10 + 1);
		if (hit < 6) {
			System.out.println("スライムに" + hit + "のダメージを与えた");
		} else {
			System.out.println("クリティカルヒット!スライムに、100のダメージを与えた!!");
		}

		int add = (int)(Math.random() * 2 + 1); // この行を修正して1から2のサイコロになるようにする
		System.out.println("追加のサイコロは、" + add);
		if (add == 1) { // この行の条件式を修正
			System.out.println("追加攻撃!スライムに、10のダメージを与えた!!!");
		} else {
			System.out.println("追加攻撃に失敗!");
		}
	}
}



if文 条件分岐 乱数 ランダムメソッド RPG ゲームプログラム Java
06:西暦から平成何年かを求めてみよう
06:西暦から平成何年かを求めてみよう (4:46)
このチャプターでは、入力しておいた西暦に応じて、平成何年か計算するプログラムを作成してみます。
このチャプターを受講する
演習1：★
演習課題「西暦年から昭和年を計算する」
右のコードは、実行するたびに1926年から1988年までの西暦年をランダムに選んで表示します。ここにコードを追加して、昭和年を計算し「西暦◎◎◎◎年は昭和XX年です。」と表示してください。

なお、昭和年は、「seireki - 1925」で求めることができます。



// 西暦年から昭和年を求める
public class Main {
	public static void main(String[] args) {
		int seireki = (int)(Math.random() * 63 + 1926);
		System.out.print("西暦" + seireki + "年は");

		// 昭和年を計算
		int showa = seireki - 1925;
		System.out.println("昭和" + showa + "年です。");
	}
}


日付処理 平成/西暦変換 Java
07:【補講】複数の条件を組み合わせてみよう - AND
07:【補講】複数の条件を組み合わせてみよう - AND (7:24)
ここでは、if文で、複数の条件を組み合わせるAND(アンド)について学習したいと思います。ANDを使うと、ひとつのif文で、複数の条件を組み合わせることができるんですよ。
このチャプターを受講する
演習1：★
演習課題「順位に合わせてメッセージを表示する」
右のコードは、実行するたびに、1から10までの数値をランダムに生成して、順位として表示します。ここにif文を追加して、2位から5位の時には「あと少し」と表示するようにしてください。

ifの条件を&&で組み合わせる
// 順位に合わせてメッセージを表示する

public class Main {
    public static void main(String[] args) {
        double rand = (Math.random() * 10) + 1;
        int number = (int) rand;
        System.out.println("あなたの順位は" + number + "位です");

        //　ここにifを追加する
        if (number >= 2 && number <=5) {
            System.out.println("あと少し");
        }
    }
}


if文 条件分岐 複数条件 AND Java
08:【補講】複数の条件を組み合わせてみよう - OR
08:【補講】複数の条件を組み合わせてみよう - OR (8:48)
ここでは、if文で、2つの条件を組み合わせるORについて学習します。
このチャプターを受講する
演習1：★
演習課題「不快指数」
右のコードは、実行するたびに、30から100までの数値をランダムに生成して、不快指数として表示します。ここにif文を追加して、55以下か70以上の時に「不快です」と表示するようにしてください。


//ifの条件を||で組み合わせる
// 不快指数
public class Main {
    public static void main(String[] args) {
        double rand = (Math.random() * 71) + 30;
        int discomfort = (int) rand;
        System.out.println("不快指数は" + discomfort + "です。");

        //　ここにifを追加する
        if (discomfort <= 55 || discomfort >= 70) {
            System.out.println("不快です");
        }
    }
}



if文 条件分岐 複数条件 OR Java
09:【補講】条件の評価結果を理解しよう
09:【補講】条件の評価結果を理解しよう (5:52)
ここでは、条件の評価結果について学習します。条件には、「成立したとき」と「成立しなかったとき」という状態がありますが、Javaでは、このような状態を表すため、論理型というデータ型を持っています。
このチャプターを受講する
演習1：★
演習課題「順位に合わせてメッセージを表示する」
右のコードは、実行するたびに、1から10までの数値をランダムに生成して、順位として表示します。そして、flag変数に、3位以内かどうかの評価結果を代入します。

ここにif文を追加して、flag変数がtrueの時に「入賞おめでとう」と表示するようにしてください。


//ifでflag変数を評価する
// 順位に合わせてメッセージを表示する

public class Main {
    public static void main(String[] args) {
        double rand = (Math.random() * 10) + 1;
        int number = (int) rand;
        System.out.println("あなたの順位は" + number + "位です");

        boolean flag = number <= 3;
        //　ここにifを追加する
        if (flag) {
            System.out.println("入賞おめでとう");
        }
    }
}



if文 条件分岐 複数条件 OR AND Boolean データ型 Java
10:【補講】データ型について理解しよう
10:【補講】データ型について理解しよう (7:39)
ここでは、Javaのデータ型について学習します。先ほどのレッスンでも、プログラムで文字列と数値を区別するデータ型について説明しましたよね。今回は、このデータ型について、さらに詳しく理解しましょう。
このチャプターを受講する
演習1：★
演習課題「文字列を数値に変換しよう」
右のコードは、「0.08」を文字として表示します。このnumber変数の値を数値に変換して出力してください。


//Double.parseDouble()メソッドで変換する
// 文字列を数値に変換しよう
public class Main {
    public static void main(String[] args) {
        String text = "0.08";
        System.out.println(Double.parseDouble(text));
    }
}

データ型 Integer Float Java
11:【補講】税込み金額を計算する
11:【補講】税込み金額を計算する (6:19)
ここでは、データ型を使った具体例として、商品の価格から割引価格や消費税込みの金額を計算します。15%オフの商品に、消費税8%を追加した場合を例にとり、小数点以下の数値をどのように扱うか学習しましょう。



演習課題「肉の量り売り」
右のコードは、100グラム128円の肉が、300グラムある場合の価格を計算しますが、正しく計算されません。間違いを修正して、肉の価格を出力してください。

//整数で割り算すると、小数点以下が切り捨てられる
// 肉の量り売り

public class Main {
    public static void main(String[] args) {
        int price = 128;
        int weight = 300;
        int amount = (int) (price / 100.0 * weight);
        System.out.println("100グラム" + price + "円の肉、" + weight + "グラムは、" + amount + "円です。");
    }
}




Java入門編3: ループ処理を学ぶ (全9回)
Javaを使って、同じ手順を繰り返すループ処理の基本を学びます。ループ処理は、大量のデータを処理するためには、欠かせないテクニックです。また今回は、プログラムの外部からデータを入力する方法についても取り上げます。
プログラミング学習 > Java入門編 > Java入門編3: ループ処理を学ぶ


01:条件によるくり返し処理1 - while
01:条件によるくり返し処理1 - while (5:52)
ここでは、数字を0から5まで表示させます。そのために、条件に合わせてループ処理するwhile（ワイル）という繰り返し命令について学習します。
このチャプターを受講する
演習1：★
 演習課題「「ハロー、paizaラーニング」と10回表示する」
右のコードは、「ハローpaizaラーニング」と表示するプログラムです。
whileを使って、「ハローpaizaラーニング」と10回出力するよう修正してください。


//whileで10回繰り返す
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
        int i = 0;
        while(i <= 9) {
            System.out.println("ハローpaizaラーニング");
            i = i + 1;
        }
    }
}


演習2：★
演習課題「数値を0から15まで表示する」
while命令を使って、0から15まで、数値を一行ずつ表示するプログラムを作成してください。

//whileで0から15まで繰り返す
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
        int i = 0;
        while(i <= 15) {
            System.out.println(i);
            i = i + 1;
        }
    }
}



while文 ループ Java
02:条件によるくり返し処理2 - while
02:条件によるくり返し処理2 - while (4:05)
ここではwhileを使ったループ処理について、もう少し学習します。そして、初期値や条件式を変更するとどうなるか試します。
このチャプターを受講する
演習1：★
演習課題「1から10までの偶数を表示する」
whileを使って、1から10までの偶数を一行ずつ表示するプログラムを作成してください。


//増分を2にして、2から10まで繰り返す
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
        int i = 2;
        while(i <= 10) {
            System.out.println(i);
            i = i + 2;
        }
    }
}

while文 ループ Java
03:RPGの攻撃シーンを作る
03:RPGの攻撃シーンを作る (5:34)
ここでは、数値を5から1までカウントダウン表示させるプログラムを作ります。そして、whileの具体例として、RPGの攻撃シーンのようなプログラムを作ってみましょう。
このチャプターを受講する
演習1：★
演習課題「数値を10から1までカウントダウン表示する」
whileを使って、10から1まで、数値を一行ずつカウントダウン表示するプログラムを作成してください。


//初期値を10、条件を1以上、増分を-1にする
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
        int i = 10;
        while(i >= 1) {
            System.out.println(i);
            i = i - 1;
        }
    }
}



演習2：★
演習課題「数値を20から10までカウントダウン表示する」
whileを使って、20から10まで、数値を一行ずつカウントダウン表示するプログラムを作成してください。

//初期値を20、条件を10以上、増分を-1にする
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
        int i = 20;
        while(i >= 10) {
            System.out.println(i);
            i = i - 1;
        }
    }
}


演習3：★
演習課題「数値を20から10までの奇数を表示する」
whileを使って、20から10までの奇数を一行ずつカウントダウン表示するプログラムを作成してください。


//初期値を19、条件を10以上、増分を-2にする
// whileによるループ処理
public class Main {
    public static void main(String[] args) {
		int i = 19;
		while(i >= 10) {
			System.out.println(i);
			i = i - 2;
		}
    }
}



RPG Java
04:0から5までを表示してみよう - for
04:0から5までを表示してみよう - for (5:21)
ここでは、for（フォー）という繰り返し命令について学習します。そのために、数字を0から4まで表示させてみましょう。
このチャプターを受講する
演習1：★
演習課題「「ハロー、paizaラーニング」を10回表示する」
右のコードは、「ハローpaizaラーニング」と表示するプログラムです。
for命令を使って、「ハローpaizaラーニング」と10回出力するよう修正してください。

//for命令で、10回繰り返す
// forによるループ処理
public class Main {
    public static void main(String[] args) {
        for(int i = 0; i <= 9; i++) {
            System.out.println("ハローpaizaラーニング");
        }
    }
}

演習2：★
演習課題「数値を0から15まで表示する」
for命令を使って、0から15まで、数値を一行ずつ表示する出力するプログラムを作成してください。


//forで0から15まで繰り返す
// forによるループ処理
public class Main {
    public static void main(String[] args) {
        for(int i = 0; i <= 15; i++) {
            System.out.println(i);
        }
    }
}


演習3：★
 演習課題「1月から12月まで表示する」
for命令を使って、1月から12月まで、一行ずつ表示する出力するプログラムを作成してください。


//for命令で1から12まで繰り返す
// forによるループ処理
public class Main {
    public static void main(String[] args) {
        for(int i = 1; i <= 12; i++) {
            System.out.println(i + "月");
        }
    }
}


for文 ループ Java
05:繰り返しでHTMLを作成する
05:繰り返しでHTMLを作成する (4:30)
ここでは、ループ処理の具体例として、HTMLのプルダウンメニューを作成します。そして、会員登録の入力フォームで、年齢を1歳から100歳まで選択できるようにしましょう。
このチャプターを受講する
演習1：★
標準入力 Java
08:複数データを読み込んでみよう
08:複数データを読み込んでみよう (5:11)
標準入力を使って、複数のデータを読み込む方法を学びます。そのために、標準入力にループ処理を組み合わせます。
このチャプターを受講する
演習1：★
演習課題「HTMLの箇条書き表示」
右のコードは、HTMLの箇条書きで1から3まで表示するプログラムです。
for命令を使って、箇条書きで1から100まで出力するよう修正してください。


//<li>要素を,for命令で繰り返し出力する
// HTMLによる箇条書き
public class Main {
    public static void main(String[] args) {
        System.out.println("<ul>");
        for(int i = 1; i <= 100; i++) {
            System.out.println("<li>" + i + "</li>");
        }
        System.out.println("</ul>");
    }
}





ループ for文 プルダウン Java
06:データの読み込み（標準入力）
06:データの読み込み（標準入力） (2:38)
ループ処理からちょっと離れて、プログラムの外部からデータを入力する標準入力について学習します。標準入力を使うと、ファイルのデータを読み込んだり、プログラムの実行時にデータを指定したりできます。
このチャプターを受講する





標準入力 Java
07:データを読み込んでみよう - 標準入力
07:データを読み込んでみよう - 標準入力 (4:20)
ここでは、実際に、Javaで標準入力から読み込むプログラムを作成します。標準入力を使うと、ファイルからデータを読み込んだり、プログラムの実行時にデータを受け取ったりできます。
このチャプターを受講する
演習1：★
演習課題「標準入力からテキストを取得する」
標準入力から文字列を1行取得して、テキストを出力するプログラムを作成してください。
読み込む文字列には、空白やタブは含まれません。
入力される値
勇者は荒野を歩いていた

 標準入力からの値取得方法はこちらをご確認ください

 期待する出力値
勇者は荒野を歩いていた

Scannerのnextで取得したデータをSystem.out.printlnする
// 標準入力
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String line = sc.next();
        System.out.println(line);
    }
}


演習2：★
演習課題「標準入力から数値を取得して計算する」
標準入力から整数データを1行取得して、100倍にした結果を出力するプログラムを作成してください。


//ScannerのnextIntで取得したint型データを、100倍してSystem.out.printlnする
// 標準入力
import java.util.*;

public class Main {
    public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int line = sc.nextInt();
	    System.out.println(line * 100);
    }
}


＃08:複数データを読み込んでみよう 
標準入力を使って、複数のデータを読み込む方法を学びます。そのために、標準入力にループ処理を組み合わせます。



 演習課題「同じテキストを指定回数出力する」
標準入力から整数が1つ与えられます。for命令を使って、その整数回分「スライムがあらわれた」と出力するプログラムを作成してください。
読み込んだ回数だけ、ループを繰り返す
// 標準入力とループ処理
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int count = sc.nextInt();
        for(int i = 0; i < count; i++) {
            System.out.println("スライムがあらわれた");
        }
    }
}


演習課題「標準入力とfor文の組み合せ」
標準入力で2つ（２行）の整数が与えられます。
1つ目の数値から２つ目の数値までを、1ずつ増加させながら、1行ずつ順番に出力するプログラムを作成してください。

入力した2つの数値を範囲にして、for文でループする
// 標準入力とループ処理
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        for(int i = num1; i <= num2; i++) {
            System.out.println(i);
        }
    }
}



演習課題「指定行数分、標準入力を取得する」
入力エリアの1行目にデータの個数が整数で示され、2行目以降に実際の文字列データが示されています。入力エリアからデータを取得して、2行目以降の文字列データを出力するプログラムを作成してください。
2行目以降の文字列データは、空白やタブは含まれません。


読み込んだ回数だけ、ループを繰り返す
// 標準入力とループ処理
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int count = sc.nextInt();

        String line;
        for(int i = 0; i < count; i++) {
            line = sc.next();
            System.out.println(line);
        }
    }
}



標準入力 Java
09:西暦年と平成年の対応表を作る
09:西暦年と平成年の対応表を作る (4:15)
ループ処理の具体例として、西暦年と平成年の対応表を作ります。
今回は、ひとつの年だけではなく、1989年から2016年まで全ての年を出力します。
このチャプターを受講する

演習課題「西暦年と昭和年の対応表を作ろう」
西暦年と昭和年の対応表を作成してください。対応表は、「西暦X年は昭和Y年です」と表示します。なお、昭和年は、西暦1926年から西暦1988年までの期間で、「西暦年 - 1925」で求めることができます。



1926から1988まで繰り返して、昭和年を求める
// 西暦年と昭和年の対応表
// 1926年から1988年までをループで出力
// ループ内で、各西暦年を昭和年に変換
public class Main {
    public static void main(String[] args) {
        int seireki, shouwa;
        for (seireki = 1926; seireki <= 1988; seireki++) {
            System.out.print("西暦" + seireki + "年は");
            shouwa = seireki - 1925;
            System.out.println("昭和" + shouwa + "年です");
        }
    }
}


演習課題「特定期間の西暦年と昭和年の対応表を作ろう」
標準入力から、1行目に西暦年、2行目に期間が与えられます。この西暦年から始まる、期間分の「西暦年と昭和年の対応表」を出力するプログラムを作成してください。
対応表の各行は、「西暦X年は昭和Y年です」と表示します。
昭和年は、西暦1926年から西暦1988年までで、「西暦年 - 1925」で求めることができます。
なお。与えられる西暦年は、昭和年に対応しています。上の方法で求めた昭和年は、正しい昭和年(昭和1年から昭和63年)になります。


//西暦年から西暦年+期間-1まで繰り返して、昭和年を求める
// 特定期間の西暦年と昭和年の対応表を作る
// 1行目：開始年
// 2行目：期間
// 昭和年 = 西暦年 - 1925
// 出力：西暦X年は昭和Y年です

import java.util.*;

public class Main {
    public static void main(String[] args) {
        int seireki, shouwa;
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt();
        int term = sc.nextInt();

        int stop = start + term - 1;
        for (seireki = start; seireki <= stop; seireki++) {
            System.out.print("西暦" + seireki + "年は");
            shouwa = seireki - 1925;
            System.out.println("昭和" + shouwa + "年です");
        }
    }
}




Java入門編4:配列の基礎 (全9回)
大規模なデータを扱うプログラムを作るときに必要になる配列について学びます。
プログラミング学習 > Java入門編 > Java入門編4:配列の基礎
Bランクレベルアップセット
練習問題セットにチャレンジしよう！
ここまでの学習内容で、スキルチェックのD問題にチャレンジすることができます。まずは練習問題を解いて、本問題への自信をつけましょう。
練習問題セットは段階的にプログラミングをすることができるため、順番に解くことで、難易度の高い問題が解けるようになっています。



01:配列とは何かを学ぼう
01:配列とは何かを学ぼう (3:36)
ここでは、プログラミング言語Javaを使って、大規模なデータを扱うプログラムを作るときに必要になる配列について、基本的な考え方を学習しましょう。
このチャプターを受講する
配列 Java
02:配列を作ろう
02:配列を作ろう (4:12)
ここでは、配列の基本操作について学びます。そして、Javaを使って、配列の作成、表示、代入といった機能を試してみましょう。
このチャプターを受講する
演習1：★
演習課題「配列の中身を出力してみよう」
右のコードには、配列が定義されています。
この配列をprintlnメソッドを使って出力してください。


//printlnメソッドでarrayを出力
// 配列の中身を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[] array = {"戦士","侍","僧侶","魔法使い"};
        // この下で、arrayを出力してみよう
        System.out.println(array[0]);
        System.out.println(array[1]);
        System.out.println(array[2]);
        System.out.println(array[3]);
    }
}


演習2：★
演習課題「指定の文字を配列にしてみよう」
item という配列に、下記の要素をこの並び順で代入して、
printlnメソッドで出力をしてください。

「ロングソード」
「ブレードソード」
「エクスカリバー」



//波カッコで配列を定義する
// 指定の文字を配列にする
public class Main {
    public static void main(String[] args) {
        String item[] = {"ロングソード", "ブレードソード", "エクスカリバー"};
        System.out.println(item[0]);
        System.out.println(item[1]);
        System.out.println(item[2]);
    }
}


//配列作成時に、変数を指定する
// 変数で、配列に代入する

public class Main {
    public static void main(String[] args) {
        String player_1 = "勇者";
        String player_2 = "魔法使い";
        String player_3 = "戦士";
        // player_1 ~ 3を、配列に代入して、printlnメソッドで出力してください。
        String team[] = {player_1, player_2, player_3};
        System.out.println(team[0]);
        System.out.println(team[1]);
        System.out.println(team[2]);
    }
}


演習3：★
 演習課題「変数で、配列に代入しよう」
右のコードには、player_1, player_2, player_3という変数に、文字列が代入されています。
このplayer_1 ~ 3を、この順番で配列に代入して、printlnメソッドで出力してください。


// 配列作成時に、変数を指定する
// 変数で、配列に代入する

public class Main {
    public static void main(String[] args) {
        String player_1 = "勇者";
        String player_2 = "魔法使い";
        String player_3 = "戦士";
        // player_1 ~ 3を、配列に代入して、printlnメソッドで出力してください。
        String team[] = {player_1, player_2, player_3};
        System.out.println(team[0]);
        System.out.println(team[1]);
        System.out.println(team[2]);
    }
}


配列 Java
03:配列の要素を取り出してみよう
03:配列の要素を取り出してみよう (5:08)
ここでは、配列の要素をいろいろな方法で取り出してみます。配列では、インデックスと呼ばれる番号を使って要素を取り出します。また、そのインデックスを変数で指定したり、計算して指定できます。
このチャプターを受講する
演習1：★
演習課題「配列から最初の要素を取り出してみよう」
右のコードエリアには、5つの要素を持つ配列が定義されています。
この配列の最初の要素(インデックスが0の要素)をprintlnメソッドで出力してください。


//最初の要素なので、インデックスが0の要素を出力する
// 配列から特定要素を取り出す
public class Main {
    public static void main(String[] args) {
        String[] team = {"勇者", "戦士", "侍", "忍者", "魔法使い"};
        // teamの1番左の要素をprintlnメソッドで出力する
        System.out.println(team[0]);
    }
}


演習2：★
演習課題「配列から特定要素を取り出してみよう」
右のコードエリアには、5つの要素を持つ配列が定義されています。
この配列のインデックスが2の要素をprintlnメソッドで出力してください。


// インデックスが2の要素を出力する
// 配列から特定要素を取り出す
public class Main {
    public static void main(String[] args) {
        String[] team = {"勇者", "戦士", "侍", "忍者", "魔法使い"};
        // teamのインデックス 2の要素をprintlnメソッドで出力する
        System.out.println(team[2]);
    }
}

配列 Java
04:ループで配列を処理しよう
04:ループで配列を処理しよう (3:34)
ここでは、ループ処理で配列を扱ってみたいと思います。そして、Javaのfor命令と配列を組み合わせます。
このチャプターを受講する
演習1：★
演習課題「配列の中身を1行ずつ表示してみよう」
右のコードエリアには、RPGの敵が、enemy配列で定義されています。
この配列から要素を順に取り出して、「＊＊が現れた」と出力してください。


// forで、配列から要素を取り出す
// 配列の中身をループで表示する
public class Main {
    public static void main(String[] args) {
        String[] enemy = {"スライム", "モンスター", "ゾンビ", "ドラゴン", "魔王"};
        // ここに、要素をループで表示するコードを記述する
        for (int i = 0; i < enemy.length; i++) {
            System.out.println(enemy[i] + "が現れた");
        }
    }
}


演習2：★
 演習課題「要素を合計を計算してみよう」
右のコードエリアでは、numbers配列に数値が格納されています。
この全要素の合計値を計算して出力してください。

// ループの中で、取り出した要素をsumに足していく
// 要素を合計を計算する

public class Main {
    public static void main(String[] args) {
        int[] numbers = {12, 34, 56, 78, 90};
        int sum = 0;
        for (int i = 0; i < numbers.length; i++) {
            // ここに、合計を計算するコードを記述する
            sum += numbers[i];
        }
        System.out.println(sum);
    }
}


配列 Java
05:ループで配列を処理しよう2
05:ループで配列を処理しよう2 (3:23)
ここでは、ループ処理の拡張for文で配列を出力します。ここまでループ処理では、for文を使ってきましたが、Javaでは拡張for文も幅広く使われているんですよ。
このチャプターを受講する
演習1：★
 演習課題「配列の中身を1行ずつ表示してみよう」
右のコードエリアには、RPGの敵が、enemy配列で定義されています。
拡張forで、この配列から要素を順に取り出して、「＊＊が現れた」と出力してください。


// for(String i : enemy)で、配列から要素を取り出す
// 配列の中身をループで表示する
public class Main {
    public static void main(String[] args) {
        String enemy[] = {"スライム", "モンスター", "ゾンビ", "ドラゴン", "魔王"};
        // ここに、要素をループで表示するコードを記述する
        for (String i : enemy) {
            System.out.println(i + "が現れた");
        }
    }
}


演習2：★
演習課題「要素を合計を計算してみよう」
右のコードエリアでは、numbers配列に数値が格納されています。
拡張forで、この全要素の合計値を計算して出力してください。


// ループの中で、取り出した要素をsumに足していく
// 要素を合計を計算する
public class Main {
    public static void main(String[] args) {
        int numbers[] = {12, 34, 56, 78, 90};
        int sum = 0;
        for (int i : numbers) {
            // ここに、合計を計算するコードを記述する
            sum += i;
        }
        System.out.println(sum);
    }
}

配列 Java
06:ArrayListクラスを使おう
06:ArrayListクラスを使おう (4:08)
ここでは、Javaの配列をパワーアップするため、ArrayListクラスについて学習します。ArrayListクラスは、配列の要素数を後から変更することができるなど便利な機能を持っています。
このチャプターを受講する
演習1：★
演習課題「ArrayListに要素を追加してみよう」
右のコードエリアには、weaponというArrayListが定義されています。
このArrayListに「木の棒」「鉄の剣」「石斧」という要素を追加してください。


// weaponに .addで追加する
// ArrayListに要素を追加する
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> weapon = new ArrayList<String>();
        // ここに、要素を追加するコードを記述する
        weapon.add("木の棒");
        weapon.add("鉄の剣");
        weapon.add("石斧");
        for (String item : weapon) {
            System.out.println(item);
        }
    }
}



演習2：★
演習課題「ArrayListの要素を上書きしてみよう」
右のコードエリアには、3つの要素を持つweaponというArrayListが定義されています。
このArrayListのインデックス2の要素を、「石斧」に書き換えてください。

// weaponに .setで更新する
// ArrayListの要素を上書きする
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> weapon = new ArrayList<String>();
        weapon.add("木の棒");
        weapon.add("鉄の剣");
        weapon.add("サビた剣");
        // ここに、要素を上書きするコードを記述する
        weapon.set(2, "石斧");
        for (String item : weapon) {
            System.out.println(item);
        }
    }
}

演習3：★
 演習課題「ArrayListから要素を削除してみよう」
右のコードエリアには、4つの要素を持つweaponというArrayListが定義されています。
このArrayListから、インデックス2の要素を削除してください。


// weaponから .removeで更新する
// ArrayListの要素を削除する
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> weapon = new ArrayList<String>();
        weapon.add("木の棒");
        weapon.add("鉄の棒");
        weapon.add("鉄の剣");
        weapon.add("銅の剣");
        // ここに、要素を削除するコードを記述する
        weapon.remove(2);
        for (String item: weapon) {
            System.out.println(item);
        }
    }
}


演習4：★
演習課題「ArrayListの要素数を出力してみよう」
右のコードエリアには、weaponというArrayListが定義されています。
このArrayListの要素数を出力してください。


// weapon.size()を出力する
// ArrayListの要素の個数を出力する
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> weapon = new ArrayList<String>();
        weapon.add("木の棒");
        weapon.add("鉄の棒");
        weapon.add("鉄の剣");
        weapon.add("石斧");
        weapon.add("エクスカリバー");
        // ここに、要素数を出力するコードを記述する
        System.out.println(weapon.size());
    }
}


配列 Java
07:splitで文字列を分割しよう
07:splitで文字列を分割しよう (3:59)
ここでは、標準入力から取り込んだデータを配列に格納する方法を学びます。そのために、カンマで区切られた1行データを、区切りごとに分割して配列に格納します。
このチャプターを受講する
演習1：★
演習課題「文字列をカンマで分割してみよう」
右のコードエリアには、team_strという文字列に、RPGのプレイヤーが、カンマで区切られて代入されています。
この文字列を、splitメソッドを使って カンマのところで分割してください。


// 文字列を .split(",")で分割する
// 文字列をカンマで分割する
public class Main {
    public static void main(String[] args) {
        String team_str = "勇者,戦士,忍者,魔法使い";
        // ここに文字列を分割するコードを記述する
        String[] team_array = team_str.split(",");
        for (String s : team_array) {
            System.out.println(s);
        }
    }
}

演習2：★
演習課題「英文の単語数を数えよう」
右のコードエリアには、ある英文がstrという文字列に代入されています。
この文字列を、splitメソッドを使って、スペースのところで分割して、単語の数を出力してください。


// 文字列を .split(" ")で分割し、要素数をlengthメソッドで出力する
// 英文の単語数を数える
public class Main {
    public static void main(String[] args) {
        String str = "One cold rainy day when my father was a little boy he met an old alley cat on his street";
        // ここに文字列を分割するコードを記述する
        int count = str.split(" ").length;
        System.out.println(count);
    }
}


演習3：★

演習課題「標準入力から読み込んだURLを分割しよう」
右のコードエリアのプログラムは、入力エリアのURLを読み込みます。
読み込んだURLを「/」で分割して、配列の各要素をprintlnメソッドで出力してください。


//文字列を .split("/")で分割する
// 標準入力から読み込んだURLを分割する
// https://paiza.jp/cgc/users/ready
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String url_str = sc.next();
        // ここに文字列を分割するコードを記述する
        String[] url = url_str.split("/");
        for (String s : url) {
            System.out.println(s);
        }
    }
}


配列 csv 文字列分割 Java
08:配列に複数行データを読み込んでみよう
08:配列に複数行データを読み込んでみよう (3:56)
ここでは、標準入力から読み込んだ複数の行データを配列に格納します。その時に、読み込む行数が事前に分からなくても、きちんと対応できるようにしましょう。
このチャプターを受講する
演習1：★
演習課題「標準入力から読み込んだ複数行を出力しよう」
右のコードエリアのプログラムは、RPGの敵の名前を、入力エリアから複数行データとして読み込んで出力します。
この文字列を、「＊＊が現れた」という形式で出力してください。


//"が現れた"という文字列を結合する
// 読み込んだ複数行を出力する
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            System.out.println(line + "が現れた");
        }
    }
}



演習2：★
演習課題「読み込んだ複数行のカンマ区切りデータを出力しよう」
右のコードエリアのプログラムは、入力エリアから複数行データとして読み込みます。
入力エリアには、RPGの敵の名前Aと匹数Bが、カンマ区切りで用意してあります。
読み込んだデータをカンマで分割して、「AがB匹現れた」と出力してください。


// enemy[0] + "が" + enemy[1] + "匹現れた"、文字列を結合する
// 複数行のカンマ区切りデータを出力する
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            // ここに、文字列を分割して、出力するコードを書く
            String[] enemy = line.split(",");
            System.out.println(enemy[0] + "が" + enemy[1] + "匹現れた");
        }
    }
}


配列 標準入力 文字列分割 Java
09:配列を使ったランダムくじ
09:配列を使ったランダムくじ (5:07)
ここでは、配列を使って、RPGの戦闘シーンのようなメッセージを表示するプログラムを作ります。



演習課題「おみくじを作ろう」
入力エリアに、おみくじの出目(例：大吉,中吉,吉,凶)が用意してあります。
右のコードエリアに、おみくじプログラムを作ってください。
おみくじは、標準入力から読み込んだ文字列をカンマで分割して、そのうち1つをランダムに出力します。



// Math．randomメソッドの要素数倍して、その数をインデックスにした配列を出力する
// おみくじプログラム
import java.util.*;
public class Main {
    public static void main(String[] args) {
        // 標準入力から1行取得
        Scanner sc = new Scanner(System.in);
        String line = sc.nextLine();

        // カンマで分割して、配列に代入
        String[] omikuji = line.split(",");

        // 配列の要素をランダムに選ぶ
        double rand = Math.random() * omikuji.length;
		int num = (int)rand;

        // ランダムに選んだ配列の要素を出力
        System.out.println(omikuji[num]);
    }
}


Java入門編5: 2次元配列を理解しよう (全11回)
Javaでの2次元配列の基礎について学び、配列のループ処理について理解を深めます。
プログラミング学習 > Java入門編 > Java入門編5: 2次元配列を理解しよう

演習課題「じゃんけんプログラムを作ろう」
入力エリアに、じゃんけんの手(例：グー,チョキ,パー)が用意してあります。
右のコードエリアのコメントを参考にして、じゃんけんプログラムを作ってください。
じゃんけんの手は、標準入力から読み込んだ文字列をカンマで分割して、そのうち1つをランダムに出力します。


// Math．randomメソッドの要素数倍して、その数をインデックスにした配列を出力する
// じゃんけんプログラム
import java.util.*;
public class Main {
    public static void main(String[] args) {
        // 標準入力から1行取得
        Scanner sc = new Scanner(System.in);
        String line = sc.next();

        // カンマで分割して、配列に代入
        String[] janken = line.split(",");

        // 配列の要素をランダムに選ぶ
        double rand = Math.random() * janken.length;
        int hand = (int)rand;

        // ランダムに選んだ配列の要素を出力
        System.out.println(janken[hand]);
    }
}

01:多次元配列の概要 (3:13)
ここでは、プログラミング言語のJavaを使って、2つのインデックスで要素を指定する2次元配列について、基本的な考え方を学習しましょう。2次元配列を使うと、複雑なデータを操作できるようになります。
このチャプターを受講する
2次元配列 Java
02:2次元配列を作成する
02:2次元配列を作成する (5:36)
ここでは、Javaを使って、実際に2次元配列を作成してみましょう。例として、2次元配列を作成して、そこから要素を表示します。
このチャプターを受講する
演習1：★
演習課題「2次元配列を作成してみよう」
右のコードには、item1, item2, item3というStringの配列があります。
このitem1, item2, item3を、この順番でbasket配列の要素にしてください。


// 2次元配列を作成してみよう
public class Main {
    public static void main(String[] args) {
        String[] item1 = {"木の棒", "こん棒"};
        String[] item2 = {"おにぎり", "おにぎり"};
        String[] item3 = {"毒消し", "薬草"};

        // item1 ~ 3を、basket配列に代入してください。


        System.out.println(basket[0][0]);
        System.out.println(basket[0][1]);
        System.out.println(basket[1][0]);
        System.out.println(basket[1][1]);
        System.out.println(basket[2][0]);
        System.out.println(basket[2][1]);
    }
}


演習2：★
演習課題「配列の中身を出力してみよう」
右のコードには、配列が定義されています。
printlnメソッドを使って、この配列の要素を全て出力してください。

// printlnメソッドでarrayをひとつずつ出力
// 配列の中身を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[][] array = {{"勇者", "忍者"}, {"武士", "戦士"}, {"僧侶", "魔法使い"}};

        // この下で、arrayの全ての要素を出力してみよう
        System.out.println(array[0][0]);
        System.out.println(array[0][1]);
        System.out.println(array[1][0]);
        System.out.println(array[1][1]);
        System.out.println(array[2][0]);
        System.out.println(array[2][1]);
    }
}

2次元配列 Java
03:2次元配列を操作する
03:2次元配列を操作する (5:03)
ここでは、2次元配列の基本操作を学習します。配列の要素を更新したり、長さを調べたりしてみましょう。
このチャプターを受講する
演習1：★
演習課題「2次元配列の要素を更新する」
右のコードエリアには、basket配列が定義されています。
この配列の「こん棒」を、「石斧」に書き換えてください。


// basket[0][1]に代入する
// 2次元配列の要素を更新する
public class Main {
    public static void main(String[] args) {
        String[][] basket = {{"木の棒", "こん棒"}, {"おにぎり", "おにぎり"}, {"毒消し", "薬草"}};

        // ここに、要素を更新するコードを記述する
        basket[0][1] = "石斧";

        System.out.println(basket[0][0]);
        System.out.println(basket[0][1]);
        System.out.println(basket[1][0]);
        System.out.println(basket[1][1]);
        System.out.println(basket[2][0]);
        System.out.println(basket[2][1]);
    }
}



演習2：★
演習課題「2次元配列の要素の個数を出力する」
右のコードエリアには、basket配列が定義されています。
この配列のインデックス1の要素数を出力してください。


// basket[1]の要素数を出力する
// 2次元配列の要素の個数を出力する
public class Main {
    public static void main(String[] args) {
        String[][] basket = {{"木の棒", "こん棒"}, {"おにぎり", "おにぎり"}, {"毒消し", "薬草"}};

        // ここに、個数を出力するコードを記述する
        System.out.println(basket[1].length);
    }
}


2次元配列 Java
04:2次元配列をループで処理する
04:2次元配列をループで処理する (4:09)
ここでは、2次元配列をループを使って処理する方法について、理解を深めます。
たくさんのデータを持つ配列を処理するには、ループ処理が欠かせませんし、2次元配列を使う時にも活躍します。
このチャプターを受講する
演習1：★
演習課題「ループで2次元配列を出力してみよう」
右のコードには、2次元配列が定義されています。
この配列をforを使って出力してください。

// 2重のforループで、arrayを出力
// ループで2次元配列を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[][] array = {{"勇者", "忍者"}, {"武士", "戦士"}, {"僧侶", "魔法使い"}};

        // この下で、forで、arrayを出力してみよう
        for (int i = 0; i < array.length; i++) {
            for (int j = 0;  j < array[i].length; j++) {
                System.out.println(array[i][j]);
            }
        }
    }
}


演習2：★
 演習課題「拡張forで2次元配列を出力してみよう」
右のコードには、2次元配列が定義されています。
この配列をprintlnメソッドを使って出力してください。



// 2重の拡張forの中で、playerを出力
// 拡張forで2次元配列を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[][] array = {{"勇者", "忍者"}, {"武士", "戦士"}, {"僧侶", "魔法使い"}};

        for (String[] team : array) {
            for (String player : team) {
                // この下で、arrayの要素を出力してみよう
                System.out.println(player);
            }
        }
    }
}


2次元配列 Java
05:2次元配列をnewで作成する
05:2次元配列をnewで作成する (4:42)
ここでは、新しい配列を作るnewメソッドを使って、2次元配列を作成してみましょう。また、配列の初期化についても説明します。
このチャプターを受講する
演習1：★
演習課題「2次元配列をnewで作成しよう」
右のコードエリアで、newキーワードを使って、次のような配列を作成してください。

・配列名は、array
・要素のデータ型は、int
・2 x 3の2次元配列


// newメソッドで[2][3]の配列を作成
// 2次元配列をnewで作成しよう
public class Main {
    public static void main(String[] args) {

        // この下で、配列を作成しよう
        int[][] array = new int[2][3];

        for (int[] item : array) {
            for (int num : item) {
                System.out.print(num);
            }
            System.out.println("");
        }
    }
}




演習2：★
 演習課題「2次元配列の初期値を指定しよう」
右のコードには、2次元配列を作成して、ループで出力しています。
この配列の初期値を、全て1にして出力してください。


// ループの中で、arrayに1を代入する
// 2次元配列の初期値を指定しよう
public class Main {
    public static void main(String[] args) {

        int[][] array = new int[2][3];

        for (int i = 0; i < array.length; i++) {
            for (int j = 0;  j < array[i].length; j++) {
                //この下で、初期値を指定する
                array[i][j] = 1;
                System.out.print(array[i][j]);
            }
            System.out.println("");
        }
    }
}

2次元配列 Java
06:ドット絵を表示する
06:ドット絵を表示する (3:11)
ここでは、2次元配列の具体例として、簡単なドット絵を表示してみましょう。元になるイラストのドットの有無を、数字のゼロイチで表して、テキストで表示します。
このチャプターを受講する
演習1：★
演習課題「ドットで文字を出力しよう」
右のコードエリアには、「A」という文字が、letterAという2次元配列で定義されています。
この配列から要素を順に取り出して、ドットで文字を出力してください。
この時、要素が1だったら「@」(半角アットマーク)、ゼロだったら「 」(半角スペース)を出力します。


// 2次元配列から2重ループで要素を取り出す
// ドットで文字を出力しよう
public class Main {
    public static void main(String[] args) {

        int[][] letterA =
            {{0,0,1,1,0,0},
             {0,1,0,0,1,0},
             {1,0,0,0,0,1},
             {1,1,1,1,1,1},
             {1,0,0,0,0,1},
             {1,0,0,0,0,1}};

        // ここに、ドットを表示するコードを記述する
        for (int[] line : letterA) {
            for (int dot : line) {
                if (dot == 1) {
                    System.out.print("@");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println("");
        }
    }
}


2次元配列 ドット絵 Java
07:3次元配列で複数のドット絵を表示する
07:3次元配列で複数のドット絵を表示する (4:07)
ここでは、複数のドット絵を表示するために、3次元配列を使ってみます。ドット絵のパターンごとに、配列を切り替えて表示してみましょう。
このチャプターを受講する
演習1：★

演習課題「ドットで文字を出力しよう」
右のコードエリアには、「A」「B」「C」という文字が、lettersという3次元配列で定義されており、そのうちの「A」の文字を出力するコードがあります。
この配列から、3文字とも出力してください。
「A」「B」「C」の各文字の間には、1行空行を挿入してください。


//外側にループを追加する
// ドットで文字を出力しよう
public class Main {
    public static void main(String[] args) {

        int[][][] letters =
            {{{0,0,1,1,0,0},
             {0,1,0,0,1,0},
             {1,0,0,0,0,1},
             {1,1,1,1,1,1},
             {1,0,0,0,0,1},
             {1,0,0,0,0,1}},
            {{1,1,1,1,1,0},
             {1,0,0,0,0,1},
             {1,1,1,1,1,0},
             {1,0,0,0,0,1},
             {1,0,0,0,0,1},
             {1,1,1,1,1,0}},
            {{0,1,1,1,1,0},
             {1,0,0,0,0,1},
             {1,0,0,0,0,0},
             {1,0,0,0,0,0},
             {1,0,0,0,0,1},
             {0,1,1,1,1,0}}};

        // ここに、ドットを表示するコードを記述する
        for (int[][] letter : letters) {
            for (int[] line : letter) {
                for (int dot : line) {
                    if (dot == 1) {
                        System.out.print("@");
                    } else {
                        System.out.print(" ");
                    }
                }
                System.out.println("");
            }
            System.out.println("");
        }
    }
}








2次元配列 3次元配列 Java
08:2次元配列で地図を表示する１
08:2次元配列で地図を表示する１ (4:21)
ここでは、2次元配列の具体的な例として、RPGの簡単な地図を作ってみましょう。マス目の位置に合わせて、城と町の間を道路で接続します。
このチャプターを受講する
演習1：★


演習課題「模様を出力してみよう」
右のコードは、2次元配列を使って、縦に5個、横に10個の「.」を四角く出力します。
このコードを修正して、四角の4つのコーナーに「.」の代わりに「+」を出力してください。


//4つのコーナーに当たる配列の初期値を「+」にする。
// 模様を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[][] areaMap = new String[5][10];
        // この下で、2次元配列の初期値を設定する
        areaMap[0][0] = "+";
        areaMap[0][9] = "+";
        areaMap[4][0] = "+";
        areaMap[4][9] = "+";

        for (int i = 0; i < areaMap.length; i++) {
            for (int j = 0; j < areaMap[i].length; j++) {
                if (areaMap[i][j] == null) {
                    areaMap[i][j] = ".";
                }
                System.out.print(areaMap[i][j]);
            }
            System.out.println("");
        }
    }
}

2次元配列 Java
09:2次元配列で地図を表示する２
09:2次元配列で地図を表示する２ (3:41)
ここでは、前回に引き続いて、RPGの簡単なマップを作って、城と町の間を道路で接続します。
このチャプターを受講する
演習1：★
演習課題「模様を出力してみよう」
右のコードは、2次元配列を使って、縦に5個、横に10個の「.」を出力します。
コードを修正して、この2次元配列のインデックスがどちらも2で割り切れる場合は、「.」の代わりに「+」を出力してください。


//「インデックスの余りがゼロの場合」という条件の論理積(&&)を取ります
// 模様を出力してみよう
public class Main {
    public static void main(String[] args) {
        String[][] areaMap = new String[5][10];

        for (int i = 0; i < areaMap.length; i++) {
            for (int j = 0; j < areaMap[i].length; j++) {
                if (i % 2 == 0 && j % 2 == 0) {
                    areaMap[i][j] = "+";
                } else {
                    areaMap[i][j] = ".";
                }
                System.out.print(areaMap[i][j]);
            }
            System.out.println("");
        }
    }
}


2次元配列 Java
10:標準入力から2次元配列
10:標準入力から2次元配列 (5:06)
ここでは、標準入力から2次元配列を読み込んでみます。複数行のデータを用意して、それを2次元配列に割り当てます。
このチャプターを受講する
演習1：★
 演習課題「標準入力から文字のドットデータを読み込む」
「A」という文字のドットデータを標準入力から読み込むコードがあります。
このデータを2次元配列に格納してください。

このコードは、最初にドットデータの縦と横のサイズを、nとmに読み込みます。


//2重のforループで、2次元配列に代入する
// 標準入力から文字のドットデータを読み込む
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int m = sc.nextInt();

        int[][] table = new int[n][m];
        // ここに、標準入力から2次元配列に代入するコードを書く
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                table[i][j] = sc.nextInt();
            }
        }

        // 2次元配列から文字を出力
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (table[i][j] == 1) {
                    System.out.print("#");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println("");
        }
    }
}


2次元配列 Java
11:2次元配列で画像を配置
11:2次元配列で画像を配置 (4:29)
ここでは、2次元配列に合わせて、RPGのキャラクターを配置して表示してみましょう。
将棋のコマの初期状態のような感じで、画像を表示してみましょう。


演習課題「2次元配列で画像を表示する」
右のコードエリアには、画像用配列playerImagesとキャラクター配置用の配列characterMapが定義されており、HTMLとしてcharacterMapの値を出力します。
このコードを修正して、characterMapの値をインデックスとして、players_imageで画像を出力してください。



//<img src = ' '>で出力する画像ファイルのURLを、players_imageで指定する
// 2次元配列で画像を表示する
public class Main {
    public static void main(String[] args) {

        //画像URL用の配列
        String[] playerImages = {
            "https://paiza-webapp.s3.amazonaws.com/files/learning/rpg/Empty.png",
            "https://paiza-webapp.s3.amazonaws.com/files/learning/rpg/Dragon.png",
            "https://paiza-webapp.s3.amazonaws.com/files/learning/rpg/Crystal.png",
            "https://paiza-webapp.s3.amazonaws.com/files/learning/rpg/Hero.png",
            "https://paiza-webapp.s3.amazonaws.com/files/learning/rpg/Heroine.png"};

        //キャラクター配置用の配列
        int[][] characterMap = {{1,1,1,1,1},
                                {2,3,3,3,2},
                                {2,4,4,4,2}};

        System.out.println("<table>");
        for (int[] line: characterMap) {
            System.out.println("<tr>");
            for (int imageId: line) {
                System.out.print("<td><img src='" + playerImages[imageId] + "'></td>");
            }
            System.out.println("</tr>");
        }
        System.out.println("</table>");
    }
}


Java入門編6: メソッドを理解しよう (全6回)
Javaのメソッドについて、その呼び出し方や作り方など、基本機能を学習します。
プログラミング学習 > Java入門編 > Java入門編6: メソッドを理解しよう
Bランクレベルアップセット
練習問題セットにチャレンジしよう！
ここまでの学習内容で、スキルチェックのC問題にチャレンジすることができます。まずは練習問題を解いて、本問題への自信をつけましょう。
練習問題セットは段階的にプログラミングをすることができるため、順番に解くことで、難易度の高い問題が解けるようになっています。




01:メソッドについて学習しよう (2:07)
ここでは、プログラミング言語Javaのメソッドについて学習します。メソッドの作り方と呼び出し方を理解していきましょう。
このチャプターを受講する
メソッド Java
02:メソッドを作ろう
02:メソッドを作ろう (3:27)
ここでは、プログラミング言語Javaのメソッドの作り方を学習します。そして、実際にメソッドを定義して、呼び出してみます。
このチャプターを受講する
演習1：★
演習課題「メソッドを呼び出してみよう」
右のコードには、メッセージを表示するsayHelloメソッドが定義されています。
mainメソッドから、このメソッドを呼び出して、メッセージを表示してください。


//say_hello()メソッドを呼び出す
// メソッドを呼び出してみよう
public class Main {
    public static void main(String[] args) {
        //この下にメソッド呼び出しを記述する
        sayHello();
    }

    public static void sayHello() {
        System.out.println("hello paiza");
    }
}

演習2：★
演習課題「メソッドを作成してみよう」
右のコードには、sayHelloメソッドを呼び出していますが、メソッドの処理が記述されていません。
以下のテキストを表示するよう、メソッドにコードを追加してください。

//sayHelloメソッドで、テキストを出力する
// メソッドを作成してみよう
public class Main {
    public static void main(String[] args) {
        sayHello();
    }

    public static void sayHello() {
        //この下にメソッド内の処理を記述する
        System.out.println("hello java");
    }
}


演習3：★
say_helloメソッドは、class Mainの波カッコの中に書く
// 間違い探し

public class Main {
    public static void main(String[] args) {
        sayHello();
    }

    public static void sayHello() {
        System.out.println("hello paiza");
    }
}
メソッド 命名規則 Java
03:引数と戻り値を追加しよう
03:引数と戻り値を追加しよう (5:23)
ここでは、プログラミング言語Javaの引数と戻り値について学習します。そして、メソッドを定義する時、引数と戻り値をどんなふうに記述するのか理解しましょう。
このチャプターを受講する
演習1：★
演習課題「掛け算メソッドを呼び出してみよう」
右のコードには、2つの引数を掛け算するmultiメソッドが定義されています。
このメソッドを呼び出して、「33ｘ44」の計算結果を表示してください。


//33と44を引数にして、multiメソッドを呼び出す
// 掛け算メソッドを呼び出してみよう

public class Main {
    public static void main(String[] args) {
        //この下にメソッド呼び出して、出力する
        int num = multi(33, 44);
        System.out.println(num);
    }

    public static int multi(int x, int y) {
        return x * y;
    }
}

演習2：★
演習課題「掛け算メソッドを作成してみよう」
右のコードには、multiメソッドを呼び出していますが、メソッドの処理が記述してありません。
xとyの二つの引数を掛け算した結果を返すよう、メソッドにコードを追加してください。


//returnの後に、計算式を記述する
// 掛け算メソッドを作成してみよう
public class Main {
    public static void main(String[] args) {
        System.out.println(multi(3, 4));
        System.out.println(multi(5, 7));
        System.out.println(multi(12, 34));
    }

    public static int multi(int x, int y) {
        // この下に処理を記述する
        return x * y;
    }
}


演習3：★
演習課題「九九の表を作成してみよう」
右のコードは、九九の2の段を出力するプログラムです。
このプログラムを修正して、九九を1の段から9の段まで出力してください。
各段は、行末で改行してください。



//forループを追加して、1の段から9の段まで出力する
// 九九の表を作成してみよう
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 9; i++) {
            for (int num = 1; num <= 9; num++) {
                System.out.print(multi(i, num));
                if (num < 9) {
                    System.out.print(", ");
                } else {
                    System.out.println("");
                }
            }
        }
    }

    public static int multi(int x, int y) {
        return x * y;
    }
}


メソッド 引数 戻り値 Java
04:スコープを理解しよう
04:スコープを理解しよう (5:17)
ここでは、変数の有効範囲であるスコープについて学習します。スコープは、メソッド定義やループ処理を使いこなすため重要な機能ですので、しっかりと理解しましょう。
このチャプターを受講する
演習1：★
演習課題「間違い探し その1」
右のコードでは、sayHelloメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、msg変数を使って、「hello paiza」と表示されるようにしてください。



//msg変数をメソッドの引数で受け渡しする
// 間違い探し その1
public class Main {
    public static void main(String[] args) {
        String text = "paiza";
        sayHello(text);
    }

    public static void sayHello(String msg) {
        System.out.println("hello " + msg);
    }
}


演習2：★
演習課題「間違い探し その2」
右のコードでは、足し算をするsumメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、「12 + 34」の計算結果が正しく表示されるようにしてください。


//メソッド定義では、戻り値のデータ型を指定する
// 間違い探し その2
public class Main {
    public static void main(String[] args) {
        int num = sum(12, 34);
        System.out.println(num);
    }

    public static int sum(int x, int y) {
        return x + y;
    }
}



メソッド 変数 スコープ ローカル変数 Java
05:RPGの攻撃シーンを作ろう
05:RPGの攻撃シーンを作ろう (3:12)
ここでは、メソッドを使った具体的な例として、RPGの攻撃シーンを表示するプログラムを作成してみます。
このチャプターを受講する
演習1：★
演習課題「RPGの攻撃シーン」
右のコードには、RPGの攻撃シーンを表示するプログラムで、teamのメンバーが順番にattack()メソッドを呼び出します。さらに、teamのメンバーが攻撃した後に、敵の体力(enemy_hp)を表示するようになっています。

ここに、teamのメンバーの攻撃した値だけ、敵の体力をマイナスするコードを追加してください。
攻撃した値は、attack()メソッドの戻り値として与えられます。


//attackメソッドの戻り値を、enemy_hpからマイナスする
// RPGの攻撃シーン
public class Main {
    public static void main(String[] args) {
        String[] team = {"勇者", "戦士", "魔法使い"};
        int enemy_hp = 300;
        for (String person : team) {
            // 以下の行を、敵の体力を減少させるコードに書き換える
            enemy_hp -= attack(person);
            System.out.println("敵のHPは残り" + enemy_hp + "です");
        }
    }

    public static int attack(String player) {
        System.out.println(player + "はスライムを攻撃した");
        int hit = (int) (Math.random() * 10 + 1) * 10;
        System.out.println(hit + "のダメージを与えた");
        return hit;
    }
}



メソッド RPG 配列 ループ ゲームプログラム ランダム関数 Java
06:ブロックのスコープを理解しよう
06:ブロックのスコープを理解しよう (4:29)
ここでは、変数のスコープについて、さらに理解を深めたいと思います。変数の有効範囲は、
メソッド定義だけでなく、ifやforのブロックにもあるんですよ。


演習課題「間違い探し - RPGの攻撃シーン」
右のコードには、RPGの攻撃シーンを表示するプログラムですが、エラーになってしまいます。
enemiesの要素を順番に、「勇者はxxxを攻撃した」と表示するように修正してください。


//player変数を、ループのブロック外でも利用できるようにする
// 間違い探し - RPGの攻撃シーン

public class Main {
    public static void main(String[] args) {
        String[] enemies = {"スライム", "モンスター", "ドラゴン"};
        String player = "勇者";

        for (String enemy : enemies) {

            System.out.println(player + "は" + enemy + "を攻撃した");
        }

        System.out.println(player + "はすべての敵を倒した");
    }
}

Java入門編7: クラスを理解しよう (全8回)
Javaのクラスの作り方や使い方など、クラスの基本的な機能について学習します。
プログラミング学習 > Java入門編 > Java入門編7: クラスを理解しよう






01:クラスについて学習しよう
01:クラスについて学習しよう (3:34)
このレッスンでは、プログラミング言語Javaのクラスについて学習します。そして、クラスの作り方と呼び出し方を理解するとともに、メソッドの使い方について理解を深めます。
このチャプターを受講する
クラス オブジェクト インスタンス オブジェクト指向 new Java
02:クラスを作成しよう
02:クラスを作成しよう (5:00)
ここでは、クラスとオブジェクトの基本的な操作を学習します。まず初めに、クラスの作り方と呼び出し方を理解しましょう。
このチャプターを受講する
演習1：★
演習課題「クラスからオブジェクトを作ろう」
右のコードには、Greetingクラスに、メッセージを表示するsayHelloメソッドが定義されています。
このクラスを実体化して、sayHelloメソッドを呼び出し、メッセージを表示してください。


//new Greeting() で、オブジェクトを作成する
// インスタンスを実体化しよう
public class Main {
    public static void main(String[] args) {
        // この下に、インスタンスを実体化し、メソッド呼び出しを記述する
        Greeting paiza = new Greeting();
        paiza.sayHello();
    }
}

class Greeting {
    public void sayHello() {
        System.out.println("hello paiza");
    }
}


演習2：★
演習課題「クラスにメソッドを定義しよう」
右のコードには、GreetingクラスのsayHelloメソッドを呼び出していますが、メソッドの処理が記述されていません。
以下のテキストを表示するよう、メソッドにコードを追加してください。


//メソッドを記述する
// クラスにメソッドを定義しよう

public class Main {
    public static void main(String[] args) {
        Greeting paiza = new Greeting();
        paiza.sayHello();
    }
}

class Greeting {
    // この下に、sayHelloメソッドを記述する
    public void sayHello() {
        System.out.println("hello java");
    }
}


演習3：★
演習課題「間違い探し」
右のコードでは、sayHelloメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、「hello paiza」と表示されるようにしてください。


//クラス名は先頭を大文字にする
// 間違い探し
public class Main {
    public static void main(String[] args) {
        Greeting paiza = new Greeting();
        paiza.sayHello();
    }
}

class Greeting {
    public void sayHello() {
        System.out.println("hello paiza");
    }
}

クラス オブジェクト オブジェクト指向 メソッド RPG new Java
03:変数をクラスで管理しよう
03:変数をクラスで管理しよう (4:30)
ここでは、クラスで変数を管理する方法を学習します。先ほど、メソッドを持つオブジェクトを作ったので、
このオブジェクトに変数を持たせてみましょう。
このチャプターを受講する
演習1：★
演習課題「クラスからオブジェクトを作ろう」
右のコードには、Greetingクラスに、「hello XXX」と表示するsayHelloメソッドが定義されています。
「XXX」の部分は、オブジェクトを作成する時に指定できます。

このクラスからオブジェクトを作成して、sayHelloメソッドを呼び出し、「hello paiza」と表示してください。


//new Greeting("paiza")でオブジェクトを作る
// インスタンスを実体化しよう
public class Main {
    public static void main(String[] args) {
        // この下に、インスタンスを実体化し、メソッド呼び出しを記述する
        Greeting paiza = new Greeting("paiza");
        paiza.sayHello();
    }
}

class Greeting {
    private String myName;

    public Greeting(String name) {
        myName = name;
    }

    public void sayHello() {
        System.out.println("hello " + myName);
    }
}



演習2：★
演習課題「メンバー変数とコンストラクタを追加しよう」
右のコードは、GreetingクラスのsayHelloメソッドを呼び出していますが、メンバー変数とコンストラクタが記述されていません。
以下のテキストを表示するよう、メソッドにコードを追加してください。


//Greeting.newで、インスタンスを実体化する
// メンバー変数とコンストラクタを追加しよう
public class Main {
    public static void main(String[] args) {
        Greeting paiza = new Greeting("java");
        paiza.sayHello();
    }
}

class Greeting {
    // この下に、メンバー変数とコンストラクタを追加する
    private String myName;

    public Greeting(String name) {
        myName = name;
    }

    public void sayHello() {
        System.out.println("hello " + myName);
    }
}



演習3：★
演習課題「間違い探し」
右のコードでは、sayHelloメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、「hello paiza」と表示されるようにしてください。


//メンバー変数のデータ型を指定する
// 間違い探し
public class Main {
    public static void main(String[] args) {
        Greeting paiza = new Greeting("paiza");
        paiza.sayHello();
    }
}

class Greeting {
    private String myName;

    public Greeting(String name) {
        myName = name;
    }

    public void sayHello() {
        System.out.println("hello " + myName);
    }
}



クラス オブジェクト オブジェクト指向 RPG 変数 インスタンス変数 コンストラクタ new メンバー変数 Java
04:RPGの敵クラスを作ろう
04:RPGの敵クラスを作ろう (4:58)
ここでは、オブジェクトを使った具体例として、RPGの敵クラスを作ります。そして、RPGの攻撃シーンを再現してみましょう。
このチャプターを受講する
演習1：★
演習課題「RPGの攻撃シーン」
右のコードには、RPGの攻撃シーンを表示するプログラムで、teamのメンバーが順番にattackメソッドを呼び出します。
下記の期待する出力値が出力されるように、右のコードの足りない部分を補ってください。


//attackメソッドを呼び出す
// RPGの攻撃シーン
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Player> team = new ArrayList<Player>();
        team.add(new Player("勇者"));
        team.add(new Player("戦士"));
        team.add(new Player("魔法使い"));

        for (Player person : team) {
            person.attack("スライム");
        }
    }
}

class Player {
    private String myName;

    public Player(String name) {
        myName = name;
    }

    public void attack(String enemy) {
	    System.out.println(myName + "は" + enemy + "を攻撃した");
    }
}


クラス オブジェクト オブジェクト指向 RPG new コンストラクタ Java
05:クラスで、引数と戻り値のあるメソッドを作ろう
05:クラスで、引数と戻り値のあるメソッドを作ろう (3:58)
ここでは、クラスのメソッドに、引数と戻り値を追加してみましょう。例として、商品ごとに単価と個数を保持するクラスを作成します。
このチャプターを受講する
演習1：★
演習課題「学生メソッドを呼び出す」
右のコードは、学生の国語と算数のテストの点数を保持するクラスで、テストの合計点数を計算するsum()メソッドを持っています。

このクラスを使って、次の学生のオブジェクトを作成し、合計点数の計算結果を表示してください。
出力形式のXXXのところに、合計点数が入ります。
国語 = 70点
算数 = 43点
出力形式： 合計はXXX点です


//国語と算数の点数を引数に指定して、学生クラスからオブジェクトを作成する
// 学生メソッドを呼び出す
public class Main {
    public static void main(String[] args) {
        // この下に、インスタンスを実体化し、メソッド呼び出しを記述する
        Gakusei yamada = new Gakusei(70, 43);
        System.out.println("合計は" + yamada.sum() + "点です");
    }
}

class Gakusei {
    private int myKokugo;
    private int mySansu;

    public Gakusei(int kokugo, int sansu) {
        myKokugo = kokugo;
        mySansu = sansu;
    }

    public int sum() {
        return myKokugo + mySansu;
    }
}


演習2：★
演習課題「学生メソッドを作る」
右のコードは、学生の国語と算数のテストの点数を保持するクラスです。
このクラスに、テストの合計点数を計算するsum()メソッドを記述してください。


//sumメソッドを定義して、国語と算数の合計点数を返す処理を記述する
// 学生メソッドを作る
public class Main {
    public static void main(String[] args) {
        Gakusei yamada = new Gakusei(70, 43);
        System.out.println("合計は" + yamada.sum() + "点です");
    }
}

class Gakusei {
    private int myKokugo;
    private int mySansu;

    public Gakusei(int kokugo, int sansu) {
        myKokugo = kokugo;
        mySansu = sansu;
    }

    // この下に、合計得点を戻り値として返すsumメソッドを記述する
    public int sum() {
        return myKokugo + mySansu;
    }
}


クラス オブジェクト オブジェクト指向 変数 new メソッド Java
06:文字列や配列もオブジェクトになっている
06:文字列や配列もオブジェクトになっている (3:52)
ここでは、プログラミング言語Java文字列や配列がオブジェクトになっていることを学習します。そして、数値や文字列が持ついろいろなメソッドを呼び出してみましょう。
このチャプターを受講する
演習1：★
演習課題「文字列に対してメソッドを実行する」
右のコードには、text変数に文字列が代入されています。この文字列の文字数をテキストとして出力してください。
なお、文字数はスペースも含めます。


//text変数に、ドットを付けてlength()メソッドを呼び出す
// 文字列に対してメソッドを実行する

public class Main {
    public static void main(String[] args) {
        String text = new String("hello java");
        //この下に、文字数をテキストとして表示する処理を記述する
        System.out.println(text.length());
    }
}



演習2：★
 演習課題「配列に対してメソッドを実行する」
右のコードには、team配列に、RPGの職業が代入されています。この配列の要素数をテキストとして出力してください。

//team変数に、ドットを付けてlengthメソッドをカッコなしで呼び出す
// 配列に対してメソッドを実行する

public class Main {
    public static void main(String[] args) {
        String[] team = {"勇者", "戦士", "魔法使い", "忍者", "商人"};
        //この下に、要素数をテキストとして表示する処理を記述する
        System.out.println(team.length);
    }
}

クラス オブジェクト オブジェクト指向 配列 メソッド new Java
07:アクセス修飾子を理解しよう
07:アクセス修飾子を理解しよう (4:35)
ここでは、メソッド定義やメンバー変数の前に付いている「public」や「private」といった、アクセス修飾子について学習します。
このチャプターを受講する
演習1：★
演習課題「間違い探し」
右のコードでは、sayHelloメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、「hello paiza」と表示されるようにしてください。


//他のクラスから呼び出されるメソッドは、アクセス修飾子をpublicにする
// 間違い探し

public class Main {
    public static void main(String[] args) {
        Greeting paiza = new Greeting("paiza");
        paiza.sayHello();
    }
}

class Greeting {
    private String myName;

    public Greeting(String name) {
        myName = name;
    }

    public void sayHello() {
        System.out.println("hello " + myName);
    }
}


クラス オブジェクト オブジェクト指向 private public メソッド メンバー変数 Java
08:もっとstaticを理解しよう
08:もっとstaticを理解しよう (3:40)
ここでは、Mainメソッドの定義や共通のメンバー変数の前についている「static」について学習します。
また、Javaに、あらかじめ用意されているメソッドについても理解を深めましょう。


演習課題「学生クラスのメソッドを呼び出す」
右のコードは、学生の国語と算数のテストの点数を計算するクラスです。メソッドにstaticが付いているので、オブジェクトを実体化しなくても、メソッドを呼び出すことができます。
mainメソッドで、次のテストの点数を使って、sum()メソッドを呼び出し、合計点数の計算結果を表示してください。
出力形式のXXXのところに、合計点数が入ります。

国語 = 70点
算数 = 43点
出力形式： 合計はXXX点です。



//Gakusei.sum()メソッドを呼び出す
// 学生メソッドを呼び出す
public class Main {
    public static void main(String[] args) {
        // この下に、合計得点を戻り値として返すsumメソッドを記述する
        // 国語 = 70点、算数 = 43点
        int total = Gakusei.sum(70, 43);
        System.out.println("合計は" + total + "点です。");
    }
}

class Gakusei {
    // この下に、合計得点を戻り値として返すsumメソッドを記述する
    public static int sum(int kokugo, int sansu) {
        return kokugo + sansu;
    }
}


Java入門編8:さらにクラスを理解しよう (全8回)
クラス継承やメソッドのオーバーライドなど、Javaのオブジェクト指向開発についてさらに学習します。
プログラミング学習 > Java入門編 > Java入門編8:さらにクラスを理解しよう




01:もっとクラスについて学習しよう (3:06)
このレッスンでは、クラス継承やメソッドのオーバーライドなど、Javaのクラス関連機能を学習して、大規模なプログラムの内容やJavaの仕組みについて、さらに理解しましょう。
このチャプターを受講する
クラス オブジェクト指向 オブジェクト インスタンス 継承 Java
02:クラスを継承する
02:クラスを継承する (5:42)
ここでは、クラスの継承ついて学習します。例として、RPGのアイテムがはいる入れ物のクラスを作り、そこから宝箱と宝石箱クラスを継承で作ってみましょう。
このチャプターを受講する
演習1：★
演習課題「クラスにメソッドを定義しよう」
右のコードでは、Greetingクラスにメンバー変数msgとtargetが定義されており、Greetingクラスを継承したHelloクラスが定義されています。
このコードでは、HelloクラスのsayHelloメソッドを呼び出していますが、メソッドが記述されていません。
sayHello()メソッドでは、以下の変数でメッセージを表示するようにしてください。

msg + " " + target


//public void sayHello()メソッドを定義する
// クラスにメソッドを定義しよう
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello();
        player.sayHello();
    }
}

class Greeting {
    public String msg;
    public String target;

    public Greeting() {
        msg = "hello";
        target = "paiza";
    }
}

class Hello extends Greeting {
    // この下に、sayHelloメソッドを記述する
    public void sayHello(){
        System.out.println(msg + " " + target);
    }
}


演習2：★
演習課題「クラスを継承しよう」
右のコードでは、Greetingクラスにメンバー変数msgとtargetが定義されています。
このGreetingクラスを継承したHelloクラスを作り、sayHello()メソッドを定義してください。
このコードでは、HelloクラスのsayHelloメソッドを呼び出していますが、メソッドが記述されていません。
sayHello()メソッドは、以下の変数でメッセージを表示するようにしてください。

msg + " " + target



//extends Greetingで継承する
// クラスを継承しよう
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello();
        player.sayHello();
    }
}

class Greeting {
    public String msg;
    public String target;

    public Greeting() {
        msg = "hello";
        target = "paiza";
    }
}
// この下に、Greetingクラスを継承した、Helloクラスを定義する。
// そこに、sayHello()メソッドの定義を記述する。
class Hello extends Greeting {
    public void sayHello(){
        System.out.println(msg + " " + target);
    }
}



演習3：★
演習課題「間違い探し」
右のコードでは、sayHelloメソッドを呼び出していますが、エラーになってしまいます。
間違いを修正して、「hello paiza」と表示されるようにしてください。


//クラス名は先頭を大文字にする
// 間違い探し
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello();
        player.sayHello();
    }
}

class Greeting {
    public String msg;
    public String target;

    public Greeting() {
        msg = "hello";
        target = "paiza";
    }
}

class Hello extends Greeting {
    public void sayHello(){
        System.out.println(msg + " " + target);
    }
}


クラス オブジェクト指向 オブジェクト インスタンス 継承 コンストラクタ Java
03:引数ありのコンストラクタ
03:引数ありのコンストラクタ (4:43)
ここでは、クラスの継承をする場合のコンストラクタの使い方について学習します。
このチャプターを受講する
演習1：★
演習課題「サブクラスにコンストラクタを定義しよう」
右のコードでは、Greetingクラスが定義されており、それを継承したHelloクラスが定義されていますが、エラーになってしまいます。
Helloクラスにコンストラクタを定義して、「hello paiza」と表示されるようにしてください。


//コンストラクタは、引数として文字列を受け取り、superメソッドを呼び出す
// サブクラスにコンストラクタを定義しよう
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello("paiza");
        player.sayHello();
    }
}

class Greeting {
    public String target;

    public Greeting(String name) {
        target = name;
    }
}

class Hello extends Greeting {
    // この下にコンストラクタを定義する
    public Hello(String name) {
        super(name);
    }

    public void sayHello(){
        System.out.println("hello " + target);
    }
}



クラス オブジェクト指向 オブジェクト インスタンス 継承 コンストラクタ Java
04:メソッドのオーバーライド
04:メソッドのオーバーライド (3:14)
ここでは、クラスを継承したときに利用できるメソッドのオーバーライドについて学習します。 オーバーライドを使うと、親クラスが持つメソッドを子クラスで再定義できます。
このチャプターを受講する
演習1：★
演習課題「メソッドをオーバーライドしよう」
右のコードには、Greetingクラスに、say_helloメソッドが定義されており、
Greetingクラスを継承したHelloクラスが定義されています。

このHelloクラスで、sayHelloメソッドをオーバーライドして、以下のメッセージを表示してください。
hello paiza



//System.out.println()で「hello paiza」を出力する;
// メソッドをオーバーライドしよう
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello();
        player.sayHello();
    }
}
class Greeting {
    public void sayHello(){
        System.out.println("greeting paiza");
    }
}
class Hello extends Greeting {
    // この下で、メソッドをオーバーライドする
    public void sayHello(){
        System.out.println("hello paiza");
    }
}



演習2：★
演習課題「メソッドをオーバーライドしよう2」
右のコードには、Greetingクラスを継承したHelloクラスが定義されています。
そして、Greetingオブジェクトを実体化して、player変数に割り当てています。

このplayer変数に、Helloオブジェクトを実体化して割り当てください。



//public void sayHello()メソッドを定義する
// メソッドをオーバーライドしよう2
public class Main {
    public static void main(String[] args) {
        Hello player = new Hello();
        player.sayHello();
    }
}

class Greeting {
    public void sayHello(){
        System.out.println("greeting paiza");
    }
}

class Hello extends Greeting {
    public void sayHello(){
        System.out.println("hello paiza");
    }
}



クラス オブジェクト指向 オブジェクト インスタンス 継承 オーバーライド Java
05:RPGのPlayerクラスを継承で記述１
05:RPGのPlayerクラスを継承で記述１ (3:40)
ここでは、クラスを継承する具体例として、RPGのPlayerクラスを継承で記述します。 まずは、親クラスを作成しましょう。
このチャプターを受講する
クラス オブジェクト指向 オブジェクト インスタンス RPG Java
06:RPGのPlayerクラスを継承で記述２
06:RPGのPlayerクラスを継承で記述２ (3:50)
ここでは、クラス継承の具体例として、RPGのPlayerクラスを継承で記述します。 前回に引き続いて、親クラスを継承して、魔法使いのクラスを作成しましょう。
このチャプターを受講する
演習1：★
演習課題「RPGの攻撃シーン」
右のコードには、RPGの攻撃シーンを表示するプログラムで、teamのメンバーがattackメソッドを順番に呼び出します。このコードを修正して、下記のサンプル出力が表示されるように、右のコードを修正してください。


//戦士をあらわすオブジェクトは、Warriorクラスから実体化させる
// RPGの攻撃シーン
public class Main {
    public static void main(String[] args) {
        Player hero = new Player("勇者");
        Player wizard = new Player("魔法使い");
        Warrior warrior = new Warrior("戦士");
        Player[] party = {hero, wizard, warrior};

        for (Player member : party) {
            member.attack("スライム");
        }
    }
}

class Player {
    public String myName;

    public Player(String name) {
        myName = name;
    }

    public void attack(String enemy) {
        System.out.println(myName + "は" + enemy + "を攻撃した");
    }
}

class Warrior extends Player {
    public Warrior(String name) {
        super(name);
    }

    public void attack(String enemy) {
        System.out.println(myName + "は" + enemy + "を猛攻撃した");
    }
}


クラス オブジェクト指向 オブジェクト インスタンス RPG 継承 オーバーライド Java
07:メソッドのオーバーロードを理解しよう
07:メソッドのオーバーロードを理解しよう (4:05)
ここでは、メソッドのオーバーロードという機能を学習します。メソッドのオーバーロードを使うと、同じメソッド名で、引数の数やデータ型が異なるメソッドを定義することができます。
このチャプターを受講する
演習1：★
演習課題「オーバーロードされたメソッドを呼び出す」
右のコードでは、引数の異なるsayHelloメソッドが定義されています。。
サンプル出力と同じように表示されるよう、sayHello()メソッドの呼び出しを追加してください。


//sayHello()メソッドを、引数なしとありで呼び出す。
// オーバーロードされたメソッドを呼び出す
public class Main {
    public static void main(String[] args) {
        // この下で、sayHelloメソッドを呼び出す。
        sayHello();
        sayHello("java");
    }

    public static void sayHello(){
        System.out.println("hello paiza");
    }

    public static void sayHello(String target){
        System.out.println("hello " + target);
    }
}



クラス オブジェクト指向 オブジェクト インスタンス オーバーロード Java
08:組み込みクラスを使ってみよう
08:組み込みクラスを使ってみよう (4:23)
ここでは、あらかじめ用意されている組み込みクラスの使い方を学習します。組み込みクラスには、 標準入力からデータを読み込むScannerやArrayListのようにオブジェクトを作って使うものがあります。


 演習課題「間違い探し」
右のコードでは、標準入力からテキストを読み込んで、「AAAは、スライムと戦った！」と表示するプログラムですがエラーになってしまいます。このプログラムを修正して、正常に動作するようにしてください。


//クラス名を大文字で記述する
//間違い探し
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String player = sc.next();
        System.out.println(player + "は、スライムと戦った！");
    }
}


Java入門編9: HashMap(連想配列)の基礎 (全6回)
JavaでのHashMap(連想配列)の基礎について学び、RPGのアイテム一覧を作る事を目指します。
プログラミング学習 > Java入門編 > Java入門編9: HashMap(連想配列)の基礎



01:HashMapとは何かを学ぼう
01:HashMapとは何かを学ぼう (2:47)
ここでは、プログラミング言語Javaを使って、配列と並んでよく使われるHashMapについて、基本的な考え方を学習します。
このチャプターを受講する
連想配列 HashMap Java
02:HashMapを作る
02:HashMapを作る (3:39)
ここでは、HashMapの基本操作について学びます。そして、Javaを使って、HashMapの作成、表示、代入といった機能を試してみましょう。
このチャプターを受講する
演習1：★
演習課題「指定の文字をハッシュにする」
右のコードには、RPGのプレイヤーのスキルがHashMapで記述されています。
このHashMapに、以下のエントリーを追加して、値だけを出力してください。

防御力 : 100
魔法力 : 200
移動力 : 380


//putメソッドで追加して、getメソッドで出力
// 指定の文字をハッシュにする
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> skills = new HashMap<String, Integer>();
        skills.put("攻撃力", 150);
        System.out.println(skills.get("攻撃力"));
        // この下に、エントリーを追加する
        skills.put("防御力", 100);
        System.out.println(skills.get("防御力"));
        skills.put("魔法力", 200);
        System.out.println(skills.get("魔法力"));
        skills.put("移動力", 380);
        System.out.println(skills.get("移動力"));
    }
}



演習2：★
演習課題「間違い探し」
右のコードには、RPGのプレイヤーのスキルがHashMapで記述されていますがエラーになってしまいます。間違いを修正して、HashMapの値だけを出力してください。


//HashMapのデータ型が整数の場合、intではなくIntegerを指定する
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> skills = new HashMap<String, Integer>();
        skills.put("攻撃力", 150);
        System.out.println(skills.get("攻撃力"));
        skills.put("防御力", 100);
        System.out.println(skills.get("防御力"));
        skills.put("魔法力", 200);
        System.out.println(skills.get("魔法力"));
        skills.put("移動力", 380);
        System.out.println(skills.get("移動力"));
    }
}



連想配列 HashMap Java
03:HashMapの基本操作
03:HashMapの基本操作 (3:37)
ここでは、HashMapの基本的な操作について、もう少し学習します。エントリーを変数で取り出したり、キーがないエントリーにアクセスしたり、いろいろと試してみましょう。
このチャプターを受講する
演習1：★
演習課題「マップのサイズを出力してみよう」
右のコードには、skillsというHashMapが定義されています。
このHashMapのサイズを出力してください。



//sizeメソッドを使用する
//  マップのサイズを出力してみよう
import java.util.HashMap;
public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> skills = new HashMap<String, Integer>();
        skills.put("攻撃力", 150);
        skills.put("防御力", 100);
        skills.put("魔法力", 200);
        skills.put("移動力", 380);

        // この下に、エントリーを追加する
        System.out.println(skills.size());
    }
}



連想配列 HashMap Java
04:HashMapをループで処理する
04:HashMapをループで処理する (3:38)
ここでは、ループでHashMapを扱います。そのために、Javaの拡張forとHashMapを組み合わせについて学習します。HashMapに多くのエントリーが格納されているとき、ループを使って一括して処理してみましょう。
このチャプターを受講する
演習1：★
演習課題「ループでマップの値を出力しよう」
右のコードには、skillsというマップが定義されています。
このマップの値をループを使って出力してください。


//拡張forで、entrySetを取り出す
// ループでマップの値を出力しよう
import java.util.HashMap;
import java.util.Map.Entry;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> skills = new HashMap<String, Integer>();
        skills.put("攻撃力", 150);
        skills.put("防御力", 100);
        skills.put("魔法力", 200);
        skills.put("移動力", 380);

        // この下で、マップの値をループで出力する
        for(Entry<String, Integer> entry : skills.entrySet()){
            System.out.println(entry.getValue());
        }
    }
}



演習2：★
演習課題「ループでマップのキーと値を出力しよう」
右のコードには、skillsというマップが定義されています。
このマップの値をループを使って出力してください。
このとき、マップのエントリーを以下の形式で出力します。

"キー"は"値"です


//getKey()で、キーを取り出す。
// ループでマップのキーと値を出力しよう
import java.util.HashMap;
import java.util.Map.Entry;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> skills = new HashMap<String, Integer>();
        skills.put("攻撃力", 150);
        skills.put("防御力", 100);
        skills.put("魔法力", 200);
        skills.put("移動力", 380);

        // この下で、マップの値をループで出力する
        for(Entry<String, Integer> entry : skills.entrySet()){
            System.out.println(entry.getKey() + "は" + entry.getValue() + "です");
        }
    }
}


演習3：★


演習課題「ループで合計を計算しよう」
右のコードには、pointsというマップに、科目とテストの点数が格納されています。
このマップの値の合計を計算して出力してください。



//ハッシュの各値を足し合わせる
// ループでマップの値を出力しよう
import java.util.HashMap;
import java.util.Map.Entry;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> points = new HashMap<String, Integer>();
        points.put("国語", 51);
        points.put("算数", 35);
        points.put("英語", 52);
        points.put("理科", 19);

        // この下で、マップの値の合計をループで計算する
        int sum = 0;
        for(Entry<String, Integer> entry : points.entrySet()){
            sum += entry.getValue();
        }
        System.out.println(sum);
    }
}



連想配列 HashMap Java
05:RPGのアイテム一覧を再現１
05:RPGのアイテム一覧を再現１ (2:20)
今回と次回のチャプターでは、マップとループを使った具体例として、RPGのアイテム一覧を作成します。まずは、どのようなプログラムを作るのか、基本的な内容を整理しましょう。
このチャプターを受講する
連想配列 配列 RPG ゲームプログラム HashMap Java
06:RPGのアイテム一覧を再現2
06:RPGのアイテム一覧を再現2 (4:05)
回と今回のチャプターでは、マップとループを使った具体例として、RPGのアイテム一覧を作成しています。このチャプターでは、実際にアイテムリストを実装していきます。


Java入門編10:例外処理を理解しよう (全13回)
実行時に発生したエラーに対応する、Javaの例外処理について学習します。





01:例外処理の概要を理解しよう
01:例外処理の概要を理解しよう (3:23)
このレッスンでは、実行時に発生する問題にプログラムを対応させる、Javaの例外処理について学習します。プログラムを安定して動作させることでプログラムの品質を高める、例外処理について理解を深めましょう。
このチャプターを受講する
例外処理 例外 Java








02:簡単な例外処理してみよう
02:簡単な例外処理してみよう (5:16)
ここでは、簡単な例外処理を実際に記述します。例外が発生する簡単なプログラムを作って、それに対応するコードを書いてみましょう。
このチャプターを受講する




演習1：★
演習課題「例外処理を定義しよう」
右のコードでは、RPGの勇者の行動を3行表示しますが、enemies配列の範囲外にアクセスするため、例外が発生してプログラムが強制終了してしまいます。
このプログラムに、try-catch-finallyを追加して、例外が発生してもプログラムが強制終了しないようにして下さい。


//try-catch-finallyを記述する。3行目はfinallyブロックに記述する
// 例外処理を定義しよう

public class Main {
    public static void main(String[] args) {
        String[] enemies = {"スライム", "ドラゴン", "魔王" };

        try {
            int number = 3;
            System.out.println("勇者は敵に遭遇した");
            System.out.println("勇者は" + enemies[number] + "と戦った");
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            System.out.println("勇者は勝利した");
        }
    }
}


例外処理 例外 finally Java
03:いろいろな書式で例外に対応しよう
03:いろいろな書式で例外に対応しよう (4:36)
ここでは、いろいろな形で例外に対応します。printStackTraceで例外情報を表示するだけでなく、分かりやすいエラーメッセージを追加してみましょう。
このチャプターを受講する
演習1：★
演習課題「例外メッセージを指定しよう」
右のコードでは、RPGの勇者の行動を3行表示しますが、enemies配列の範囲外にアクセスするため、例外が発生してしまいます。
このプログラムで、例外が発生した時に、標準エラー出力に下記のメッセージを表示して下さい。


//System.err.println()で、エラーメッセージを出力する
// 例外メッセージを指定しよう

public class Main {
    public static void main(String[] args) {
        String[] enemies = {"スライム", "ドラゴン", "魔王" };

        try {
            int number = 3;
            System.out.println("勇者は敵に遭遇した");
            System.out.println("勇者は" + enemies[number] + "と戦った");
        } catch (Exception e) {
            System.err.println("その敵は表示できません");
        } finally {
            System.out.println("勇者は勝利した");
        }
    }
}



例外処理 標準エラー出力 Java
04:発生させる例外を変えてみよう
04:発生させる例外を変えてみよう (4:24)
ここでは、いろいろな種類の例外に対応する方法を学習します。例として、ゼロで割り算するだけでなく、数値変換の例外を捕捉してみましょう。
このチャプターを受講する
演習1：★
演習課題「例外の種類を変更しよう」
右のコードでは、RPGの勇者の行動を3行表示します。
しかし、enemies配列の範囲外にアクセスするため例外が発生するのですが、捕捉する例外が異なるため、プログラムが強制終了してしまいます。
このプログラムを修正して、配列の範囲外にアクセスした場合の例外を捕捉してください。



//ArrayIndexOutOfBoundsExceptionか、Exceptionを捕捉する
// 例外の種類を変更しよう
public class Main {
    public static void main(String[] args) {
        String[] enemies = {"スライム", "ドラゴン", "魔王" };

        try {
            int number = 3;
            System.out.println("勇者は敵に遭遇した");
            System.out.println("勇者は" + enemies[number] + "と戦った");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.err.println("その敵は表示できません");
        } finally {
            System.out.println("勇者は勝利した");
        }
    }
}



例外処理 例外 Java
05:複数の例外を捕捉してみよう
05:複数の例外を捕捉してみよう (4:59)
ここでは、複数の種類の例外に対応する方法を学習します。
ゼロ除算や数値変換などの複数の例外に対応できるよう、割り算プログラムを改良していきましょう。
このチャプターを受講する
演習1：★
演習課題「例外の種類を変更しよう」
右のコードは、RPGの勇者の行動を3行表示します。
しかし、enemies配列の範囲外にアクセスするため例外が発生するのですが、捕捉する例外が異なるため、プログラムが強制終了してしまいます。
このプログラムにcatchブロックを追加して、配列の範囲外にアクセスした場合の例外を捕捉してください。追加したブロックでは、標準エラー出力に下記のメッセージを表示して下さい。



//catchブロックを追加して、ArrayIndexOutOfBoundsExceptionか、Exceptionを捕捉する。
追加メッセージは、System.err.println()で表示します。
// 複数の例外を捕捉しよう

public class Main {
    public static void main(String[] args) {
        String[] enemies = {"スライム", "ドラゴン", "魔王" };

        try {
            int number = 3;
            System.out.println("勇者は敵に遭遇した");
            System.out.println("勇者は" + enemies[number] + "と戦った");
        } catch (NumberFormatException e) {
            System.err.println("文字列を数値に変換できません。");
        } catch (Exception e) {
            System.err.println("その敵は表示できません");
        } finally {
            System.out.println("勇者は勝利した");
        }
    }
}


例外処理 例外 Java
06:具体例：標準入力でプレイヤーを選択する
06:具体例：標準入力でプレイヤーを選択する (5:49)
ここでは、例外処理の具体例として、RPGのプレイヤーを表示するプログラムに例外処理を追加します。 
標準入力からの値に合わせて、プレイヤーを選択して表示しますが、処理できない場合にエラーメッセージを表示させましょう。
このチャプターを受講する
演習1：★
演習課題「標準入力でモンスターを選択する」
右のコードは、標準入力から受け取った値に合わせて、RPGの勇者の行動を3行表示します。
このプログラムで、例外の種類に合わせて、下記のエラーメッセージを標準エラー出力に表示して下さい。

文字を入力 : 数値を入力してください
配列の範囲外にアクセス : 0から(配列の最大インデックス)を入力してください



//catch文の中に標準エラー出力のコードを記述する
//標準入力でモンスターを選択する
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // モンスターを配列で記述する
        String[] enemies = {"スライム", "ドラゴン", "魔王" };

        try {
            // 標準入力から整数を入力
            Scanner sc = new Scanner(System.in);
            int number = Integer.parseInt(sc.next());

            // 入力値に合わせて、プレイヤー名を表示する
            System.out.println("勇者は敵に遭遇した");
            System.out.println("勇者は" + enemies[number] + "と戦った");

        } catch (ArrayIndexOutOfBoundsException e) {
            System.err.println("0から" + (enemies.length - 1) + "を入力してください");
        } catch (NumberFormatException e) {
            System.err.println("数値を入力してください");
        } finally {
            System.out.println("勇者は勝利した");
        }
    }
}



例外処理 RPG Java
07:throwで意図的に例外を投げよう
07:throwで意図的に例外を投げよう (4:08)
ここでは、例外を意図的に投げるthrowについて学習します。
throwを使うと、意図的に例外処理を起動できます。また、catchと組み合わせることで、
メソッドの呼び出し元にある例外処理を利用できます。
このチャプターを受講する
演習1：★
演習課題「間違い探し」
右のコードは、簡単な割り算プログラムです。強制的にゼロ除算例外を発生するはずですが、コンパイルエラーになってしまいます。ゼロで割り算した時に、下記のエラーメッセージを表示するようコードを修正してください。



//ArithmeticExceptionの例外ハンドラを追加する
// 例外処理 - 間違い探し

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");

        try {
            int answer = 100 / 0;
            System.out.println(answer);
            throw new ArithmeticException("強制エラー");
        } catch (ArithmeticException e) {
            System.err.println("0では割り算できません");
        } catch (NumberFormatException e) {
            System.err.println("数値を入力してください");
        } catch (Exception e) {
            System.err.println("例外が発生しました");
        } finally {
            System.out.println("Hello Java");
        }
    }
}



例外処理 throw Java
08:テキストファイルを読み書きしよう
08:テキストファイルを読み書きしよう (4:45)
ここでは、例外からちょっと離れて、Javaでテキストファイルを読み書きする方法を学習します。
プログラムでは、データをやり取りしたり保存するために、ファイルを使うことが良くあります。
このチャプターを受講する
演習1：★
 演習課題「0から99までファイルに書き込む」
右のコードは、ファイルを読み書きするプログラムです。これを改良して、0から99まで1行ずつ書き込んで、表示するプログラムを作成してください。



//0から99まで、ループで出力する。書き込む時、行末は改行する。
// 0から99までファイルに書き込む
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) throws IOException {

        File file = new File("articles.txt");

        // ファイル書き込み
        FileWriter filewriter = new FileWriter(file);
        // ここに、0から99まで1行ずつ書き込むコードを記述する
        for (int i = 0; i < 100; i++) {
            filewriter.write(i + "\n");
        }
        filewriter.close();

        // ファイル読み込み
        Scanner scan = new Scanner(file);
        while (scan.hasNextLine()) {
            String line = scan.nextLine();
            System.out.println(line);
        }
        scan.close();
    }
}



例外処理 ファイル操作 Java
09:ファイルアクセスに例外処理を追加しよう
09:ファイルアクセスに例外処理を追加しよう (4:04)
ここでは、ファイルアクセスに例外処理を追加します。
先ほど作ったテキストファイルの読み書きプログラムに、
try-catchの例外処理を付け加えてみましょう。
このチャプターを受講する
演習1：★
演習課題「間違い探し」
右のコードは、ファイルに0から99まで1行ずつ書き込んで表示するプログラムですが、コンパイルエラーになってしまいます。間違いを修正して、プログラムを完成させてください。


//FileWriterオブジェクトとScannerオブジェクトのコンストラクタに引数を指定する
// 0から99までファイルに書き込む
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {

        File file = new File("articles.txt");

        // ファイル書き込み
        try (FileWriter filewriter = new FileWriter(file)) {
            for (int i = 0; i < 100; i++){
                filewriter.write(i + "\n");
            }
        } catch (IOException e) {
            System.err.println("ファイル書き込みに失敗しました");
            e.printStackTrace();
        }

        // ファイル読み込み
        try (Scanner scan = new Scanner(file)) {
            while (scan.hasNextLine()) {
                String line = scan.nextLine();
                System.out.println(line);
            }
        } catch (FileNotFoundException e) {
            System.err.println("ファイル読み込みに失敗しました");
            e.printStackTrace();
        }
    }
}



例外処理 ファイル操作 finally Java
10:ファイルアクセスにtry-with-resourcesを使おう
10:ファイルアクセスにtry-with-resourcesを使おう (2:34)
ここでは、Java7以降で利用できるtry-with-resourcesについて学習します。この機能を使うと、ファイルやデータベースなどで自動的にクローズ処理を行うことができます。
このチャプターを受講する
演習1：★
例外処理 ファイル操作 try-with-resources Java
11:例外クラスのクラス構成を理解しよう
11:例外クラスのクラス構成を理解しよう (5:45)
ここでは、例外オブジェクトのクラス構成について学習します。例外オブジェクトについて学習すると、例外処理の動作をもっと理解できます。
このチャプターを受講する
演習1：★
例外処理 例外 throws Java
12:throwsで例外処理を呼び出し元に任せよう
12:throwsで例外処理を呼び出し元に任せよう (3:50)
ここでは、チェック例外の対応を呼び出し元に任せるthrowsについて学習します。throwsを使うことで、メソッドの呼び出し元で適切にチェック例外に対応することが可能になります。
このチャプターを受講する
演習1：★
演習課題「間違い探し」
右のコードは、ファイルに0から99まで1行ずつ書き込んで表示するプログラムですが、コンパイルエラーになってしまいます。コードを修正して、プログラムを完成させてください。




//メソッド定義にthrows FileNotFoundExceptionを追加する
// 0から99まで表示する
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {

        File file = new File("articles.txt");

        // ファイル書き込み
        try {
            FileWriter filewriter = new FileWriter(file);
            for (int i = 0; i < 100; i++){
                filewriter.write(i + "\n");
            }
            filewriter.close();
        } catch (IOException e) {
            System.err.println("ファイル書き込みに失敗しました");
            e.printStackTrace();
        }

        // ファイル読み込み
        try {
            Scanner scan = makeScanner(file);
            while (scan.hasNextLine()) {
                String line = scan.nextLine();
                System.out.println(line);
            }
            scan.close();
        } catch (FileNotFoundException e) {
            System.err.println("ファイル読み込みに失敗しました");
            e.printStackTrace();
        }
    }

    public static Scanner makeScanner(File file) throws FileNotFoundException {
        Scanner scan = new Scanner(file);
        return scan;
    }
}

例外処理 例外 throws Java
13:throwとtry-catchで再スローしよう
13:throwとtry-catchで再スローしよう (3:58)
ここでは、throwとtry-catchを組み合わせる再スローについて学習します。
再スローでは、メソッドのcatchブロックの中から、受け取った例外を呼び出し元にスローします。
そのおかげで、捕捉した例外を、catchのところで出来るだけ対応して、
残りの作業を呼び出し元に任せることができます。


演習課題「間違い探し」
右のコードは、ファイルに0から99まで1行ずつ書き込んで表示するプログラムですが、コンパイルエラーになってしまいます。コードを修正して、プログラムを完成させてください。


//メソッド定義にthrows FileNotFoundExceptionを追加する
// 0から99まで表示する
import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {

        File file = new File("articles.txt");

        // ファイル書き込み
        try (FileWriter filewriter = new FileWriter(file)) {
            for (int i = 0; i < 100; i++){
                filewriter.write(i + "\n");
            }
        } catch (IOException e) {
            System.err.println("ファイル書き込みに失敗しました");
            e.printStackTrace();
        }

        // ファイル読み込み
        try (Scanner scan = makeScanner(file)) {
            while (scan.hasNextLine()) {
                String line = scan.nextLine();
                System.out.println(line);
            }
        } catch (FileNotFoundException e) {
            System.err.println("ファイル読み込みに失敗しました");
            e.printStackTrace();
        }
    }

    public static Scanner makeScanner(File file) throws FileNotFoundException {
        try {
            Scanner scan = new Scanner(file);
            return scan;
        } catch (FileNotFoundException e) {
            System.err.println("makeScannerで例外を検出しました");
            throw e;
        }
    }
}
