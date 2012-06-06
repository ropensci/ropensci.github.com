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


Jekyll Extensions 
-----------------

The site relies on serveral extensions not available on the Jekyll copy provided on Github's gh-pages.  

* redcarpet2 -- Providing support for [Github-flavored markdown](http://github.github.com/github-flavored-markdown/)
* feedzirra -- Grab and format rss feed information  



