---
layout: post
title:  "Upgrading R on Mac and migrating libraires"
date:   2015-10-27 
author: Allen Y. Lin
categories: R
---
This post is migrated from my old blog as it helped me today to solve the exact R upgrading problem. 

Updating R usually involves two things: 1) update R per se, 2) update the libraries/pakcages.

###1. Update R per se

First delete the old version:
```
rm -rf /Library/Frameworks/R.framework /Applications/R.app
rm -rf /Library/Receipts/R-*
```
Second, install the new version from CRAN. Find the suitable version in either src or binary

###2. Migrating the libraries
In your home directory:
```
mkdir Rlibs
nano .Reviron
```
Type in:
`R_LIBS=~/Rlibs`
