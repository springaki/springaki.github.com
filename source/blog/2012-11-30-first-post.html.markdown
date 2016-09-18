---
layout: post
title: "Octopressを使ってみる"
date: 2012-11-30 18:29
comments: true
categories:
---

[Octopress](http://octopress.org/) を使ってBlogを書いてみる。

> "Create a new Github repository and name the repository with your user name or organization name username.github.com or organization.github.com."

と書かれているとおり、githubのユーザ名が組織アカウント名でリポジトリを作らなければいけない。
ユーザ名.github.com というリポジトリを作る。

リポジトリの場所を指定

```
    rake setup_github_pages
```
リポジトリを指示通りの形式で入力。

Blogの枠を生成してデプロイする。

```
    rake generate
    rake deploy
```
