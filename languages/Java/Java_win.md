# Java（ Windows ）

## Javaについて

* 1995年に登場したオブジェクト指向プログラミング言語
* [Android](https://ja.wikipedia.org/wiki/Android) アプリ開発言語として採用
* 2010年に開発元の米 [Sun Microsystems](http://bit.ly/2mySRXN) が米 [Oracle](http://bit.ly/2m5QRZU) により買収され、[Java](https://ja.wikipedia.org/wiki/Java) 関連の権利も移転
* ① [Java SE](http://bit.ly/1qWEkCh)（スタンドアローン用） ② [Java EE](http://bit.ly/2m11Mn2)（サーバサイド用） ③ [Java ME](http://bit.ly/2lODD2J)（組み込み分野用）のエディションがある

## 開発環境の構築

|カテゴリ|ソフトウェア|リリース|
|:--:|:--:|:--:|
|OS|[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows) 10（64bit）|ー|
|開発環境|[Java SE Development Kit](http://bit.ly/1lO1FSV) 1.8.0_121|2017年01月|
|エディタ|Visual Studio Code 1.10.2|2017年03月|
|拡張機能|[Java Language Support](http://bit.ly/2lj4bpb) 0.0.23|2016年10月|

1. [Java SE Development Kit](http://bit.ly/1lO1FSV) のインストール
    1. http://www.oracle.com/technetwork/java/javase/downloads/ にアクセスし、[Java DOWNLOAD] を選択
    1. [Accept License Agreement] のラジオボタンを選び、jdk-8u121-windows-x64.exe を選択
    1. ダウンロードした .exe ファイルをダブルクリックして指示に従いインストール

1. [環境変数](http://bit.ly/2lCIAgK)の設定  
    1. タスクバーのスタートボタンを右クリック → [コントロールパネル] → [システムとセキュリティ] → [システム] → [システムの詳細設定] → [環境変数] を開く
    1. [システム環境変数] で変数 "Path" を探して選択 → [編集] ボタンをクリック
    1. 変数値の最後に ;C:\Program Files\Java\jdk1.8.0_121\bin を追加（java.exe、javac.exeが存在）
    1. Windows を再起動
    1. コマンドプロンプトでバージョン確認  
        \>java -version  
        java version "1.8.0_121"  
        \>>javac -version  
        javac 1.8.0_121

1. Visual Studio Codeに拡張機能の追加  
    [表示] → [拡張機能] から [Java Language Support](http://bit.ly/2lj4bpb) を検索＆インストール

## コードの記述

1. Visual Studio Code を起動
    1. [ファイル] → [新規ファイル] を選択
    1. [ファイル] → [保存] を選択
    1. 任意の場所（今回はデスクトップ上に Java フォルダを作成）に MyClass<b>.java</b> という名で保存  
    ※<b>ファイル名は作成するクラスと同じ名前にする必要がある</b>

1. コードの記述
```
//MyClass.java
public class MyClass { //publicは省略可能
    //コンストラクタ
    public static void main(String[] args) {
        System.out.println("Hello,world!");
    }
}
```

## コンパイル〜実行

1. コマンドプロンプトを起動

1. MyClass.java ファイルのあるディレクトリに移動  
\>cd \Users\（ユーザー名）\Desktop\Java

1. コンパイル（.java → .class）  
\>javac MyClass.java

1. MyClass.java ファイルと同階層に MyClass.class ファイルが生成されたのを確認

1. 実行  
\>java MyClass  
Hello,world! ←と表示されたら成功！

***
作成者: 夢寐郎  
作成日: 2017年03月16日