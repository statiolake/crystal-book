# Linux (Linuxbrew)

Linux に Crystal を簡単にインストールするには、 [Linuxbrew](http://linuxbrew.sh/) を使う手があります。

```
brew update
brew install crystal-lang
```

もし言語そのものに貢献しようと考えているなら LLVM を同時にインストールするとよいかもしれません。最後の行を次のように書き換えてください。

```
brew install crystal-lang --with-llvm
```
