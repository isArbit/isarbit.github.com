---
layout: post
title: "rake preview shows a blank page in Safari 7"
date: 2014-02-26 10:10:52 +0800
comments: true
categories: shell
---

When I was deploying this blog and trying to preview with command:

```
$ rake prview
```

I found out that safari shows a blank page for me with the default URL:<code>http://localhost:4000</code>.


That's pretty strange actually. After googling for a minute, I found a solution
in [here](https://github.com/imathis/octopress/issues/1395).
[@chengyanlai](https://github.com/chengyanlai) gives an solution taht install
`thin` to gem file could make it work. The following commands are:

```
$ echo gem \"thin\" >> Gemfile
$ bundle install
```

After installation, everything works!
