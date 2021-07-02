---
title: "首届 Go 语言中国贡献者峰会回顾"
date: 2021-06-29T19:00:00Z
description: 首届 Go 语言中国贡献者峰会回顾
image: "/images/blog/all.jpg"
image_webp: "/images/blog/all.jpg"
author: contributor

---

# Golang China Contributor Summit 2021

> Organizing committee: Andy Pan, Baokun Lee, Ben Shi, Meng Zhuo
>

![](/images/blog/banner.png)

## 峰会简介

在 GopherChina 2021 召开的前一天下午，中国最核心的几位 Go 语言贡献者和社区的开发者们共聚一堂，举办了第一届中国 Go 语言开源贡献者峰会，对 Go 语言的一些热点议题进行了分享和交流。

![](/images/blog/ready.jpg)

峰会主要分为两部分：

- 三位主讲人分享一些国内社区发展情况和过去一年在 Go 社区的一些主要工作，作为全局主题。
- 全局主题结束之后分设三个圆桌讨论三个议题：
  - 编译器/工具链/硬件
  - 标准库和 Runtime
  - 社区发展和生态

分桌议题期间，与会嘉宾可以根据自己的兴趣自由、灵活地加入圆桌参与讨论。

## 峰会议题

### 国内 Go 语言贡献者社区（by Baokun Lee）

![BKLee](/images/blog/bklee.jpg)

当前中国的 Go 开发者数量庞大，并且 Go 语言在很多公司已成为主流开发语言。

- 字节跳动：后端栈基于 Go 语言，第一开发语言。
- 滴滴：后端栈基于 Go 语言，第一开发语言。
- 腾讯：Go 语言是仅次于 C++  的第二开发语言。
- 其他国内大厂如阿里、百度、美团等，也有不小规模的 Go 线上服务。

但与此同时，中国地区对 Go 上游社区的回馈极少，话语权微弱。因此早期中国区的几位对技术有追求的 gophers，自发地给 Go 语言项目贡献代码，并组织成立了 Go 语言中国开源贡献者俱乐部。

![badges](/images/blog/badges.jpg)


俱乐部的愿景如下：

- 鼓励并帮助更多的中国 gophers 向上游官方 Go 社区贡献代码，并对上游社区施加国人的影响力；
- 定期分享 Go 工具链和运行时等内部实现机制，和国内 gophers 共同学习成长；
- 和各界 gophers 加强交流，精细分工，共同完善 Go 语言生态系统。

目前俱乐部已取得如下成果：

- 五年间累计给上游官方 Go 语言项目贡献超过十万行代码，包括但不限于编译器、Runtime 和标准库；
- 俱乐部有六位成员拥有 Go 官方 Git 仓库的 approver 权限，可以 review/merge 全球其他贡献者的补丁；
- 俱乐部有四位成员进入全球贡献者排名**前一百名**;
- 受邀参加 Go 官方在美国举办的全球峰会。


过去的一年，共有 7 位贡献者加入俱乐部，目前总共有 12 位成员。

![](/images/blog/members.png)

过去的一年，共有 7 位贡献者加入俱乐部，从 2020 年初到 2021 年 6 月底，12 位贡献者共给社区提交了 198 个 CLs。

![eric-cls](/images/blog/eric-cls.jpg)

俱乐部骨干成员 Zhuo Meng 和 Andy Pan 由于广东地区突发的新冠疫情而未能按原计划到场参加本次峰会，因此通过远程视频接入了此次峰会。

![](/images/blog/mengzhuo.jpg)

俱乐部欢迎更多的 gophers 加入，除了定期的组内交流和干货分享，还有其它回馈和鼓励机制：

- 获得一个 @golangcn.org 后缀邮箱
- 加入 golangclub@github 组
- 参加 China Golang Contributor Summit
- GopherChina 免费门票
- ECUG Con 免费门票

在 2021 年 6 月，Andy Pan 为俱乐部改版了官方网站，加入博客系统，鼓励成员们知识分享和交流。https://golangcn.org/

![OfficialSite](/images/blog/website.png)

### Go Map 高并发读写（by 张怀龙）

来自 Intel 的 gopher 张怀龙分享了 Go Map 高并发读写的优化方案，包括四个部分：

- Go 语言中 Map 的基本结构
- 一个在并发程序中使用 Map 的实例和潜在的性能问题
- 提高并发读写性能的方案
- 对此问题更深远的思考

![huailong](/images/blog/huailong.jpg)

### 如何破冰成为 Go 语言贡献者（by Ben Shi）

国内很多 gophers 都有魔改 Go 工具链/运行时的经历，然而最终只能让小范围内的人获益，未能回馈给 Go 上游社区。这其中有多种因素，包括技术线路上的，政策上的，思想意识上的因素。

