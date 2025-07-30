# vscode-extension_intro

この講座では、主に自身のコーディングの手助けとなるような拡張機能の作成と使用を目的としています。  
~~ちなみに主は作成を途中で放棄して半ば諦めています~~



## 目次
1. Node.jsのDLとinst  
2. 雛型の作成
3. 



## 1.Node.jsのDLとinst

[https://nodejs.org/ja/download](https://nodejs.org/ja/download)からLTS版をDLする。

> [!NOTE]
> そのほかの設定はそのままで大丈夫(多分)

その後、インストーラーでインストールする。

> [!TIP]
> ターミナルに以下のコマンドを1行ずつ打ち込む
> ```
> node -v
> pnm -v
> ```
> それぞれバージョンが表示されれば正しく入っている
> そうでなければ上手く入っていないため、良い感じに頑張ってください



## 2.雛型の作成

```
// `yo`と`yo code`を使えるようにするための作成コマンド
npm install -g yo generator-code
// 拡張機能を作成するためのテンプレートを作成する
yo code
```
→可愛いおじさんの質問にええ感じに答えていく  
　![カワおじ](./images/kawaozi.png)

```
// 拡張機能の型を聞いてる、私はjsしかできないのでそれ選びました
? What type of extension do you want to create?
// 拡張機能の名前を入力
? What's the name of your extension?
// そのままエンター押せば何とかなる(らしい)
? What's the identifier of your extension?
// 拡張機能の説明
? What's the description of your extension?
// ここはyで良いらしい(ってチャッピーが)
? Enable JavaScript type checking in 'jsconfig.json'?
// gitリポジトリを作るならここ
// 既にリポジトリをクローンした中でy答えると二重になるから注意by前科1犯
? Initialize a git repository? No
// ここはnpmを選択
? Which package manager to use? npm
```

ここまで入れるとぐわーって色々出てきます、待ちましょう  
![主のスクショ](./images/questions.png)

```
// 開く？って質問、そのままエンター
? Do you want to open the new folder with Visual Studio Code?
```

これで、無事に拡張機能のテンプレートを作成できました㊗