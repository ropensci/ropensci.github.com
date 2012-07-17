---
layout: page
title: Basic Installation Instructions

---


### API Keys

#### Q: Do all rOpenSci packages require an API key to use?

A: No, not all packages require an API key. The packages listed below
under the next question do require a key.

#### Q: Where do I obtain API Keys?

A: You will need to sign on at individual sources to obtain keys.

-   [Mendeley](http://dev.mendeley.com/applications/register/)
-   [PLoS](http://api.plos.org/registration/)
-   [Springer](http://dev.springer.com/page)
-   [Encyclopedia of Life](http://eol.org/users/register)
-   [uBio](http://www.ubio.org/index.php?pagename=form)
-   [Biodiversity Heritage
    Library](http://www.biodiversitylibrary.org/getapikey.aspx)

### Automatically loading keys on R startup

#### Q: How do I make keys load automatically when I launch R?

A: The best way to do this is to add the keys to your .rprofile

**Step 1**: Get your API key at a link above for the package of
interest.

**Step 2**: Create a text file called .rprofile in your home directory
([mac](http://cran.r-project.org/bin/macosx/RMacOSX-FAQ.html#The-R-Console))
([pc](http://cran.r-project.org/bin/windows/rw-FAQ.html#What-are-HOME-and-working-directories_003f))

In this file, add all of your API keys so it can be automatically read
by R during startup.

```r 
options(PlosApiKey= "YOUR_KEY") # PLoS  
options(BioHerLibKey="YOUR_KEY") # Biodiversity Heritage Library
options(MendeleyKey="YOUR_KEY")  # Mendeley
```

**Step 3**: When you open R, type in

```r Options() \# To verify individual keys, use the
getOption() function like so: getOption('MendeleyKey')
getOption('PlosApiKey') getOption('BioHerLibKey') ```

and you should see all of your API keys alongside other options.

### Installing packages

#### **Q: How do I install a package that's already on CRAN?**

A: Easy-peasy. Just go to CRAN to download and install from
Terminal/Shell, or download from within R.

#### **Q: How do I install a package that's just in development on GitHub?**

A: There are two options. The first option is:

**Step 1**: Sign up for a free account at GitHub (if you don't have one
already) [here](https://github.com/signup/free)

**Step 2**: Clone the repository/package you want to your local machine
(see [here](http://help.github.com/git-cheat-sheets/) for help on this)

**Step 3**: Load the functions in R using this generic format (change
the path for the specific package)

```r 
setwd('path/to/package/R') # the functions should be in the /R folder typically 
funcs <- as.list(dir()) # create list of function file names 
require(plyr) \# load plyr to use the functionl_ply 
l_ply(funcs, source) # loads each function in a loop 
```

And here's the second option, which may not work for all of our
packages, but it's worth a try as it's so easy!

**Step 1**: Install and load the devtools package by Hadley Wickham:

```r 
install.packages("devtools") 
require(devtools) 
```

**Step 2**: Use the install_github function from devtools to attempt to
install one of our packages directly from GitHub

```r 
install_github(repo = "nameofoneofourpackages", username = "username", branch = "master") 
# e.g., 
install_github(repo ="RMendeley", username = "ropensci") 
```

**Step 3**: Load the package

```r 
require(nameofoneofourpackages) 
```

#### Q: What if I don't want to get a GitHub account?

A: Just go to the site for the package of interest, and you can download
or copy/paste functions of interest. Also, you don't need a GitHub
account to use the second option above, installing with install\_github,
to install and try our packages.
