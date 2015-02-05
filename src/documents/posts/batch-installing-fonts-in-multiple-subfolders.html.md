---
title: Batch installing fonts in multiple subdirectories
author: 'Devon Zuegel'
tags: ['mac', 'fonts', 'batch', 'install', 'command line']
collection: posts
date: 'February 2 2015'
img: 'http://i.stack.imgur.com/o76m6.png'
---

I'm a digital pack rat, especially when it comes to fonts. Every time I see a nice typeface, I immediately forget whatever it is I'm actually reading and instead dig into the source code, find its name, and search the corners of the web for a a free copy. It doesn't help that my favored form of procrastination is scrolling through pages upon pages of fonts on sites like [MyFonts.com](https://www.myfonts.com/) and [FontSquirrel.com](http://www.fontsquirrel.com/). The result is that I frequently find myself with a mess of directories bloated with `.ttf` and `.otf` files. <img src='http://i.imgur.com/VTK3tEG.png' width='270px' style='float:right; margin:15px'/>

The sad hangover to my embarrassingly frequent font binges is actually installing them. OSX has no easy way to get multiple fonts into Font Book all at once, leaving you with the painful task of installing them by hand, one by one. It's particularly unpleasant when the files are in multiple subfolders, the common format of the downloaded bundles I love so much.

Luckily, it's easy to install all fonts within the subfolders of a directory from the command line with the following steps:

1. First, **locate the parent directory** of all of the font files you wish to install. In my case, the directory is `~/Downloads/fonts-to-install`.

2. Next, **open your terminal** and **enter the following command** to install the fonts directly into Font Book. If you are dealing with `.otf` s or some other file type, replace `"*.ttf"` with `"*.otf"`.

``` bash
find ~/Downloads/fonts-to-install\ Fonts/ -name "*.ttf" -exec cp -iv {} /Library/Fonts \;
```

And that's that! Go use your newly-saved font-installing time for something fun.