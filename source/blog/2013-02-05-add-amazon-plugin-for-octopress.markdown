<!-- ---
layout: post
title: "Amazon plugin を追加する"
date: 2013-02-05 15:24
comments: true
categories:
--- -->

gem install
	$ gem install ruby-aaws

{% codeblock Gemfile add ruby-aaws - Gemfile %}
	gem 'ruby-aaws'
{% endcodeblock %}


octopress の pluginディレクトリに以下のソースを入れる

[Mr. Janssen’s plugin from Github.](https://github.com/jamuraa/base0.net/blob/master/_plugins/amazon_liquid_tags.rb)

	$ curl https://raw.github.com/jamuraa/base0.net/master/_plugins/amazon_liquid_tags.rb > plugins/amazon_liquid_tags.rb


Homeディレクトリに設定ファイルを追加

{% codeblock setting config - ~/.amazonrc %}
key_id = 'YOUR-ACCESS-KEY-GOES-HERE'
secret_key_id = 'YOUR-SECRET-KEY-GOES-HERE'
associate = 'aktone-22'	# アソシエイトID
cache = false
locale = 'jp'
encoding = 'UTF-8'
{% endcodeblock %}

使い方

{% gist 4712786 %}

こんなふうに表示される

{{ "4048687158" | amazon_medium_image }}
{{ "4798122971" | amazon_medium_image }}


参照
[http://zanshin.net/2011/08/24/amazon-plugin-for-octopress/](http://zanshin.net/2011/08/24/amazon-plugin-for-octopress/)
