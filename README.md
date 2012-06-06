Source Code for ropensci.org 
=============================

**Primary server for site**: [ropensci.org](http://ropensci.org), hosted by [A Small Orange](http://asmallorange.com)

This hosts only the compiled html files of the site. The original Jekyll source used to produce the site is [found here on Github](https://github.com/ropensci/ropensci.github.com) on the [source branch](https://github.com/ropensci/ropensci.github.com/tree/source), a mirror of the site is found on the [master branch](https://github.com/ropensci/ropensci.github.com/tree/master), which renders at [ropensci.github.com](http://ropensci.github.com)

Installing and Jekyll and plugins required to compile the site
--------------------------------------------------------------

(These instructions are based on my Ubuntu 12.04 platform.)


Install Ruby version >= 1.9

```
sudo apt-get install ruby1.9.1-full
```

Make sure the [latest version is selected](http://askubuntu.com/questions/91693/how-do-you-uninstall-ruby-1-8-7-and-install-ruby-1-9-2)

```
sudo update-alternatives --config ruby
sudo update-alternatives --config gem
```

Install Jekyll and the dependencies needed for a few plugins.

`sudo gem install jekyll redcarpet feedzirra`


In the root directory of the project, run `jekyll --server`, if successfull, after a few seconds the site should be available by pointing your browser to `localhost:4000`.  


### Working with source on Github 

Make sure to develop on the source branch,

```
git checkout source
```

and push changes to the source branch on Github 

```
git push origin source
```

The easiest way to update the ropensci.github.com copy is perhaps to clone a second copy of the site and keep it switched to the master branch.  Then just copy the contents of `_site/` directory, after running jekyll, into the master branch to update it.  



Creating pages and posts
------------------------

New posts must be created in the `_posts` directory, and must begin with date in yyyy-mm-dd format, followed by the post title (or short version of the title).  Posts are written in markdown, and just need a minimal YAML header to control metadata, such as:

```
---
layout: post
title: my clever title
subtitle: is optional
tags: [optional, in brackets, for multiple]
categories: [optional, in brackets, for multiple]
---
```


See the [Jekyll project wiki](https://github.com/mojombo/jekyll/wiki) for details.  

Pages are created in the same way but in the root directory, but don't need the date and don't get tags and categories.   Set `layout: default` for pages.  Layouts are defined in the `_layout` directory, which assembles the layout from html blocks that are kept in `_includes` directory (i.e. so you can reuse the same header or footer across multiple layouts).  


Jekyll Extensions 
-----------------

The site relies on serveral extensions not available on the Jekyll copy provided on Github's gh-pages.  

* redcarpet2 -- Providing support for [Github-flavored markdown](http://github.github.com/github-flavored-markdown/)
* feedzirra -- Grab and format rss feed information  



