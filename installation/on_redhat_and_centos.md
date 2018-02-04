# RedHat / CentOS

RedHat 系のディストリビューションでは、公式 Crystal レポジトリを利用できます。

## レポジトリを設定する

まずはレポジトリを YUM の設定に加えましょう。簡単に設定するには次のようにコマンドラインで入力してください。

```
curl https://dist.crystal-lang.org/rpm/setup.sh | sudo bash
```

これで自動的に署名キーとレポジトリの設定が追加されます。もし手動で設定したければ、次のコマンドを実行してください。

```
rpm --import https://dist.crystal-lang.org/rpm/RPM-GPG-KEY

cat > /etc/yum.repos.d/crystal.repo <<END
[crystal]
name = Crystal
baseurl = https://dist.crystal-lang.org/rpm/
END
```

## インストール

レポジトリが設定されてしまえば、インストールの準備は完了です。

```
sudo yum install crystal
```

## アップグレード

新しいバージョンの Crystal がリリースされたら、次のようにしてアップグレードできます。

```
sudo yum update crystal
```
