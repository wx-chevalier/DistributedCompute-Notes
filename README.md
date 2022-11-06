[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![license: CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-lightgrey.svg)][license-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/wx-chevalier/DistributedSystem-Series">
    <img src="header.svg" alt="Logo" style="width: 100vw;height: 400px" />
  </a>

  <p align="center">
    <a href="https://wx-chevalier.github.io/DistributedSystem-Series"><strong>在线阅读 >> </strong></a>
    <br />
    <br />
    <a href="https://github.com/wx-chevalier/Awesome-CheatSheets">速览手册</a>
    ·
    <a href="./examples">代码案例</a>
    ·
       <a href="https://github.com/wx-chevalier/Awesome-Lists">参考资料</a>
    ·
    <a href="./README.en.md">English Version</a>

  </p>
</p>

# Distributed System Series（分布式系统·实践笔记）

现实世界中的数据系统往往颇为复杂。大型应用程序经常需要以多种方式访问和处理数据，没有一个数据库可以同时满足所有这些不同的需求。因此应用程序通常组合使用多种组件：数据存储，索引，缓存，分析系统，等等，并实现在这些组件中移动数据的机制。许多现有数据系统中都采用这种数据处理方式：你发送请求指令，一段时间后(我们期望)系统会给出一个结果。数据库，缓存，搜索索引，Web 服务器以及其他一些系统都以这种方式工作。

像这样的在线（online）系统，无论是浏览器请求页面还是调用远程 API 的服务，我们通常认为请求是由人类用户触发的，并且正在等待响应。他们不应该等太久，所以我们非常关注系统的响应时间。值得说明的是，这不是构建系统的唯一方式，其他方法也有其优点。我们来看看三种不同类型的系统：

- 服务（在线系统）：服务等待客户的请求或指令到达。每收到一个，服务会试图尽快处理它，并发回一个响应。响应时间通常是服务性能的主要衡量指标，可用性通常非常重要（如果客户端无法访问服务，用户可能会收到错误消息）。

- 批处理系统（离线系统）：一个批处理系统有大量的输入数据，跑一个作业（job）来处理它，并生成一些输出数据，这往往需要一段时间（从几分钟到几天），所以通常不会有用户等待作业完成。相反，批量作业通常会定期运行（例如，每天一次）。批处理作业的主要性能衡量标准通常是吞吐量（处理特定大小的输入所需的时间）。

- 流处理系统（准实时系统）：流处理介于在线和离线（批处理）之间，所以有时候被称为准实时（near-real-time）或准在线（nearline）处理。像批处理系统一样，流处理消费输入并产生输出（并不需要响应请求）。但是，流式作业在事件发生后不久就会对事件进行操作，而批处理作业则需等待固定的一组输入数据。这种差异使流处理系统比起批处理系统具有更低的延迟。

![分布式计算概念图](https://i.postimg.cc/dtd6t4MP/image.png)

## Nav | 关联导航

- 如果你想了解微服务/云原生等分布式系统的应用实践，可以参阅；如果你想了解数据库相关，可以参阅 [Database-Series](https://github.com/wx-chevalier/Database-Series)；如果你想了解虚拟化与云计算相关，可以参阅 [Cloud-Series](https://github.com/wx-chevalier/Cloud-Series)；如果你想了解 Linux 与操作系统相关，可以参阅 [Linux-Series](https://github.com/wx-chevalier/Linux-Series)。

# About

## Copyright & More | 延伸阅读

笔者所有文章遵循 [知识共享 署名-非商业性使用-禁止演绎 4.0 国际许可协议](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh)，欢迎转载，尊重版权。您还可以前往 [NGTE Books](https://wx-chevalier.github.io/books/) 主页浏览包含知识体系、编程语言、软件工程、模式与架构、Web 与大前端、服务端开发实践与工程架构、分布式基础架构、人工智能与深度学习、产品运营与创业等多类目的书籍列表：

[![NGTE Books](https://s2.ax1x.com/2020/01/18/19uXtI.png)](https://wx-chevalier.github.io/books/)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/wx-chevalier/DistributedSystem-Series.svg?style=flat-square
[contributors-url]: https://github.com/wx-chevalier/DistributedSystem-Series/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/wx-chevalier/DistributedSystem-Series.svg?style=flat-square
[forks-url]: https://github.com/wx-chevalier/DistributedSystem-Series/network/members
[stars-shield]: https://img.shields.io/github/stars/wx-chevalier/DistributedSystem-Series.svg?style=flat-square
[stars-url]: https://github.com/wx-chevalier/DistributedSystem-Series/stargazers
[issues-shield]: https://img.shields.io/github/issues/wx-chevalier/DistributedSystem-Series.svg?style=flat-square
[issues-url]: https://github.com/wx-chevalier/DistributedSystem-Series/issues
[license-shield]: https://img.shields.io/github/license/wx-chevalier/DistributedSystem-Series.svg?style=flat-square
[license-url]: https://github.com/wx-chevalier/DistributedSystem-Series/blob/master/LICENSE.txt
