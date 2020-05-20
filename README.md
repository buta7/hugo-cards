# README

## セットアップ

サイト作成

```shell
hugo new site hugo-cards
```

レポジトリ初期化

```shell
cd hugo-cards
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
echo '.env' >> .gitignore
```

テーマ設定

```shell
cd themes 
git submodule add git@github.com:bul-ikana/hugo-cards.git
```

サイト設定

```shell
cd hugo-cards
cp -pr themes/hugo-cards/exampleSite/{content,config.toml} .
cp -pr themes/hugo-cards/{layouts,static,archetypes} .
```

config.toml

```toml
baseURL = "https://higebobo.github.io/hugo-cards/"
languageCode = "ja"
title = "Hugo Cards"
publishDir = "docs"
#themesDir = "../.."
paginate = 6

```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:higebobo/hugo-cards.git
cp somplace/Makefile
git add .
git commit -m 'init'
git push -u origin master
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:higebobo/hugo-cards.git higebobo-cards
cd higebobo-cards
git submodule update --init --recursive
```

## 使い方

### 投稿

新規投稿

```shell
hugo new posts/hello.md
content/posts/hello.md created
```

編集

```shell
vi content/posts/hello.md
```

### ポートフォリオ

```shell
vi data/artworks.toml
```

## Link

* [Hugo Cards \| Hugo Themes](https://themes.gohugo.io/hugo-cards/)
