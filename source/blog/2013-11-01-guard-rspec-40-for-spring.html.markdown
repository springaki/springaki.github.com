---
layout: post
title: "Guard::RSpec 4.0から :spring オプションはdeprecated"
date: 2013-11-01 18:45
comments: true
categories:
---

Guardでspringを使用する時に今までは

    guard :rspec, spring: true do
      # ...
    end

と書いていましたが、
Guard::RSpec 4.0 からは :spring オプションは非推奨になっていて実行時にwarningが出るようになります。4.0以降は :cmd オプションを使うのが良いみたいです。

    # Guardfile
    guard :rspec, cmd: 'spring rspec -f doc' do
      # ...
    end


Guard::RSpec 4.0で表示されるwarningはこんな感じ。

    Guard::RSpec DEPRECATION WARNING: The :spring option is deprecated. Please customize the new :cmd option to fit your need.


[https://rubygems.org/gems/guard-rspec](https://rubygems.org/gems/guard-rspec)

Guard::RSpec Versions

- 4.0.3 October 18, 2013
- 4.0.2 October 17, 2013
- 4.0.1 October 14, 2013
- 4.0.0 October 11, 2013
- 3.1.0 September 22, 2013
