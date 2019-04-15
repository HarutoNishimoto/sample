# sample
随時，gitについてのメモを書き足していってください．

追加１
追加２
ついか３


クローンからプルしてマージ、コミットしてプッシュする

# とりあえずすればいいこと（3手順）

## 1.作業ディレクトリで変更したファイルを索引（index）に追加（コミット準備、管理対象にする）
git add sample2.py
git add .

## 2.変更内容をコミット
git commit -m "コメント"
変更したものに対してコメントがつく
これで変更内容が索引からコミットされ、HEADに格納されました。
まだ共有リポジトリには反映されていないことに注意して下さい。

## 3.共有リポジトリに反映
編集内容がローカルの作業ディレクトリ内でHEADに格納されています。
あなたの変更を共有リポジトリに反映させる必要があります。
反映させるために利用するコマンドは push(プッシュ)です。
git push
git push origin master
ローカルブランチ「master」を、リモートレポジトリ「origin」上の同名のブランチに反映する

origin は共有リポジトリを指し示す名前です。
コマンドの解釈として、「マスタブランチにコミットされた HEAD の内容を共有リポジトリに送信する」となります。

masterはローカルのHEADのことで
originは共有リポジトリのこと

# その他のコマンド

git pull
あなたの作業ディレクトリを最新のコミットに更新する
この操作は共有リポジトリの最新情報を取得し、作業ディレクトリの状態に統合(merge)します。


# 単語いろいろ

## 大事な３要素

###１．作業ディレクトリ(Working Directory)
共有リポジトリ(リモートリポジトリ)と同じファイルがローカルに展開され、ファイルの追加修正を行うディレクトリ

###２．索引(Index)
コミットするためにファイルを索引に追加し、コミット予定のファイル群を記録します。
このコミット対象のファイルを索引に追加する操作は、「ステージング」「コミット予定」「管理対象」と言われます。

###３．作業最後のコミットを指す HEAD
git は作業ディレクトリでコミットが行われると master ブランチと呼ばれる作業ディレクトリを作ります。master ブランチは直近のコミットを指し示す意味を持っています。この後コミットを繰り返す度に master ブランチの指し示す場所は進んでいきます。HEAD とは作業ディレクトリでコミットされた最後のコミットを指すことを意味すると覚えておいて下さい。

共有リポジトリ
みんなで編集できる場所
これはweb上のあれをさす

作業ディレクトリ（ワーキングディレクトリ）
作業ディレクトリとは、共有リポジトリから取得したローカル環境のリポジトリです。

コミット
「コミット」は新規作成したファイルや編集したファイルを保存することを意味しています。

https://tracpath.com/bootcamp/learning_git_firststep.html

master ブランチは直近のコミットを指し示す意味を持っています。


プル
共有リポジトリはあなた以外の開発メンバーもコミット・プルします。
他のメンバーが追加した機能や修正したファイルを自分の作業ディレクトリに取り込むことができます。
この操作をプル(pull)と言います。

# remote関連
git remote add <name> <url>
リモートリポジトリを追加

git remote -v
リモートリポジトリの一覧がでる


