---
layout: page-fullwidth
title: "Build with Feeling Responsive template"
subheadline: ""
teaser: "Feeling Responsive allows you to use all kinds of headers. This header is with text."
categories:
    - myblog
tags:
    - myblog
    - jekyll

header:
    title: Feeling Responsive Template
    background-color: "#EFC94C;"
#    pattern: pattern_concrete.jpg
    image_fullwidth: unsplash_brooklyn-bridge_header.jpg
    caption: This is a caption for the header image with link
    caption_url: https://unsplash.com/
---
<!--more-->

## Front Matter Code

### 1. Create Github Page Repository

See [Github Pages](https://pages.github.com/)

### 2. Download Feeling Responsive Jekyll Template

#### Download [Feeling Responsive Template](https://github.com/Phlow/feeling-responsive) to other folder.

```
$ git clone https://github.com/Phlow/feeling-responsive.git
```
#### Copy all files to your Github pages

```
$ cp -r ./feeling-responsive ./klitever.github.io
$ cd ./klimtever.github.io
$ gem install bundler
$ bundle install
```

### 3. Config for your pages
Move to your GitHub repo.

#### Change URLs

* Open and Edit `_config.yml`
```
# This URL is the main address for absolute links. Don't include a slash at the end.
#
url: 'https://klimtever.github.io'
baseurl: ''
```
* Submit to the repository
```
$ git add .
$ git commit -m "Change URLs"
$ git push
```

#### Visit your Page from a browser, for example, `https://klimtever.github.io/`

### 4. Build your site locally
1. Open Terminal.
```
$ cd ./klimtever.github.io
$ bundle exec jeyll serve
/Users/klimtever/.rvm/gems/ruby-2.7.0/gems/sassc-2.2.1/lib/sassc/engine.rb:34: warning: rb_safe_level will be removed in Ruby 3.0
                    done in 1.248 seconds.
 Auto-regeneration: enabled for '/Users/klimtever/playground/myblog/klimtever.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```
2. Open web brwoser with `http://localhost:4000`


~~~
header:
    title: header with text
    image_fullwidth: unsplash_brooklyn-bridge_header.jpg
    caption: This is a caption for the header image with link
    caption_url: https://unsplash.com/
~~~

<!-- ### All Header-Styles 
{: .t60 } -->

{% include list-posts tag='myblog' %}