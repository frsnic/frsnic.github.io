---
layout: post
title: "Ubuntu share NTFS partition"
description: ""
category: note
tags: [ntfs, ubuntu]
---
{% include JB/setup %}
```
sudo ntfs-3g -o uid=1000,gid=1000 /dev/sda3 ntfs
```
