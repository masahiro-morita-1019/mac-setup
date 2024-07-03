# mac-setup
mac立上のためのインストールスクリプトや手順をまとめる

# 1.パッケージ管理システム(Homebrew)のインストール
## 1.1 コマンドライン・デベロッパツールのインストール
## 1.2 xcodeをコマンドラインでインストール
Homebrewを使うにはxcodeが必要.
以下のコードを実行すればよい。が、そこで1.1の作業が必要と言われた

```
xcode-select --install
```
## 1.3 Homebrewインストール
https://brew.sh/index_ja に記載のスクリプトを流す

```
2022/9/7現在
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
インストールすると以下環境変数の設定を要求されるので、端末に合わせて設定

```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> Users/masahiro.morita/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
GUIパッケージのインストールには brew install xxx --caskを使う。昔は brew cask install xxxだった模様。


# 2. Ansibleのインストール
Ansibleはインフラの構成管理とOSやソフトウェアなどの設定作業を自動化するツールです。yamlに各resourceの設定を記述して実行することで、その構成通りに構築を行うことができます。
```
brew install ansible
```
Ansibleの概要はhttps://tech.prog-8.com/entry/2021/12/19/setup-mac-ansible を参照

・本リポジトリをclone ※passwordはアクセストークンにする必要があり
その後cloneしたプロジェクトのrootディレクトリで以下実行
```
ansible-playbook playbook.yml -K
```
### memo
・トラックパッド、マウスの速度を上げる
・トラックパッドの向き、キーボードのリピート速度向上
=> コード書けそう
