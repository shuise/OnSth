# Github 与多人协作



电脑及软件都是提高个人和组织生产力的工具，对于每个人而言，每天的阅读、思考和记录是最有价值的部分，需要良好的记录沉淀。

在互联网世界，文本时最简单最强大的工具，文本可以不受限制的记录信息。使用数据库或者特殊专业软件格式是部分专业人士的特权，使用文本则是互联网时代所有人的平权。

文本可以让人专注于记录信息本身，不必在意格式排版等，尤其适合平时的随手记录。

缺点也很明显，对于文字段落之外的信息支持的不好，经常导入很多信息难以录入，最可行的办法是使用类文本的 md，输入过程还是像文本一样，只是通过各种工具增强了输入和渲染表达。

归纳一下，常用的信息有标题、段落、表格、图片/音频/视频、链接、流程图等。



## 推荐 md 及对应协作工具

1.   typora：https://typora.io/ (支持 windows、mac、linux)
2.   mermaid 流程图：https://mermaidjs.github.io/（typora 原生支持）
3.   pandoc 插件 https://www.jianshu.com/p/6ba04f669d0b（加上 pandoc，typora 就可以导出 pdf、word）





## 协作问题

工作中最常见的麻烦就是文档传来传去，各种几乎无效的复制备份，甚至经常因为不是同一个版本而产生大量的误会。

我曾经做过彻底的解决，大致的思路是一切信息云端集中管理，通过 uri 同步信息，所有人都基于相同的 uri 沟通协作，所有有权限的人都可随时修改且不影响他人工具。

**使用到的工具**：

1.   公司内部的 Gitlab，可以认为等于 Github：https://github.com
2.   typora、gitbook、seafile 云盘（dropbox也行）



当时整个过程是我刚接管产品技术团队，前端、后端、产品之间的协作混乱，各种信息不一致且不知道那个版本正确，每个人都用自己的习惯自己的工具写东西，各种传递每天继续恶化问题。

我先拉着几块的关键人员沟通协商，大家一起协商了几个原则：

1.   文件与文档分离，文件（设计稿、合同文件、商务 PPT等）使用云盘，团队提前配置好了云盘的目录结构，大家把自己手里的文件都按约定统一到云端，相似文件保留多版本，用时在处理；
2.   文档也按照约定方式放入 git，老文档先不动，新文档用 md 编写，还专门定义了文档结构、示范；
3.   拉了一个热心肠的开发做技术支持，让每个人掌握 git/gitbook 的使用，沟通期间可以在局域网预览他人本地的文档，边改边沟通，云端更新自动出发编译生成正式链接，邮件或聊天工具同步；
4.   要求会议记录、团队周报、产品文档、技术文档等全部在线化，且互相连通，通过任意一个入口链接就可以按图索骥的看到其他相关内容
5.   因为 git 有自动版本管理，能精准控制到标点符号，因此大家只需要沟通、修改、提交，不需要在意是否要备份，快速迭代往前走，有问题随时查找老版本信息。



**实践后的总结**

1.   md 有一个质疑到接受的过程，主要是观念的变化，
     一个是改掉同时处理表现与内容的习惯，把输出交给工具解决，输入时只关注内容本身；
     另外一个因为文本能力偏弱，慢慢都有了简化处理的思维，很多时候其实没必要那么复杂，简单够用就好；

2.   git 的云端备份带来十足的安全感；
     协作机制让每个人都可以专注自己的工作，不再需要被冲突干扰，不再被乱七八糟的各种小问题消耗，更多精力都放在协作本身，约定工作方法、研究工作效率的优化等。

     

美中不足的是没能在真正的写作层面有所突破接下来，还是想找机会在知识管理与写作上做一些新的尝试。



我现在会把 git + md 的协作方式推荐给每一个人，不管是做什么工作，只要使用电脑，我都坚持用着两个工具先记录信息，这是一个不可动摇的基础。





## 附 Git 使用心得

1.   如果只是记录信息，不需要使用分支；
2.   随后记录，随手提交，保证及时云端备份；
3.   根据内容变更进行管理，<del>反面例子是根据文件进行管理</del>，要聚焦于内容变更的原因和修改本身，比如修改「邮件使用说明」，该修改几个文件就修改几个文件，修改完成后集中提交本地修改；
3.   每次修改务必提交日志，说明为什么修改，越详细越好，不需要说明修改了什么（内容变更本身已经有交代）
3.   多人协作情况下，每次开始工作先获取云端最新版本