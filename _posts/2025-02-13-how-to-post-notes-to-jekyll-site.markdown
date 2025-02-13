---
title: How to Post Notes to Jekyll Site
layout: post
date: '2024-02-13 00:00:00'
categories:
- jekyll
---

Create a github token if you don't have, and enable repo functions

```
https://github.com/settings/tokens
```

Bring up Jekyll container, clone github Jekyll project to /srv/jekyll/, remove _posts from .gitignore

```
~/workshop/jekyll/srv$ git clone https://github.com/edwardlu71/edwardlu71.github.io.git
```

Bring up Jekyll process in the container

```
root@53cb163793c3:/srv/jekyll/edwardlu71.github.io# bundle exec jekyll serve --host 0.0.0.0 &
```

Create a note

```
vi _draftes/2025-02-13-how-to-post-notes-to-jekyll-site.markdown
mv _draftes/2025-02-13-how-to-post-notes-to-jekyll-site.markdown _posts/
```

At this point, we can see the note from local server. 

To post the change to git doc site

```
~/workshop/jekyll/srv$ git add .
~/workshop/jekyll/srv$ git commit -m "posting new notes"
~/workshop/jekyll/srv$ git push

(with username and token)
```

Push to [Github](https://github.com/edwardlu71/edwardlu71.github.io)

It is accessibe from [Edward's doc site](https://edwardlu71.github.io/)
