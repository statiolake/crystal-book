# Bash on Ubuntu on Windows

Crystal は **まだ** Windows をサポートしていませんが、もし Windows 10 を使っているなら (実験的に) [Bash on Ubuntu on Windows](https://msdn.microsoft.com/en-us/commandline/wsl/about) を使って Crystal を使ってみることができます。Bash on Windows は Windows 上で動く Bash 環境です。インストールは [Debian / Ubuntu](on_debian_and_ubuntu.md) と同様ですが、いくつか気をつけるべき点があります。

いずれにせよ **とても実験的だ** ということは忘れないでください。

## レポジトリを設定する

まずはレポジトリを APT の設定に加えましょう。簡単に設定するには次のようにコマンドラインで入力してください。

```
curl -sSL https://dist.crystal-lang.org/apt/setup.sh | sudo bash
```

これで自動的に署名キーとレポジトリの設定が追加されます。もし手動で設定したければ、次のコマンドを **root 権限で** 実行してください。

```
sudo apt-key adv --keyserver keys.gnupg.net --recv-keys 09617FD37CC06B54
echo "deb https://dist.crystal-lang.org/apt crystal main" | sudo tee /etc/apt/sources.list.d/crystal.list
sudo apt-get update
```

## 依存関係

Crystal は C コンパイラ (`cc`) とリンカ (`ld`) を必要とするので、インストールする必要があります。

```
sudo apt-get install clang binutils
```

## インストール

レポジトリが設定されて依存関係をインストールしてしまえば、インストールの準備は完了です。

```
sudo apt-get install crystal
```

## アップグレード

新しいバージョンの Crystal がリリースされたら、次のようにしてアップグレードできます。

```
sudo apt-get update
sudo apt-get install crystal
```
