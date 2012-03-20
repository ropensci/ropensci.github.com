---
layout: post
title: "Welcome to rOpenSci"
category: 
tags: []
---
{% include JB/setup %}

### **rOpenSci** is a [collaborative effort](http://ropensci.org/wp-admin/project-overview/ "Profile") to develop R-based tools for facilitating Open Science.

## *So what is Open Science? *

Open science is the practice of making various elements of scientific
research -- data & methods, code & software, and results & publications
-- readily accessible to anyone. While this has great potential for
advancing research (in addition to education, public policy, &
commercial innovation) as a whole, there are both technical and social
challenges preventing this practice from being more widespread. Social
challenges stem largely from the dichotomy between what is best for an
individual researcher and what is best for the community. Technical
challenges arise largely from issues of scale: putting free print copies
of DNA sequencing data in a box in front of your office doesn't scale as
well as depositing those sequences on repositories like
[GeneBANK](http://www.ncbi.nlm.nih.gov/genbank/).
## *Why does open science need tools?*

Our goal is to provide open-source tools to help address both these
challenges. These are interesting times. The technology to facilitate
the access and utilization of this data has never been better, yet it is
only beginning to be employed. The internet -- firmly in its second
generation, the read-write Web 2.0 culture in which users generate
content as readily as they consume it -- has led to the explosion of
mechanisms for sharing. Yet these tools are not widely leveraged in
scientific communities [1](http://dx.doi.org/10.1038/nm1107-1276b).
## *Why R for open science?*

[R](http://www.r-project.org/) is an open-source statistical environment
that can be used for not only statistics, but also for data acquisition,
data manipulation, modeling, among other uses. R is increasingly being
used by scientists across all disciplines and has
[overtaken](http://www.tiobe.com/index.php/content/paperinfo/tpci/index.html)
popular scientific programming tools. Part of the reason behind R's
[explosive
growth](http://blog.revolutionanalytics.com/2010/01/r-package-growth.html)
is the ease with which the ever-growing userbase can add new
functionality, a fact evidenced by
[3,000+](http://cran.r-project.org/web/packages/) currently available R
packages. The R framework is ideal for open science because:
1.  The software is free.
2.  There is an extensive user community from which help is very quickly
    given, and
3.  The scientific workflow can be documented for fully [reproducible
    research](http://cran.r-project.org/web/views/ReproducibleResearch.html).

### Open Access Literature

Published literature is still the most common repository of scientific
information. While literature continues to expand exponentially, the
amount any individual researcher can consume[appears to be
constant](http://www.slideshare.net/CameronNeylon/science-in-the-open/90).
Whether discovering what to read, identifying research trends, or
summarizing existing work, scalable solutions require computational
approaches. [Mendeley](http://www.mendeley.com/), a citation tool,
literature repository, and social network which has just cataloged its
[100 millionth
paper](http://www.mendeley.com/blog/progress-update/mendeley-1-0-is-here/),
has released a [public API](http://apidocs.mendeley.com/) through which
it challenges the scientific community to leverage this data to
facilitate novel applications. [PLoS](http://www.plos.org/), The Public
Library of Science, has also joined the start-up with there own [public
API](http://api.plos.org/) allowing access to the metadata and full text
of all its publication through an accessible [RESTful
interface](http://en.wikipedia.org/wiki/Representational_State_Transfer).
### Open Data

Access to scientific data is rapidly emerging as a central theme in the
future of research [2](http://dx.doi.org/10.1126/science.331.6018.692). In our
field of Ecology and Evolution, new requirements for [data management
plans from NSF](http://www.nsf.gov/news/news_summ.jsp?cntn_id=116928),
data deposition requirements of [prominent
journals](http://datadryad.org/partners), and the emergence of
well-developed repositories like
[GeneBANK](http://www.ncbi.nlm.nih.gov/genbank/),
[Dryad](http://datadryad.org/),
[TreeBASE](http://www.treebase.org/treebase-web/home.html),
[DataONE](https://www.dataone.org/),
([KNB](http://knb.ecoinformatics.org/index.jsp),
[NBII](http://www.nbii.gov/portal/server.pt/community/nbii_home/236),
[GBIF](http://www.gbif.org/)) have opened a wealth of potential
[3](http://dx.doi.org/10.1126/science.1197962).
### Building Bridges between Open Access Literature and Open Data

Despite these dramatic shifts, the bulk of scientific research has been
slow to benefit from the transformation than they are to comply with the
new requirements. To address these challenges, we have set about
building bridges between the repositories and the open source R
statistical environment. We are creating packages that allow access to
these data repositories through a statistical programming environment
that is already a familiar part of the workflow of many scientists. We
hope that these bridges will not only facilitate drawing data into an
environment where it can readily be manipulated, but also one in which
those analyses and methods can be easily shared, replicated, and
extended by other researchers. Keep up with updates on the rOpenSci
project here and on [twitter](http://twitter.com/#!/ropensci "Tweets").

