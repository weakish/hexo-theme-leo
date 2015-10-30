---
layout: post
title:  邮件的IMAP和POP协议，在iPad的邮件登录QQ邮箱
date:   2015-10-21 08:24:00
category: [Mac]
tags: [Mac,iOs,iPad]
---

如果直接在邮件中登录QQ邮箱，会提示密码错误。因为要先到QQ邮箱开启IMAP服务（或POP3服务），使用独立密码，才可以登录。

<!--more-->

## 开启QQ邮箱IMAP服务
登录网页QQ邮箱，`设置——账号——POP3/IMAP/SMTP/Exchange/CardDAV/CalDAV服务——开启IMAP/SMTP服务`。

![开启IMAP/SMTP服][1]

根据提示设置独立密码，以后登录第三方应用就使用这个独立密码。

## 登录iPad的邮件应用

打开iPad的邮件应用登录，密码使用钢设置的独立应用。接收邮件服务器：`imap.qq.com`，发送邮件服务器：`smtp.qq.com`

如果上一步开启的是POP3方式，接收邮件服务器写：`pop.qq.com`

如果已经登录了其他邮箱，就到`系统设置——邮件账号——添加新账号`。

##拓展

###POP3是什么？
POP3，全名为“Post Office Protocol - Version 3”，即“邮局协议版本3”。是TCP/IP协议族中的一员，由RFC1939 定义。本协议主要用于支持使用客户端远程管理在服务器上的电子邮件。提供了SSL加密的POP3协议被称为POP3S。

POP 协议支持“离线”邮件处理。其具体过程是：邮件发送到服务器上，电子邮件客户端调用邮件客户机程序以连接服务器，并下载所有未阅读的电子邮件。这种离线访问模式是一种存储转发服务，将邮件从邮件服务器端送到个人终端机器上，一般是PC机或 MAC。一旦邮件发送到 PC 机或MAC上，邮件服务器上的邮件将会被删除。但目前的POP3邮件服务器大都可以“只下载邮件，服务器端并不删除”，也就是改进的POP3协议。

###IMAP是什么？
IMAP，即Internet Message Access Protocol（互联网邮件访问协议），你可以通过这种协议从邮件服务器上获取邮件的信息、下载邮件等。它的主要作用是邮件客户端（例如MS Outlook Express)可以通过这种协议从邮件服务器上获取邮件的信息，下载邮件等。当前的权威定义是RFC3501。IMAP协议运行在TCP/IP协议之上，使用的端口是143。
 
###IMAP和POP有什么区别？
IMAP和POP3协议的主要区别是用户可以不用把所有的邮件全部下载，可以通过客户端直接对服务器上的邮件进行操作。

POP允许电子邮件客户端下载服务器上的邮件，但是你在电子邮件客户端的操作（如：移动邮件、标记已读等），这是不会反馈到服务器上的，比如：你通过电子邮件客户端收取了QQ邮箱中的3封邮件并移动到了其他文件夹，这些移动动作是不会反馈到服务器上的，也就是说，QQ邮箱服务器上的这些邮件是没有同时被移动的 。

但是IMAP就不同了，电子邮件客户端的操作都会反馈到服务器上，你对邮件进行的操作（如：移动邮件、标记已读等），服务器上的邮件也会做相应的动作。也就是说，IMAP是“双向”的。同时，IMAP可以只下载邮件的主题，只有当你真正需要的时候，才会下载邮件的所有内容。

  [1]: http://77g54f.com1.z0.glb.clouddn.com/QQ20151012163142.png