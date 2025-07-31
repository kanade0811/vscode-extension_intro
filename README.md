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

今回は、テンプレートを作成して拡張機能を作っていきます

```
// `yo`と`yo code`を使えるようにするための作成コマンド
npm install -g yo generator-code
// 拡張機能を作成するためのテンプレートを作成する
yo code
```

→可愛いおじさんの質問にええ感じに答えていく  
　![カワおじ](./images/kawaozi.png)
以下、特に重要(と主が思っている)部分を抜粋

```
? What's the identifier of your extension?
// そのままエンター押せば何とかなる(らしい)
? Initialize a git repository? No
// gitリポジトリを作るならここ
// (既にリポジトリをクローンした中でy答えると二重になるから注意by前科1犯)
? Which package manager to use? npm
// ここはnpmを選択
```

ここまで入れるとぐわーって色々出てきます、待ちましょう  
![主のスクショ](./images/questions.png)

```
? Do you want to open the new folder with Visual Studio Code?
// 作成したテンプレを開くかの質問、そのままエンター
```

これで、無事に拡張機能のテンプレートを作成できました㊗


## 3.テンプレートの構造理解
では実際にコードを作っていきましょう！
……の前に、まず何が何なのかを知らないといけませんよね

以下がよく使うファイルの例です(じゃば)

`
package.json
`
→拡張機能の設定をするファイル。実は大事。
`
extension.js
`
→実際に拡張機能の処理を書くファイル。めっちゃ大事。