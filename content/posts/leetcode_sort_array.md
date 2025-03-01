---
title: "Let's sort it out!"
date: 2025-02-27T16:03:00+01:00
# weight: 1
# aliases: ["/first"]
tags: ['coding','leetcode','quicksort', 'two-way-partition', 'three-way-partition' ]
author: ["Mainak Mandal"]
katex: true
showToc: true
TocOpen: false
draft: true
hidemeta: false
comments: false
description: "The Staircase Paradox"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---
#  Intro

Let's talk about a very simple looking problem on Leetcode, called [912. Sort An
Array](https://leetcode.com/problems/sort-an-array/description/). I knew
bubble sort and quicksort from my Data Structure classes from IISER Kolkata days,
of course most of the course was on taught on paper. But I knew QuickSort was
$ O(log(n))$. So, I revised my quicksort and got to work. It was quite easy and was passing the given tests. But I was hit with `test failed`.

