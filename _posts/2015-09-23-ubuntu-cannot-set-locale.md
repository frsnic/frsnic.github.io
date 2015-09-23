---
layout: post
title: "Ubuntu: Cannot set LC\_ALL to default locale"
description: "Ubuntu Cannot set LC\_ALL to default locale: No such file or directory"
category: note
tags: [ubuntu, locale]
---
{% include JB/setup %}

### Problem 
```$ sudo dpkg-reconfigure tzdata```   
perl: warning: Setting locale failed.   
perl: warning: Please check that your locale settings:   
  LANGUAGE = (unset),   
  LC\_ALL = (unset),   
  LC\_PAPER = "zh\_TW.UTF-8",   
  LC\_ADDRESS = "zh\_TW.UTF-8",   
  LC\_MONETARY = "zh\_TW.UTF-8",   
  LC\_NUMERIC = "zh\_TW.UTF-8",   
  LC\_TELEPHONE = "zh\_TW.UTF-8",   
  LC\_IDENTIFICATION = "zh\_TW.UTF-8",   
  LC\_MEASUREMENT = "zh\_TW.UTF-8",   
  LC\_TIME = "zh\_TW.UTF-8",   
  LC\_NAME = "zh\_TW.UTF-8",   
  LANG = "en\_US.UTF-8"   
    are supported and installed on your system.   
perl: warning: Falling back to the standard locale ("C").   
locale: Cannot set LC\_ALL to default locale: No such file or directory   
/usr/bin/locale: Cannot set LC\_ALL to default locale: No such file or directory
*** 
### Fix
```$ sudo locale-gen zh\_TW.UTF-8```   
Generating locales...   
  zh\_TW.UTF-8... done   
Generation complete.   

```$ sudo dpkg-reconfigure locales```   
Generating locales...   
  en\_US.UTF-8... done   
  zh\_TW.UTF-8... up-to-date   
Generation complete.
