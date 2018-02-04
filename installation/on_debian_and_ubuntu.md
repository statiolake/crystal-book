# Debian / Ubuntu

Debian 系のディストリビューションでは、公式 Crystal レポジトリを利用できます。

## レポジトリを設定する

まずはレポジトリを APT の設定に加えましょう。簡単に設定するには次のようにコマンドラインで入力してください。

```
curl https://dist.crystal-lang.org/apt/setup.sh | sudo bash
```

これで自動的に署名キーとレポジトリの設定が追加されます。もし手動で設定したければ、次のコマンドを **root 権限で** 実行してください。

```
apt-key adv --keyserver keys.gnupg.net --recv-keys 09617FD37CC06B54
echo "deb https://dist.crystal-lang.org/apt crystal main" > /etc/apt/sources.list.d/crystal.list
apt-get update
```

## インストール

レポジトリが設定されてしまえば、インストールの準備は完了です。

```
sudo apt-get install crystal
```

場合によっては、Crystal のプログラムをコンパイル・実行するために、パッケージ `build-essential` が[必要になることがあります](https://github.com/crystal-lang/crystal/issues/4342)。このパッケージは次のコマンドでインストールすることができます。

```
sudo apt-get install build-essential
```


## アップグレード

新しいバージョンの Crystal がリリースされたら、次のようにしてアップグレードできます。

```
sudo apt-get update
sudo apt-get install crystal
```
