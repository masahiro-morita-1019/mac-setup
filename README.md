# mac-setup
mac立上のためのインストールスクリプトや手順をまとめる

# 1.パッケージ管理システム(Homebrew)のインストール
## 1.1 コマンドライン・デベロッパツールのインストール
## 1.2 xcodeをコマンドラインでインストール
Homebrewを使うにはxcodeが必要.
以下のコードを実行すればよい。が、そこで1.1の作業が必要と言われた

```
$ xcode-select --install
```
## 1.3 Homebrewインストール
https://brew.sh/index_ja に記載のスクリプトを流す

```
2022/9/7現在
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### memo
・カーソル速度を上げる => コード書けそう
