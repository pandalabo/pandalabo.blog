---
title: ごいたコマンドアプリの紹介
date: 2017-03-18 21:09:51
tags:
    - ごいた
    - ツール
---

ごいたが遊べるコマンドラインツールを作成しました。

こんな画面です。

![ごいたコマンド](2017-03-18-23-40-31.png)

インストール方法等を説明します。  

# インストール手順

Windows, Linux, MacOS 全てで手順は共通です。

## Node.jsをインストールする
Node.jsダウンロードページへ行き、LTS版をダウンロードします。

[https://nodejs.org/](https://nodejs.org/)

お使いのOSに合ったものをダウンロード候補に表示されます。

インストール手順はこちらを参考に。  
npmパッケージマネージャーはこのあと使用するので、インストールオプションから外さないようにしてください。  
環境変数PATHへの追加のオプションも外さないようにしてください。

うまくいきそうな参考サイトをピックアップしておいたので、なんとかうまくやってください。

- Windows: [Node.js / npmをインストールする（for Windows）](http://qiita.com/taipon_rock/items/9001ae194571feb63a5e)
- MacOS: [Macにnode.jsをインストールする手順。](http://qiita.com/akakuro43/items/600e7e4695588ab2958d)
- Linux: お使いのディストリに合わせた手順を行ってください。

コマンドプロンプト(端末・Terminal) にて、以下の2つのコマンドを打ち、バージョンが表示されたら次のステップへ進むことが出来ます。

```sh
node -v
npm -v
```

![Node.jsのバージョン確認](2017-03-19-00-28-04.png)

## goita-cli をインストールする

以下のコマンドを実行します。

```sh
npm install -g goita-cli
```

Windowsなら管理者権限、Linuxなら sudo が必要になるかもしれません。  

# アップデート手順

今後、コマンドツールに更新があった場合にすでにインストール済みの場合は以下のコマンドで最新化します。

```sh
npm update -g goita-cli
```

# アンインストール手順

ごいたコマンドのアンインストールには

```sh
npm uninstall -g goita-cli
```

Node.jsのアンインストールには、それぞれのOS毎のアンインストール手順を実行してください。

# 遊び方

以下のコマンドでゲームが起動します。コマンドプロンプト(端末・Terminal)の大きさはある程度縦長にしておかないと表示しきれません。
```sh
goita game
```

もし相方が5しの場合、**続行(continue-to-play)**か**配り直し(redeal)**の選択が表示されます。  
続行ならば、 y をタイプしてEnter  
配り直しならば、 n をタイプしてEnter  
で進めます。 

```txt
your partner has 5 shi
-----------------------
do you wish to play?
yes/no>
```

操作手順は、自分の番が回ってきたら、**受け駒選択**、または**なし**を入力します。  
キーボードを使って駒に対応した半角数字`1〜9`または、なしに対応する`0`を入力して、Enterキーを押します。

```txt
5: 金, 8: 王, 0: なし
select block koma>
```

**なし**以外を選択した場合は、続けて**攻め駒**を入力します。

```txt
5: 金, 8: 王, 0: なし
select block koma>5
1: し, 2: 香, 3: 馬
select attack koma>
```

# 対戦相手のコンピューターについて

現状のバージョン 0.0.5では非常に弱いです。  
手応えのあるやつらに出来るようにしたいので、強くするアイデアはいつでもお待ちしています。  
何かアイデアがありましたら、  

Twitter: [＠GoitaOnline](https://twitter.com/goitaonline)  

にメッセージをくれるとありがたいです。

また、コンピューターの実装は  
[https://github.com/Goita/goita-ai-sample-js](https://github.com/Goita/goita-ai-sample-js)  
にありますので、ご自由に改造してPullRequestいただけると嬉しいです。

# プログラムソースコード

githubの[**Goita Organization**](https://github.com/Goita)にソースコードを置いています。

ちょっとごいた関係のプログラムを書きたくなった・・・　そんな場合は

[Goita Core Library - https://github.com/Goita/goita-core-js](https://github.com/Goita/goita-core-js)

をご利用ください。
