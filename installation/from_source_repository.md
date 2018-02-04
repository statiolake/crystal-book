# ソースから

もし言語に貢献したいと思ってくださるなら、 Crystal をソースからインストールしたいかもしれません。

1. [Crystal の最新版リリースをインストールする](https://crystal-lang.org/docs/installation). Crystal をコンパイルするのには Crystal が必要なのです。(^_-)

2. パスにサポートされているバージョンの LLVM がインストールされていることを確認してください。現在のところ、 Crystal は LLVM 3.8, 3.9 と 4.0 をサポートしています。可能なら、最新のものを使ってください。もし Mac で Homebrew を使っているのなら、 Crystal をインストールするときに `--with-llvm` オプションを付けると自動的に設定されます。

3. [必要な全てのライブラリ](https://github.com/crystal-lang/crystal/wiki/All-required-libraries) がインストールされていることを確認してください。[貢献ガイド](https://github.com/crystal-lang/crystal/blob/master/CONTRIBUTING.md) も読みましょう。

4. リポジトリをクローンしてください。

```
git clone https://github.com/crystal-lang/crystal.git
```

5. コンパイラをビルドするために `make` コマンドを実行してください。
6. `make spec` とすると全部の仕様をパスしているか、と、全てのものが適切にインストールできているかを確認できます。
7. `bin/crystal` がビルドされたバイナリです。

新しい `bin/crystal` についてもっと知りたければ [コンパイラを使う](https://crystal-lang.org/docs/using_the_compiler/) をチェックしてください。

注意: 実際のバイナリは `.build/crystal` にビルドされますが、実行するべきなのはラッパースクリプトの `bin/crystal` です。
