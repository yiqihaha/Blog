---
title: IDEA使用
date: 2017-01-12 15:23:03
tags:
---

##  IDEA使用 

#### @Autowired和@Resource时报错

使用IDEA工具时使用@Resource和@Autowired自动注解bean时会显示红色，但是项目能运行。
解决方法： 
```
File – Settings – Inspections。
在spring Core – Autowring for Bean Class 中将Severity的级别由之前的error改成warning。
```