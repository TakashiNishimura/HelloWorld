# C#（ macOS ）

## C#について

* 2000年にアルファ版が登場、2002年に Ver.1.0 がリリース（現在 Ver.8.0）
* C/C++ から構文・キーワード・演算子を譲り受けつつ、文法は Java に大きな影響を受けている
* [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework) 、[Mono](http://bit.ly/2l5Mzx1) 等のライブラリを使うことで最大限の力を発揮する
* [Ecma インターナショナル](http://bit.ly/2lLMUZZ)、[ISO](http://bit.ly/1VLZ5lB) により標準化され、[JIS](http://bit.ly/2lQk5vD) で標準プログラミング言語として制定されている
* [Unity](http://bit.ly/2l5GJMb) の開発言語して採用

## 開発環境の構築

|カテゴリ|ソフトウェア|リリース|
|:--:|:--:|:--:|
|OS|[macOS Sierra](https://ja.wikipedia.org/wiki/MacOS) 10.15.6|2020年07月|
|統合開発環境|[Xcode](https://developer.apple.com/download/) 12 beta 3|2020年07月|
|コンパイラ|[Mono](http://www.mono-project.com/) Framework 6.10.0（C# 8.0）|2020年05月|
|エディタ|Visual Studio Code 1.47.2|2020年07月|
|拡張機能|C#（Microsoft） 1.22.1|ー|

1. [Xcode](https://ja.wikipedia.org/wiki/Xcode) のインストール  
    1. Apple ID を用意し [Xcode](https://developer.apple.com/download/) にアクセス
    1. <b>Xcode</b> 12 beta 3 を [Download] を選択、指示に従ってダウンロード
    1. ダウンロードした <b>Xcode</b>_12_beta_3.xip をダブルクリック、指示に従ってインストール
    1. 生成された <b>Xcode</b>-beta<b>.app</b> をアプリケーションフォルダに移動

1. [Mono](http://www.mono-project.com/) のインストール
    1. http://www.mono-project.com/download/ にアクセス
    1. [Download Mono 6.10.0(Visual Studio channel)] を選択
    1. ダウンロードした <b>.pkg</b> ファイルをダブルクリック、指示に従ってインストール
    1. ターミナルでバージョン確認  
    $ mono --version  
    Mono JIT compiler version 6.10.0.104 (2019-12/5d03a6fe116 Wed Apr 29 20:51:09 EDT 2020)

1. Visual Studio Codeに拡張機能の追加  
    [表示] → [拡張機能] から [C#（Microsoft）] を検索＆インストール

## コードの記述

1. Visual Studio Code を起動
    1. [ファイル] → [新規ファイル] → [テキスト エディター] を選択
    1. [ファイル] → [保存] を選択
    1. 任意の場所（今回はデスクトップ上に作成）に test<b>.cs</b> という名で保存

1. コードの記述
```
//test.cs
using System; //Console.WriteLine() に必要

class HelloWorld { //Mainは不可
    static void Main() { //自動的に最初に実行される
        Console.WriteLine("Hello,world!");
    }
}
```

## コンパイル〜実行

1. Visual Studio Code で [表示] → [ターミナル] を選択

1. test.cs ファイルのあるディレクトリに移動  
$ cd /Users/（ユーザー名）/Desktop

1. コンパイル（.cs → .exe）  
$ <b>mcs</b> test<b>.cs</b>

1. test.cs ファイルと同階層に test.exe ファイルが生成されたのを確認

1. 実行  
$ <b>mono</b> test<b>.exe</b>  
Hello,world! ←と表示されたら成功！

***
作成者: 夢寐郎  
作成日: 2017年03月05日  
更新日: 2020年07月26日