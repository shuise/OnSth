# 接口工具与协作



Apifox 与 postman 是类似的工具，都可以用来管理接口设计和开发调试，下面以 Apifox 为例解释相关细节。



从开发角度看，[Apifox](https://www.apifox.cn/ ) 是一款集API 文档、API 调试、API Mock、API 自动化测试于一体的工具

```Apifox = Postman + Swagger + Mock + JMeter```



## 团队的用法

> 逐个接口都定义唯一编号，基于编号沟通无歧义

1. 开发初期，先通过 Apifox 定义接口，前端基于接口定义生成的 mock 接口进行开发，同时从业务角度校验接口设计
2. 自测时在 Apifox 编写接口用例，穷举使用场景
2. 有了上面两步，联调过程就简化为接口设计校对和接口用例检查，前端确认了出入参没问题，接口用例保证覆盖度，直接跑一遍流程就基本完成调试
4. 提测阶段附上接口用例，测试对接口用例进行评测，是否遗漏用例一目了然，发现问题先核对用例，有缺失随时补充用例
5. 通过组合接口用例的方式来编写用例，对接口修改后回归测试提供便利
2. 针对复杂的场景，额外做测试用例



## 带来的一些改变

1. 接口文档和调试聚合到一起，后续维护接口更便捷

2. 团队都针对同一份文档配合工作，联调和测试过程中的沟通成本会降低很多，重复的工作也会减少

3. 测试和联调工作被前置了一部分，如果有问题可以提前发现

4. 相应的，需要花一些精力来管理和维护 Apifox 文档

   

## 后续想法
现代工程先后端分离，操作数据都是通过接口；跨项目组也都是通过接口协作；

SaaS 的时代两个公司之间经常有基于 API 的沟通协作；即便提供了 SDK 和文档，很多时候受限于运行环境，还是不如接口来的简单；

有很多时候，非开发人员也需要使用接口，比如验证 AI 能力接口可用性，基于开放平台接口做一些必要操作等；

尤其重要的场景是个人数字世界的秩序打造。

而这些都可以通过 Apifox 解决，不需要写太多代码，只需要配置参考和接口，点击调用即可，可以在开发人员尽量不参与的情况下，让非开发人员完成更多的事情。



**关于个人数字世界的秩序打造：**

1.   通过分析常用网站的非公开接口为自己做甜点工程，比如导出微信读书、豆瓣、得到都网站的笔记；
2.   对接常用网站，比如基于豆瓣的待读搜索电子书商城；对接编辑器与发布平台等
3.   基于 notion、airtable 或者私有部署的 headless 服务收集个人的互联网数据等
4.   可以构建基于多人协作的跨网站跨应用流程



**需要掌握的技能**

1.   http 协议与抓包
2.   Apifox 的使用