我们都在项目中大量地使用过开源代码，并经历过维护私有仓库的痛苦：因为私仓和官仓分叉越来越远，导致后期升级困难，而私仓能 merge 到官仓是唯一的解决方案。俱乐部成立的一个重要目的，就是鼓励国内更多的 gophers 贡献代码到上游社区。

俱乐部骨干成员 Ben Shi 介绍了给 Go 社区贡献代码的几种方式，由易到难的顺序是：完善文档 < 添加测试 case < 报告 bug < 解决 bug < 给官仓 CI 添加机器 < 完成 TODO < 优化源码 < 添加新功能 < 将 Go 移植到新的平台。

![benshi](/images/blog/benshi.jpg)

### Go-ARM64 的展望（by Zheng Xu）

ARM64 是 Go 工具链重点支持的平台，来自 ARM 中国的 Zheng Xu 带领他的团队为 Go 工具链贡献了大量的 ARM64 的特性和优化。Zheng Xu 此次分享了他团队下一步的工作计划，并欢迎各界 gophers 加入他的团队（其中还有国内唯一的女性贡献者，总贡献量已进入全球前 100 名）。

![ZhengXu](/images/blog/zhengxu.jpg)

![Eric](/images/blog/eric.jpg)

![Fannie](/images/blog/fannie.jpg)

## 分组讨论

现场人员根据自己的兴趣参与分桌议题讨论，共有三桌子议题：

- 编译器/工具链/硬件
- 标准库和 Runtime
- 社区发展和生态

![](/images/blog/agenda1.png)
<br />

![](/images/blog/table1.jpg)

![](/images/blog/table2.jpg)

## 俱乐部的 95 后

俱乐部的成员 Cholerae Hu 来自字节跳动，1997 年的小鲜肉，目前已经给 Go 语言贡献了十多个优质的补丁。让笔者体会到了什么叫后生可畏。

![hu](/images/blog/hu.jpg)

## 翌日的 GopherChina 2021

Go 语言贡献者俱乐部受邀参加 GopherChina 2021，并在首场演讲中与 Go Core Team 成员、全球编译器大拿 Ian Lance Taylor 畅谈了 Go 2.0 中的泛型设计和 Go 语言未来的发展计划。

![ian](/images/blog/ian.jpg)

## 来访嘉宾

- 中国科技大学教授张昱
- 腾讯开源联盟主席单致豪
- 凤凰网高级运维总监温迪
- GopherChina 创始人谢孟军
- 华为 2012 开源实验室姜宁
- Go 语言中文网创始人徐新华
- 《Go 语言高级编程》作者曹春晖
- 知名公众号『码农桃花源』作者饶全成
- 龙芯公司移植 Go 到龙芯平台的负责人刘晓东
- 华为 2012 编程语言实验室刘军
- Intel 苏涛
- Intel 陈海滨
- Intel 谢林

![all](/images/blog/all.jpg)

## 鸣谢

本次峰会的赞助商为 **Intel**，主办方为 **凤凰网** 以及 **腾讯云**。

![](/images/blog/sponsors.png)

感谢赞助商为 Go 语言中国贡献者峰会提供的精美的茶歇小食和丰盛的晚宴，感谢凤凰网荣乾、GopherChina 谢孟军以及帅气志愿者们的鼎力支持。

## 展望

第一届中国 Go 贡献者峰会已经落下帷幕，由于是首次举办，经验尚有不足，如若有所怠慢，还望各位海涵！

本次峰会虽过程略有曲折，但也算是顺利完成；虽不免有些许遗憾，但也取得不少意外的收获。我们希望明年的第二届峰会能扩大规模和影响力，也希望我们的峰会能引起更多国内厂商的重视并且吸引更多的公司积极参与进来。

我们 Go 语言中国贡献者俱乐部希望能在这股中国的 Go 语言浪潮中尽其所能，通过鼓励并帮助更多的中国 gophers 向上游 Go 社区贡献代码，并在国内的 Go 语言社区中定期分享 Go 工具链/运行时等的内部实现机制，助力国内社区的繁荣发展以及和国内 gophers 共同学习成长，共同建设国内的 Go 生态，并愿意尝试作为沟通中国 Go 社区和 Go 语言官方的一道桥梁。

最后，再次重申我们俱乐部的愿景作为结尾，谢谢各位！

- 鼓励并帮助更多的中国 gophers 向上游官方 Go 社区贡献代码，并对上游社区施加国人的影响力；
- 定期分享 Go 工具链和运行时等内部实现机制，和国内 gophers 共同学习成长；
- 和各界 gophers 加强交流，精细分工，共同完善 Go 语言生态系统。
