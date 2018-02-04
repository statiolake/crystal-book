# Mac OSX (Homebrew)

Mac に Crystal を簡単にインストールするには、 [Homebrew](http://brew.sh/) を使う手があります。

```
brew update
brew install crystal-lang
```

もし言語そのものに貢献しようと考えているなら LLVM を同時にインストールするとよいかもしれません。最後の行を次のように書き換えてください。

```
brew install crystal-lang --with-llvm
```

## OSX 10.11 (El Capitan) でのトラブルシューティング

もし次のようなエラーが出たら

```
ld: library not found for -levent
```

コマンドラインツールを再インストールしてデフォルトのツールチェインを洗濯する必要があります。

```
$ xcode-select --install
$ xcode-select --switch /Library/Developer/CommandLineTools
```
