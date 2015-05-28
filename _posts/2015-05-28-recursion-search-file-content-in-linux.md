---
layout: post
title: "Recursion search file content in Linux"
description: ""
category: note
tags: [ubuntu]
---
{% include JB/setup %}
```
grep --color=auto -nH 'DIR' *
```
-n, --line-number
      Prefix  each  line of output with the 1-based line number within its input file.  (-n is specified by POSIX.)

-H, --with-filename
      Print  the  file  name for each match.  `This is the default` when there is more than one file to search.

*, file path

