---
title: How to build Jekyll Site
layout: post
date: '2024-12-20 16:38:19'
categories:
- jekyll
---

After the build of ruby container, run

```
gem install jekyll bundler
gem install jekyll
```

Create a site

```
jekyll new edwardlu71.github.io
cd edwardlu71.github.io
```

Workaround problems

```
Gemfile:
group :jekyll_plugins do
  gem "sinatra", ">= 3", "< 4"
  gem "jekyll-admin"
  gem "jekyll-feed", "~> 0.12"
end

bundle install

Gemfile:
group :jekyll_plugins do
  gem "rackup"
  gem "jekyll-admin"
  gem "jekyll-feed", "~> 0.12"
end

bundle install
```

Startup of JekyII

```
bundle exec jekyll serve --host 0.0.0.0 &
```

Push to [Github](https://github.com/edwardlu71/edwardlu71.github.io)

It is accessibe from [Edward's doc site](https://edwardlu71.github.io/)
