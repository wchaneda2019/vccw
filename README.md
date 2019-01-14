# VCCW for WordCamp Haneda 2019

このリポジトリは[WordCamp Haneda 2019]( https://2019.haneda.wordcamp.org/)のための開発環境[VCCW](http://vccw.cc/)です。

フォークしていますが、本家リポジトリとは独立して管理します。

## インストール方法

このリポジトリをクローンまたはダウンロードします。ディレクトリ内で`vagrant up`コマンドを入力します。vccwの動作要件については[マニュアル](http://vccw.cc/#h2-2)を参照してください。

```
vagrant up
```

動作が終わると、プラグインやサイトの設定がインポートされます。

## テーマのインストール

オリジナルテーマ`wch2019`もインストールできればよかったのですが、できませんでした。したがって、個別にインストールしてください。こちらはGitを利用します。

```
# テーマディレクトリまで移動
cd wordpress/wp-content/themes
# クローンする
git clone git@github.com:wchaneda2019/wch2019.git
# ビルドする
npm install && npm start
```

これでテーマはできたのですが、有効にする必要があるので、次のコマンドを入力してください。

```
# Vagrantの中に移動
vagrant ssh
# テーマを有効化
wp theme activate wct2019
```

## サイトへのアクセス

ローカルサイト`https://wchaneda2019.local`にはadmin/adminでログインすることができます。

## 問題報告

このリポジトリにイシューとして立ててください。担当者として @marubon を指定していただくと話が早いです。
