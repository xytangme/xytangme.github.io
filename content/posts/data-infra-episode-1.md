---
title: "Data Infra: What's Next 科技早知道 × Snowflake & Databricks"
date: 2022-10-20T01:38:31+08:00
draft: false
---

有了感兴趣的话题，先找找有没有相关的播客，逐渐成了一种习惯。幸运的是，今年开始关注的`data infra`这个话题，已经有不少播客谈论过。摘取其中一些，与各位看官分享。今日第一par，必须聊聊（仍然是）该领域的当红炸子鸡[`Snowflake`](https://www.snowflake.com/en/)和[`Databricks`](https://www.databricks.com)这对“欢喜冤家”。

如果您只是好奇本文提到的播客，请直奔[相关播客](#相关播客)。*注：本文仅包含了`Snowflake`和`Databricks`产品相关内容，更全内容请听播客*

---

# Snowflake

## Summary

在 **[What's Next 科技早知道 - #45 股神加持云端独角兽 Snowflake，SaaS 的黄金 10 年来了？](https://www.xiaoyuzhoufm.com/episode/5f72db9183c34e85ddfa7a17)** 这一期当中，一位早期（90+号）员工讲述了了他眼中的Snowflake相对其他于云厂商的竞争优势：

- 对于小公司来讲，能够根据计算的复杂度弹性收费，最后的效果就是更便宜
- 对于大公司来讲，由于cloud agnostic，能够做到跨云备份，也不需要跟任一云厂商绑定，如果需要的话可以做到低成本的迁移
- 存算分离，存储和计算可以分别Scale，还可以为不同部门提供单独的计算资源
- 基于用量的计费模式，用的越多收费越高，net retention 158%是一个比较高的水平，迁移成本高所以不易替换
- 独特的产品形态，例如早期的数据仓库即服务，后期的data sharing（零拷贝，类似数据领域的远程协同）

以及提到一个fun fact，Snowflake的双重意义：创始人都是滑**雪**爱好者，以及**雪花**型数据模型。

这一期还采访了[Howie Xu 徐皞](https://twitter.com/H0wie_Xu)，他从投资人的角度讲述了对Snowflake这家公司的看法：

正面看法：

- Snowflake的种子投资基金Sutter Hills在硅谷创业人眼里是一家低调但特别优秀的基金，被他们投资是一种荣誉
	- Sutter Hills的传统，是帮助几个厉害的工程师共同打造一家公司，投资人即公司CEO，公司起来之后换成有大公司管理经验的CEO，上市之前再换
	- Sutter Hills是一家Evergreen常青基金，投资人无需融资，Snowflake的70万投资多数来自投资人自己的钱
- 同期SaaS公司集中上市，主要因为时机合适，股市特别好，总统大选结果未出暂无震荡
- Snowflake的成功与CEO Frank Slootman有关，ServiceNow的CEO加入也是一个强大的signal
- Net dollar retention亮眼
- 2012年，在市场觉得关系型数据库走到尽头，以及对数据上云持怀疑态度的情况下坚持做云上数仓，创始人也没什么名气，但最终建立起护城河
- 同期亚马逊在Redshift上犯错，使用了比较烂的源代码，团队质量不高
- 产品技术好、便宜、易用（不懂技术懂商业就能用），“数据仓库里的zoom”
	- 用户变化了，产品的易用性变得非常重要
- Covid使得对数字化的要求变高了（云、企业软件、网络安全、数据）
	- 被逼数字化：教育

负面看法：

- 至今仍然亏本，股价仍然太贵，虚胖
- 客户数量几千个，还刚刚起步，市值几十亿美元比较合理
- 11%的营收来自一个客户（思科），说明公司还非常早期
- 赛道非常拥挤，还是一个非常小的player
- 亚马逊花大量力气在修正Redshift的错误，谷歌BigQuery + Looker足够打败Snowflake + Tableau
- 公司文化是否健康，存疑，例如CEO的更换不讲人味

But，可能的误判原因：

- Net dollar retention惊人的出色，说明客户满意度非常高，六七百亿的市值是值得的
- Market timing非常好，正好处在数据即服务的爆发期
- 第一次把data as a service做的特别易用，易用性的佼佼者
- 人性通常高估一年的估计，但低估指数增长的效应，如果能保持超过100%的增速，前途无量
- I don't know what I don't know. 外部视角雾里看花，不能完全appreciate

# Databricks

## Summary

**[What's Next 科技早知道 - S6E06 硅谷徐老师｜对话Databricks联合创始人Reynold Xin：380 亿美元估值背后的长期主义](https://www.xiaoyuzhoufm.com/episode/624d6e51bfd2579bb23872cc)** 这一期，[Howie Xu 徐皞](https://twitter.com/H0wie_Xu)采访了Databricks的联合创始人[Reynold Xin](https://www.linkedin.com/in/rxin)。以下是他的观点：

- Spark的起源：为Netflix的基于电影评分的推荐系统比赛开发的计算框架（最后算法并列第一但晚交了二十分钟，没有赢到一百万，啊）
- 早期坚持长期主义的三个大方向
	- **只做云，不做on premise**：从长期角度来看，云是未来，能做到更快的部署，客户维护成本低，但直到19年才不被新executive，投资人和客户challenge
	- **只做data science, data engineering和AI产品，不做data warehouse**：data warehouse竞争太激烈，当年不被看好，因为data science还未被广泛接受，后面第一个产品获得得天独厚的优势，市场上没有可以竞争的产品
	- **不纯粹做support**：2014/2015年Spark小有名气，有比较大的support需求（e.g. 砸一千万支持data center），但坚持做产品和平台
- 头三年，产品营收远低于Spark峰会营收，一些中间层有问题的决定
	- **过于依赖开源**：对标错了做很多定制化的cloudera；云厂商直接把开源服务封装成产品，从工程角度要求低，然后以非常低的价格卖出，从价格角度Databricks无法竞争
	- **未重视top down的销售**：infra产品难以bottom up，越基础越需要上层push
- 2015/2016左右两个大决定
	- 引入top down销售团队
	- 产品层面做出竞争壁垒：性能、scalability、安全
		- 对开源产品比别人理解更深，做的更快，有时间壁垒
		- 好的engineer
		- 运维自动化，每天在三大云上run 1200万台虚拟机，几百号工程师编写程序维护，已经是竞争壁垒之一
		- 培养开源社区，带来bottom up sales（但有限），培养人才
- Azure Databricks：Databricks开发，微软销售
	- 对于Databricks，因为支持直接把客户的微软的budget转到Databricks，不需要那么多销售，利润提高，时间缩短
	- 对于微软，一年之间从没有大数据和数据科学产品，完全没有竞争优势，到业界领先，带来营收，是Azure上最成功的服务之一，也带来了计算和存储层面的提高
- 对未来的展望
	- 从纯计算层面，到做存储：2018年客户问题一半与存储有关，诞生第二个大的开源项目delta lake
	- 最终决定做data warehouse：绝大多数企业客户的架构是，基于data lake 10%的数据做data warehouse
		- 问题：数据的拷贝、性能（技术问题），不同团队不同权限不同数据，得出不同决策，导致商业团队不相信数据（业务问题）
	- 未来的数据架构：统一的数据平台
	- SQL很重要，但更复杂的应用需要Python

Fun fact: cloudera = cloud + era，一开始是准备做云，但08/09年经过市场调研，发现云的时代还未到来，于是改做on premise

# Snowflake vs Databricks

[What's Next 科技早知道 - Bonus｜Clubhouse 爆火，美股声网起飞，下一个会是谁？](https://www.xiaoyuzhoufm.com/episode/60226843493452791d18f5cb)

[What's Next 科技早知道 - S5E02 硅谷徐老师｜云数据存储和分析市场千亿美元机会的格局和前景](https://www.xiaoyuzhoufm.com/episode/605acf8fb16ae5d6ad7f7d29)

- 大数据产品三个应用场景：BI、ETL和data warehouse、机器学习
- Databricks本是Snowflake的上游，但二者都开始做对方领域的事情
	- Databricks: Delta Lake
	- Snowflake: 布局机器学习（投资datarobot）、自建spark服务、ELT
	- 长期来看哪种方式更有效，未知
- 商业模型、收费模式上都是按使用量付费
	- 数据增长快过人头增长；已经上云，对这种收费模式很熟悉
	- Snowflake将底层云计算的成本隐藏：如果能通过底层优化省更多云的成本利润会更高，但要承担更多风险
	- Databricks分别计算：无法通过优化计算效率来提高利润，但不用承担云的成本
	- 二者实际盈利可能相当，Databricks毛利高过Snowflake
- 三种竞争关系
	- Snowflake和Databricks和其他竞品之间的竞争
	- On premise和cloud之间的的竞争
	- Snowflake和Databricks与平台已有服务的竞争
		- 对于云厂商，AWS要考虑跟GCP的竞争，需要先吸引客户上自己的云，所以不会把Snowflake或者Databricks剔除

---

# (Personal taste) What's Next?

- 站在现在（2022年10月）来看，Snowflake上述的技术优势是不是保持到了现在，存疑。特别是存算分离这个feature，现在已经有不少数据库产品都能支持，Snowflake的独特之处在哪里？
- 很好奇Howie Xu如果两年后的现在再录一期节目，有没有改变看法？Snowflake目前仍然亏损，股价\~170，市值\~540亿
- 我个人也是信统一数据架构那一挂的，但离大规模使用还有多远？

---

# 名词解释

## Data Infrastructure 数据基础设施

“大数据”这个概念在中文语境恐怕已经被说烂了，但在技术领域，it is a real thing。所谓Data Infrastructure，或者Data Infra，指的是与大数据应用有关的一系列技术基础设施，包括不限于数据获取、存储、加工、分析、展示等各个环节使用到的工具产品。一般来说Data Infra有两类上层应用，一类是分析向的，目的是支持商业决策，还有一类是运营向的，例如一个搜索或者推荐系统中的机器学习模块。这两类应用独立发展出了各自的infra体系，不过目前有一种融合的趋势。详情可参考[其他链接](#其他链接)。

## Data Warehouse 数据仓库

Data Warehouse主要的应用场景，是上文提到的商业决策。它由一系列结构化的数据表组成，可类比为很多相关联的excel表格，分析师以其作为数据源，来寻找业务优化方向，也是[`Snowflake`](https://www.snowflake.com/en/)主要的产品形态。

## Data Lake 数据湖

与Data Warehouse只支持结构化数据不同，Data Lake可支持任意格式的数据，包括半结构化及非结构化数据（简单来讲，所有无法用简单的行和列来表示和分析的数据格式）。它的主要应用场景是上文提到的机器学习，主要的使用者则是机器学习研发人员，以及机器学习系统，也是[`Databricks`](https://www.databricks.com)主要的应用领域。

## SQL, or Structured Query Language 结构化查询语言

Structured Query Language 顾名思义，用来查询结构化数据的一种语言，所以主要用来做基于Data Warehouse的查询，不过近年来Data Lake也逐步开始支持类似的查询机制。

## Spark

最大的开源的大数据框架。[`Databricks`](https://www.databricks.com)是由[`Spark`](https://spark.apache.org/docs/latest/quick-start.html)的creators们创立的，基于Spark做商业化的公司。

## On Premise vs Cloud Computing 云计算 & SaaS Software as a service 软件即服务

传统的软件开发，从购买或者租用服务器机器开始，称On Premise。当下更新的模式是，亚马逊、微软、谷歌、阿里等厂商负责维护服务器并对外提供租赁服务，使用者按需订阅并付费，称Cloud Computing。基于Cloud Computing又诞生了，连上层应用都给封装好，无需开发开箱即用的商业模式，称SaaS。 Data Infra领域的SaaS，就包括存储（Data Warehouse or Data Lake）和计算（e.g. Spark）相关的软件。

*相关的还有IaaS和PaaS，有兴趣的看官请自行查阅。。*

---

# 参考资料

## 相关播客

*（链接均为小宇宙）*

[What's Next 科技早知道 - #45 股神加持云端独角兽 Snowflake，SaaS 的黄金 10 年来了？](https://www.xiaoyuzhoufm.com/episode/5f72db9183c34e85ddfa7a17)

[What's Next 科技早知道 - Bonus｜Clubhouse 爆火，美股声网起飞，下一个会是谁？](https://www.xiaoyuzhoufm.com/episode/60226843493452791d18f5cb)

[What's Next 科技早知道 - S5E02 硅谷徐老师｜云数据存储和分析市场千亿美元机会的格局和前景](https://www.xiaoyuzhoufm.com/episode/605acf8fb16ae5d6ad7f7d29)

[What's Next 科技早知道 - S6E06 硅谷徐老师｜对话Databricks联合创始人Reynold Xin：380 亿美元估值背后的长期主义](https://www.xiaoyuzhoufm.com/episode/624d6e51bfd2579bb23872cc)


## 其他链接

[Future (a16z) - Emerging Architectures for Modern Data Infrastructure](https://future.com/emerging-architectures-modern-data-infrastructure/)

[Future (a16z) - Emerging Architectures for Modern Data Infrastructure: 2020
](https://future.com/emerging-architectures-for-modern-data-infrastructure-2020/)
