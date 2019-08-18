---
tags: [lang/ruby]
title: ruby bundle
created: '2019-07-30T06:19:49.225Z'
modified: '2019-08-02T07:25:30.784Z'
---

# ruby bundle


```sh
bundle env

which bundle ruby gem

bundle list

bundler exec <gem>
```


### rake
> A make-like build utility for Ruby
```sh
bundle exec rake -T       # list rake tasks

bundle exec rake gitlab:env:info RAILS_ENV=production

bundle exec rake gitlab:backup:create RAILS_ENV=production      # /home/git/data/backups/ 

bundle exec rake gitlab:backup:restore RAILS_ENV=production

app:rake gitlab:backup:create
```
[GitHub - sameersbn/docker-gitlab](https://github.com/sameersbn/docker-gitlab/tree/e56b05963e86be76c6d17d9c6068a0d49e1e4306)