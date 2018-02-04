# プログラミング言語 Crystal

これはプログラミング言語 Crystal のリファレンスです。

Crystal の目標は、

* Ruby に似た文法を持つこと。 (ただし、互換性は目標ではありません)
* 静的に型検査をする一方で、変数やメソッドの引数で型を明示しなくてよくすること。
* Crystal 言語でバインディングを書いて C 言語のコードを呼び出せるようにすること。
* 時にコンパイル時に評価やコードの生成を行い、ボイラープレートなコードを減らすこと。
* 効率的なネイティブコードへコンパイルすること。

です。

## リファレンスへの貢献

このリファレンスのバグを見つけた時や、もっと分かりやすくできる部分を見つけた時はぜひ助けてください。プルリクエストは次のレポジトリへ。
<http://dummy/>

よろしくお願いします。

### ローカル環境でのビルド・テスト

```
$ git clone https://github.com/crystal-lang/crystal-book.git
$ cd crystal-book
$ npm install -g gitbook-cli@2.3.0
$ npm install
$ gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 8 plugins are installed
info: loading plugin "ga"... OK
...
Starting server ...
Serving book on http://localhost:4000

```

`_book` フォルダに HTML ファイルが出力されます。ローカルでファイルを開いていると、リンクの一部が正しく設定されない可能性があります。依存関係をグローバルにインストールするのが嫌なときは、 docker 環境も用意しています。

```
$ docker-compose up
...
gitbook_1  | Starting server ...
gitbook_1  | Serving book on http://localhost:4000
gitbook_1  | Restart after change in file node_modules/.bin
...
```

### ページの追加

ページを追加するには、好きなところに Markdown のファイルを作成してください。例えば `overview/hello_world.md` など。その後、そのファイルへのリンクを `SUMMARY.md` に追加してください。このファイルがリファレンスのナビゲーションバーになります。
