---
title: "一年成为Emacs高手 (像神一样使用编辑器)"
date: 2024-06-06
lastmod: 2024-06-06
tags: ["emacs"]
description: ""
summary: "如何在一年内成为Emacs高手（像神一样使用编辑器）"
slug: master-emacs
---

# Table of Contents

1.  [简介](#org4d1c286)
2.  [为什么用 Emacs (可选)](#orgfa57942)
    1.  [学会了Emacs就同时学会了其他编辑器](#org6e16b65)
    2.  [优秀的社区](#org3102ce7)
    3.  [编程速度更快](#org5fe80d0)
    4.  [Emacs 会永存](#org274e1e8)
    5.  [可以立刻开始工作](#org1e3713f)
    6.  [一年指的是一年中的空闲时间](#orgf0c444f)
3.  [实事求是,戒骄戒躁](#org1a2ed1f)
    1.  [理解软件自由](#orgfa2d651)
    2.  [避免门户之见](#org1d0de92)
    3.  [以科学理性做指导](#orgc3d6b89)
4.  [具体步骤](#org29daa18)
    1.  [无 Linux/Unix 经验新手的快速指南 (可选)](#orgaf96b98)
    2.  [读官方教程](#org846ae7d)
    3.  [以实际问题作为切入点](#org40c0a28)
    4.  [待解决的问题设定优先度](#orgab703be)
    5.  [站在巨人的肩膀上](#org71ffacc)
    6.  [报 bug](#orgc05d10b)
    7.  [持续改进](#org5bc0222)
    8.  [加入社区更上一层楼](#orgb4c4cfb)
        1.  [Reddit](#orge21f1fb)
        2.  [GitHub 是高手云集的地方](#orged31382)
        3.  [博客](#orgd75e883)
        4.  [在 Stack Overflow 上搜索相关讨论](#orgc3d032a)
        5.  [到 Youtube 上看 emacs 相关的视频](#org1632e43)
5.  [读书最有效](#orgc960512)
    1.  [EmacsWiki](#orgb577917)
    2.  [Emacs Lisp 书籍推荐 (可选)](#orgf2d7d09)
6.  [知识管理](#org027d9ec)
    1.  [配置纳入 GitHub 的版本控制](#org4c59fb7)
    2.  [将相关资料备份](#org10eb1ba)
7.  [第三方插件推荐](#org981fb2e)
8.  [Emacs 是一种生活方式](#orgc067285)
9.  [付之于行动](#org4b2ab03)
10. [使用 Evil](#orgde4db21)
    1.  [Text Object](#org275be3a)
    2.  [Leader 键](#org999c259)
    3.  [Evil 兼容 Emacs 原生插件](#org4d54242)
    4.  [Evil 专用的插件介绍](#org4289f02)
        1.  [evil-surround](#org710ce4c)
        2.  [evil-nerd-commenter](#orgd773a5c)
        3.  [evil-matchit](#orgd65fcb3)
        4.  [evil-escape](#org9bcfcae)
        5.  [evil-visualstar](#org94e1ffa)
    5.  [在 Shell 和 Interactive Interpreter 中使用 Evil](#org7b547c1)
    6.  [Evil 的小结](#org46e1ff2)
11. [答疑](#orgab537db)
    1.  [新手怎么开始](#org2ad4661)
    2.  [如和理解他人配置](#org8b73282)
    3.  [他人配置是否太重量级?](#org49a6fcf)
    4.  [其他第三方配置](#org8fb3ce4)
    5.  [该使用 Emacs 的哪个版本](#orga01fc3a)
    6.  [Vi 用户要转阵营吗?](#orgf29d0f3)
    7.  [为什么很多 Vi 用户不接受 Evil?](#org1918f8d)
    8.  [不习惯默认快捷键, 怎么办？](#org1cd5358)
    9.  [使用第三方配置后有些奇怪的 bug, 怎么改?](#orgdd500c3)
    10. [已更新软件包, 但是没有任何作用, 也没有任何错误信息](#orgc426d2d)
    11. [有配置问题](#org651868a)
    12. [启动报错](#org470243c)
    13. [自己的简单配置好控制](#orgf48784f)
    14. [自己加的插件无效](#orge2344f5)
    15. [我想用 Windows 版本的 Emacs 而不是 Cygwin 版本, 怎么做?](#org05c6f00)
    16. [Emacs 在代码跳转和自动完成上和商业 IDE 有差距, 怎么办?](#org178da7d)
    17. [邮件](#orga7e63f1)
    18. [为什么 Emacs 启动时从服务器 (elpa) 安装第三方软件包 (package) 会失败?](#org7080547)
    19. [有些网站 Emacs 访问不了](#orgdb007d2)
    20. [是否应尽早学习 Emacs Lisp](#org7ad80d4)
    21. [掌握 Emacs Lisp 是否是成为高手的必要条件?](#orgca0eadd)
    22. [有必要学习键盘宏 (Keyboard Macros) 吗?](#org34be8ec)
    23. [基本操作我会了, 下一步学什么迷茫中](#orgfc6e2a9)
    24. [如何学习 org-mode?](#org631ae9e)
    25. [对于 &ldquo;一切都用 Emacs 来完成&rdquo; 的观点你怎么看?](#org61c8d8b)
12. [结语](#orge99e655)


<a id="org4d1c286"></a>

# 简介

成为高手很容易. 我初学Emacs时常忘记&ldquo;退出&rdquo;的快捷键, 一年后我完全掌握了Emacs.

一些文章强调Emacs有多牛, 但关于&ldquo;如何做&rdquo;则语焉不详. 即使涉及到&ldquo;如何做&rdquo;, 谈细节多而方法论少.

很多人花了大量时间&ldquo;学习&rdquo;Emacs却最终放弃,就是因为过于拘泥细节,而方法论上出了问题.

例如,初学者背少用的快捷键会有很大的挫折感.一个月记住50个快捷键后算很厉害了.但是Emacs可以配置快捷键的命令近7000个.如果记住所有快捷键等同于掌握Emacs的话,一个人需要花至少十年.99%的快捷键很少用,少用的按键很快就忘了.花了十年做了99%都是无用功的事情当然非常打击积极性.

除本文之外的任何一本Emacs教程都会列出至少100个&ldquo;常用&rdquo;的快捷键.我不会刻意教你某个快捷键,但是会告诉你:

-   一个人记住的快捷键数量和他的Emacs水平没有必然联系
-   20个甚至更少的快捷键够用了
-   常用的是哪些快捷键
-   其他按键在使用过程中会自然记住

我在快捷键这个问题上指明大方向,避免了记住7000个快捷键这个恐怖的任务,学习过程变轻松很多.

这个例子说明了本文独特之处在于集中火力在&ldquo;方法论&rdquo;.

方法论基于实践和经验总结,有事实证据支持.例如常用快捷键列表是用 [keyfreq](https://github.com/dacap/keyfreq) 的插件积累至6个月数据统计出来的.

全文结构如下:

-   为什么 Emacs 值得学习, 对开源文化熟悉可跳过这一章
-   实事求是,戒骄戒躁
-   充分利用高手成果, 不要重复发明轮子
-   尽快掌握 Emacs 的步骤
-   如何提高 (社区, 阅读, 知识管理)
-   跳出具体技巧, 重要的是人
-   答疑和小结


<a id="orgfa57942"></a>

# 为什么用 Emacs (可选)

虽然本文的重点是&ldquo;怎么做&rdquo;, 而不是&ldquo;为什么&rdquo;.但先解释一下Emacs的优秀之处很有必要.


<a id="org6e16b65"></a>

## 学会了Emacs就同时学会了其他编辑器

Emacs的自由度高且历史悠久,所以即使常用的功能也比其他软件类似功能强大的多.

切换到其他编辑器后,可以根据Emacs的独特经验优化自己的工作流.


<a id="org3102ce7"></a>

## 优秀的社区

Emacs Lisp 不同寻常的语法决定了其开发者都是资深开发者, 掌握了多门语言.


<a id="org5fe80d0"></a>

## 编程速度更快

IDE 针对特定语言或框架优化, Emacs 完成通用任务更有效.

例如, 我碰到难题需上 IRC 请教国外高手 (工作流是, 粘贴代码到 <http://gist.github.com>, 在 irc 提问, 看网页, 将解决方案粘贴回来), Emacs 集成了 IRC 工具和浏览器操作就很方便.

口说无凭, 请看高手视频, [abo-abo演示的查找替换技术](https://www.youtube.com/watch?v=AgRsYOJi6ao)

顺便说一下, Emacs的&ldquo;代码自动完成&rdquo;和&ldquo;代码导航&rdquo;两个功能对主流编程语言支持都不错.

&ldquo;不错&rdquo;的意思是达到90%的功能,是否能达到100%取决于安装了哪些插件. 达不到100%,适当妥协一下,90%也不错.

不要斤斤计较在&ldquo;代码自动完成&rdquo;和&ldquo;代码导航&rdquo;要完全复制IDE的体验.而忽视了Emacs的在这两个功能上的特色.

高级程序员对API早已熟悉,在大项目中的新代码和老代码相似.所以他们对&ldquo;智能&rdquo;不在意,对写代码速度更重视.

例如web程序员需求在javascript文件写css和html代码. Emacs结合 [Ctags](https://en.wikipedia.org/wiki/Ctags) 在同一代码文件自动完成javasscript&html&css,这显然很方便.


<a id="org274e1e8"></a>

## Emacs 会永存

[个人开发者会丧失兴趣](https://forum.sublimetext.com/t/project-alive/16005), 公司会倒闭. 但自由软件基金会将一直存在下去.

Emacs 作为其招牌软件也会维护下去, 投资永不会贬值.


<a id="org1e3713f"></a>

## 可以立刻开始工作

软件开源, 配置是纯文本, 且资源消耗小, 安装包很小 (命令行版本 30M 左右), 任何环境下都可用.

这在大项目中特别有益, 例如, 某项目需同时编辑 Perl, Java, C, Bash, SQL, 要编辑远程服务器上的代码, 网速不快. Emacs 的优势就体现出来了.


<a id="orgf0c444f"></a>

## 一年指的是一年中的空闲时间

我利用一年中通勤时间就取得了很大进步.


<a id="org1a2ed1f"></a>

# 实事求是,戒骄戒躁


<a id="orgfa2d651"></a>

## 理解软件自由

何为软件自由没有比自由软件基金会更权威了. 建议把 <https://www.gnu.org/philosophy/free-sw.zh-cn.html> 反复读, 理解何为四大自由.

一旦真正理解了软件自由, Emacs 就变得非常简单了.

例如, 很多用户习惯让 Emacs 启动时自动从其官方插件仓库 <https://elpa.gnu.org> 下载安装插件. 当该网站偶尔下线或者公司的防火墙拦截了对外网站访问时, Emacs 就会启动失败.

这也就是一分钟可以解决的小事, 如果你理解软件自由, **有勇气** 到 `~/.emacs.d/elpa/` 目录下看一看的话。

一个插件仓库 (repository) 本质上就是一个文件夹, 它有一个含有插件列表名为 `archive-contents` 的文本文件, 以及一系列插件包. 你完全可以把这些文件下载下来, 在本地硬盘里建立 ELPA 的镜像.

对个人来说, 安装 [elpa-mirror](https://github.com/redguardtoo/elpa-mirror) 每年备份一下所有插件就足够了.


<a id="org1d0de92"></a>

## 避免门户之见

比如用了 Emacs 就排斥 Vim 的快捷键, 或者反之.

避免门户之见的关键就是实事求是.

以 Emacs 和 Vim 的快捷键为例, 两种快捷键完全可以无缝接合.


<a id="orgc3d6b89"></a>

## 以科学理性做指导

有读者反映我的方法类似于大学里写论文做研究, 事实上这正是我的灵感来源.

Emacs 只是一种技术, 其学习方法和其它技术是通用的.

打好基础, 让自己的知识有 **足够的** 广度和 **适当的** 深度, 对新手是最重要的. 否则会在一些琐碎问题上浪费时间.

新手的错误是花大量时间记快捷键, 事实上网上教程列出的初学者&ldquo;必知&rdquo;快捷键不是必需的. 很少用到的快捷键直接输入对应命令就行了. 用 [smex](http://www.emacswiki.org/emacs/Smex) 或同类插件输入命令很高效.


<a id="org29daa18"></a>

# 具体步骤

后文用到的命名惯例,

-   `C` 表示按下 Ctrl 键, `M` 表示按下 Alt 键
-   `M-x my-command` 表示同时按下 Alt 和 X, 输入 &ldquo;my-command&rdquo;, 然后回车


<a id="orgaf96b98"></a>

## 无 Linux/Unix 经验新手的快速指南 (可选)

建议,

-   不安装任何第三方插件
-   掌握shell基本知识, 什么是环境变量, 什么是 stdin, stdout, pipe. 这些知识可以帮助用户理解 Emacs 如何和其他软件交互
-   读Emacs官方教程(快捷键 `M-x help-with-tutorial-spec-language`), 学会基本的文本操作 (大概十几个快捷键)
-   使用 Emacs 自带的 [org-mode](http://www.orgmode.org), org-mode 关键是用起来, 只要记住按 TAB 键是展开内容就可以了, 其他都不用学

Org-mode 是Emacs内置的插件.用来写文档,记笔记,管理个人工作事务等等. 有很多第三方插件拓展. 不是三言两语可以概况其功能的. 它最受欢迎的的特性是支持名为 [GTD (Getting Things Done)](https://en.wikipedia.org/wiki/Getting_Things_Done) 的工作流. 很多人认为 org-mode 是最好的GTD软件. 新手以此入门上手很快, 可以立刻提高自己的生产力.


<a id="org846ae7d"></a>

## 读官方教程

按以下步骤阅读教程:

-   不安装任何插件打开 Emacs, 比如在 Shell 中运行命令 `emacs -nw -Q`
-   `M-x help-with-tutorial` 打开教程

完成该教程仅需半小时.

即使不用 Emacs 默认快捷键, 这步也是必须的, 不要跳过!

最起码要知道以下命令,

-   `M-x describe-variable`, 快捷键 `C-h v`, 查看变量的文档
-   `M-x describe-function`, 快捷键 `C-h f`, 查看命令的文档
-   `M-x describe-key`, 快捷键 `C-h k`, 查看快捷键的文档


<a id="org40c0a28"></a>

## 以实际问题作为切入点

努力能很快得到回报, 会越学越有乐趣, 进入正反馈.

例如, 我急需 GTD 的工具, 而 Emacs 的 [Org-mode](http://orgmode.org/) 是同类软件中最好的. 用 Org-mode 节省了时间后, 我对 Emacs 兴趣高涨.

反面例子是啃Lisp教程开始Emacs之旅, 坚持下来的人寥寥无几.


<a id="orgab703be"></a>

## 待解决的问题设定优先度

关键在于理性地考虑你最迫切需要解决的一个问题.

**以这个问题作为出发点**, 除此之外都可以妥协.

虽然 Emacs 无所不能, 但是饭也要一口一口吃. 有时退一步等于进两步.

例如, 我一直以为 Emacs 的中文显示很完美, 搞不懂为什么有人在字体配置上花那么多时间.

在读者反馈后, 才明白原来我一直在终端下使用Emacs, 终端软件可以完美显示中文字体, 所以就没 Emacs 什么事了. 需要配置字体的人用的是图形界面 Emacs.

当初只在终端下使用 Emacs 是因为需连接到远程服务器. 我认为这是重点. 甚至为此放弃了漂亮的配色主题 (后来发觉此牺牲毫无必要). 塞翁失马, 由此也避免了图形界面版本的所有问题.


<a id="org71ffacc"></a>

## 站在巨人的肩膀上

刚开始我也是抱着玩的心态, 到处拷贝别人代码到我的配置中去. 浪费了很多时间.

后来我停止折腾, 安心用 [Steve Purcell](http://www.sanityinc.com/) 的 [Emacs 配置](https://github.com/purcell/emacs.d) , 从此走上正轨.

初学者开始阶段应以模仿为主. 这点是本文核心思想.

之前提过, 我选择不背快捷键,而用smex优化输入命令的效率.这也是因为我使用他人成熟配置后学会的.

考虑一下:

-   我就是这么做的, [看看一年内我给他报了多少 bug](https://github.com/purcell/emacs.d/issues?direction=asc&page=1&sort=created&state=closed)
-   要超越高手就必须了解其高度, 你需要一年时间去模仿去学习
-   基于 Purcell 的配置给他报 bug (甚至是提交patch), 你就是考虑到了他未考虑到的问题, 至少在这点就超过他了, 日积月累就很可观了


<a id="orgc05d10b"></a>

## 报 bug

像武侠小说那样拜高手为师是白日做梦. 唯一能让高手指点的办法是先付出. 最可靠的付出就是报 bug.

我就是这样 [学到一些高级 Lisp 技巧的](https://github.com/capitaomorte/yasnippet/issues/256).


<a id="org5bc0222"></a>

## 持续改进

要在高手已有工作上改善. 即使是微小的改善, 如果坚持一段时间, 就是巨大的进步了, 你就可以在这一点上笑傲江湖.

再找出另一高手需要改善的地方, 使用同样的方法.

例如, 默认在 Emacs 中移动子窗口焦点不是很方便. 需按 `C-x o` 多次. 我找到了 emacs 插件 [switch-window](https://github.com/dimitri/switch-window), 只要按 `C-x o` 一次, 会有提示子窗口编号, 接下来输入编号就可以了. 但还有改善空间, 我又找到了 [window-number.el](https://github.com/nschum/window-numbering.el), 只要按 `M-NUM` 一次. 这个方法已几乎完美, 但 Alt 键还是有点慢, 我结合 [evil](https://github.com/emacs-evil/evil) 和 [evil-leader](https://github.com/cofi/evil-leader), 可以按逗号和数字飞速切换子窗口了. 我的这个点子后来被[spacemacs采用](https://github.com/syl20bnr/spacemacs/commit/0931e4abece1307def3a024f4f2717359fb8d6e8).现在已是大多数Emacs用户的标准配置了.


<a id="orgb4c4cfb"></a>

## 加入社区更上一层楼

最重要的是专一. 不去定阅和 Emacs 无关的话题.


<a id="orge21f1fb"></a>

### Reddit

[Reddit](http://www.reddit.com/r/emacs/) 是最好的.


<a id="orged31382"></a>

### GitHub 是高手云集的地方

GitHub 的版本控制服务很好. 现在它的社区化倾向越来越强了, 我喜欢.

例如, 可以看一下 <https://github.com/search?p=1&q=stars%3A%3E20+extension%3Ael+language%3Aelisp&ref=searchresults&type=Repositories> 上最酷的 Emacs 插件.


<a id="orgd75e883"></a>

### 博客

最好的是 [Planet EmacsLife](https://planet.emacslife.com/), 多个 Emacs 博客的集合.


<a id="orgc3d032a"></a>

### 在 Stack Overflow 上搜索相关讨论

google &ldquo;emacs-related-keywords site:stackoverflow.com&rdquo;

我会定期搜索, 同一帖子反复精读. 因为讨论质量很高.

<http://emacs.stackexchange.com> 是 Stack Overflow 旗下专门的 Emacs 问答社区.


<a id="org1632e43"></a>

### 到 Youtube 上看 emacs 相关的视频

我就是看了 [Google Tech Talks 上这个 Org-mode 作者的介绍](http://www.youtube.com/watch?feature=player_embedded&v=oJTwQvgfgMM) 而爱上 org-mode.

不过 Youtube 搜索结果是最佳匹配的. 由于相关视频并不多, 如按照默认算法, 每次总是那几个. 所以如果关注最新进展, 搜索应以时间排序.


<a id="orgc960512"></a>

# 读书最有效


<a id="orgb577917"></a>

## EmacsWiki

[EmacsWiki](http://www.emacswiki.org/) 是社区维护的文档.

有人抱怨文档太乱, 质量参差不齐. 前者我有同感. 后者不赞同. EmacsWiki 文档质量相当高, 因其是 **唯一的** 半官方文档. 忍受其乱中有序的现状吧.

最佳阅读方法是, 选定一特定主题, 从头读到尾. 这样对最新进展都了解了. 是否要采用其建议另当别论.


<a id="orgf2d7d09"></a>

## Emacs Lisp 书籍推荐 (可选)

Bob Glickstein 的 [Writing GNU Emacs Extensions](http://www.amazon.com/Writing-GNU-Emacs-Extensions-Glickstein/dp/1565922611) 是最好的.

生动, 例子丰富. 作者用心安排了书的结构. 例如, 很早就介绍了 defadvice 的用法. defadvice 是 Emacs Lisp 的精华.

Xah Lee 提供 [付费 Lisp 教程](http://xahlee.info/emacs/emacs/buy_xah_emacs_tutorial.html) 也相当不错.


<a id="org027d9ec"></a>

# 知识管理

不要低估长时间的累积效应.

例如 Steve Purcell 的配置. 2000 年开始维护,其质量不用我多费口舌.

知识积累的越多, 这些知识之间的联系就会越多. 联系增长的速度是以指数的方式增长的. 如从头来过, 意味着积累知识的书面记录丢失了. 损失是很大的. 基数已归零, 增长的量又能有多少.

这也是后文谈到为什么要用工具保存配置和知识的原因.


<a id="org4c59fb7"></a>

## 配置纳入 GitHub 的版本控制

我的配置见 <https://github.com/redguardtoo/emacs.d>.

版本控制可以认为是一个集中式的知识管理, 任何时刻任何地点对配置的修改都要及时上传合并 (merge). 这是积累能力的关键.

共享实际也是一种利己行为, 很多人用我的配置等于帮我测试.


<a id="org10eb1ba"></a>

## 将相关资料备份

我还写了许多博客文章. 这些文章都存在 org 格式的文件中. 最后发布的静态博客也纳入版本控制, 参见 <http://github.com/redguardtoo/redguardtoo.github.io>.


<a id="org981fb2e"></a>

# 第三方插件推荐

建议对少数优秀插件深入研究.阅读甚至编写相关代码.

以下是清单：

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">名称</th>
<th scope="col" class="org-left">说明</th>
<th scope="col" class="org-left">同类插件</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left"><a href="https://github.com/emacs-evil/evil">Evil</a></td>
<td class="org-left">将 Emacs 变为 Vim</td>
<td class="org-left">没有</td>
</tr>


<tr>
<td class="org-left"><a href="http://orgmode.org/">Org</a></td>
<td class="org-left">Org-mode, 全能的笔记和GTD工具</td>
<td class="org-left">没有</td>
</tr>


<tr>
<td class="org-left"><a href="https://github.com/company-mode/company-mode">company-mode</a></td>
<td class="org-left">自动完成输入, 支持各种语言和后端</td>
<td class="org-left">auto-complete</td>
</tr>


<tr>
<td class="org-left"><a href="https://github.com/capitaomorte/yasnippet">yasnippet</a></td>
<td class="org-left">强大的文本模板输入工具</td>
<td class="org-left">没有</td>
</tr>


<tr>
<td class="org-left"><a href="http://www.emacswiki.org/emacs/FlyMake">flymake</a></td>
<td class="org-left">对不同语言做语法检查</td>
<td class="org-left">flycheck</td>
</tr>


<tr>
<td class="org-left"><a href="https://github.com/abo-abo/swiper/blob/master/ivy.el">ivy</a> or <a href="https://github.com/emacs-helm/helm">helm</a></td>
<td class="org-left">自动完成, 在其上有插件完成具体功能</td>
<td class="org-left">ido</td>
</tr>


<tr>
<td class="org-left"><a href="https://github.com/magit/magit">magit</a></td>
<td class="org-left">玩转 git</td>
<td class="org-left">没有</td>
</tr>
</tbody>
</table>


<a id="orgc067285"></a>

# Emacs 是一种生活方式

Geek 其他方面也很牛. 举一反三你收获会很多.

[Sacha Chua](http://sachachua.com/blog/) 就是这样的女孩, 这是她的 [Youtube 录像](http://www.youtube.com/watch?v=eoyi2vrsWow). 她学习的方式是 [让 Emacs 自动将手册语音合成](http://sachachua.com/blog/2012/07/transcript-emacs-chat-john-wiegley/), 这样她在房间里走来走去的时候也可以听文档了.

我现在有意识地整理高手名单, 观察他们 **除了 Emacs 外** 用什么工具.

例如, [js2-mode](https://github.com/mooz/js2-mode) 的维护者 Masafumi Oyamada (网名 mooz) 也开发了 [keysnail](https://github.com/mooz/keysnail) 和 [percol](https://github.com/mooz/percol). 特别是 percol, 使我命令行效率提高了 10 倍.

这个阶段可称之为 **心中有剑, 手中无剑**.

是否用 Emacs 不重要了, 重要的是随心所欲. 例如, 很多人争论哪个编辑器自带的文件管理较好. 我 [从 mooz 那学到大招后](http://blog.binchen.org/posts/how-to-do-the-file-navigation-efficiently.html), 就跳出五行外, 不在三界中了.


<a id="org4b2ab03"></a>

# 付之于行动

如何行动因人而异.

关键是真正理解本文要点.

例如，你是否意识到之前的章节意味着以下行动:

-   找出所有插件的作者
-   在 Twitter/GitHub/Reddit 上跟随他们
-   通读他们已发表的贴子


<a id="orgde4db21"></a>

# 使用 Evil

Evil 是 [Vim 模拟器](https://github.com/emacs-evil/evil).

如果你不熟悉 Vim, 在命令行里运行 `vimtutor` 或者安装 Emacs 插件 [evil-tutor](https://github.com/syl20bnr/evil-tutor) 学习 Vim 基本命令.

该教程大概需要半小时. 关于 Vim 的基本操作的讨论就到此为止了. 网上教程汗牛充栋, 你可自行阅读.

这里展示一些高级技巧 (有些技巧是我独创的).


<a id="org275be3a"></a>

## Text Object

了解 [Vim Text Object](http://vimdoc.sourceforge.net/htmldoc/motion.html) 的概念.

Evil 的强大之处就是你可以用 Emacs Lisp 来自定义 `Text Object`. 自由的 Lisp 使得你完全超越 Vim 的 &ldquo;约定俗成&rdquo;.

比如在操作自定义的 Text Object 时, 当前焦点完全可以在 Text Object 之外. 这是 Lisp 写的 [寻找附近的文件路径或者 URL.](http://blog.binchen.org/posts/evil-text-object-to-select-nearby-file-path.html) 用 Vim Script 写个类似的脚本难很多. 即使你用了 [vim-textobj-user](https://github.com/kana/vim-textobj-user) 之类的插件辅助开发也没用的.

而且 Lisp 代码完全可以调用 **任何** 的第三方插件或者 Emacs 的不计其数的 API. 比如 Evil 中操作 `Text Object` 的过程中可以问用户问题, 访问网站等等.

实现这些额外功能对 Vim 来说很难.


<a id="org999c259"></a>

## Leader 键

Vim 自带 Leader 键的功能, 你先按了 Leader 键 (很多人定义为空格键) 后, 再按其他键 (比如 `kk`) 会触发你自定义的命令. 本质就是给你更多的快捷键.

在 Emacs 中需要使用第三方插件如 [general.el](https://github.com/noctuid/general.el) 来实现此功能.

某些 Vim 用户不能迁移到 Evil 的原因就是自定义了太多使用 Ctrl 键的快捷键, 和 Emacs 默认的快捷键有冲突.

这些用户没有意识到的是借鉴 Emacs 的思想, 他们在 Vim 和 Emacs 的效率可以有巨大的提升. 我只提三点供参考:

第一, 充分利用 Leader 快捷键. 我看过大多数 Vim 高手在 GitHub 上的设置, 他们一般定义 **10 到 20 个** Leader 相关的快捷键.

我定义了 **300 个** 相关的快捷键.

典型 Evil 用户 (如 Spacemacs 用户) 大概有 **3000 到 10000 个** 相关快捷键可用.

第二, Vim 用户的另一个问题是快捷键没有优化. 常用命令的快捷键应按. 何为常用命令须来自 **真实数据**.

这是我用 Emacs 的插件 [keyfreq](https://github.com/dacap/keyfreq) 测试月的数据 (我的 Leader 键定义为逗号):

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-right" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">Times</th>
<th scope="col" class="org-right">Percentage</th>
<th scope="col" class="org-left">Command</th>
<th scope="col" class="org-left">Key</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">4967</td>
<td class="org-right">12.00%</td>
<td class="org-left">evilmi-jump-items</td>
<td class="org-left">%</td>
</tr>


<tr>
<td class="org-right">2892</td>
<td class="org-right">6.99%</td>
<td class="org-left">compile</td>
<td class="org-left">, o o</td>
</tr>


<tr>
<td class="org-right">2178</td>
<td class="org-right">5.26%</td>
<td class="org-left">find-file-in-project-by-selected</td>
<td class="org-left">, k k</td>
</tr>


<tr>
<td class="org-right">1953</td>
<td class="org-right">4.72%</td>
<td class="org-left">copy-to-x-clipboard</td>
<td class="org-left">, a a</td>
</tr>


<tr>
<td class="org-right">1566</td>
<td class="org-right">3.78%</td>
<td class="org-left">paste-from-x-clipboard</td>
<td class="org-left">, z z</td>
</tr>


<tr>
<td class="org-right">1227</td>
<td class="org-right">2.96%</td>
<td class="org-left">er/expand-region</td>
<td class="org-left">, x x</td>
</tr>


<tr>
<td class="org-right">897</td>
<td class="org-right">2.17%</td>
<td class="org-left">evil-repeat</td>
<td class="org-left">.</td>
</tr>


<tr>
<td class="org-right">866</td>
<td class="org-right">2.09%</td>
<td class="org-left">ido-find-file</td>
<td class="org-left">, x f, C-x C-f</td>
</tr>


<tr>
<td class="org-right">819</td>
<td class="org-right">1.98%</td>
<td class="org-left">toggle-full-window</td>
<td class="org-left">, f f</td>
</tr>


<tr>
<td class="org-right">815</td>
<td class="org-right">1.97%</td>
<td class="org-left">etags-select-find-tag-at-point</td>
<td class="org-left">C-], , h t</td>
</tr>


<tr>
<td class="org-right">721</td>
<td class="org-right">1.74%</td>
<td class="org-left">back-to-previous-buffer</td>
<td class="org-left">, b b</td>
</tr>


<tr>
<td class="org-right">682</td>
<td class="org-right">1.65%</td>
<td class="org-left">split-window-vertically</td>
<td class="org-left">, x 2</td>
</tr>


<tr>
<td class="org-right">539</td>
<td class="org-right">1.30%</td>
<td class="org-left">find-function</td>
<td class="org-left">, h f, C-h C-f</td>
</tr>


<tr>
<td class="org-right">494</td>
<td class="org-right">1.19%</td>
<td class="org-left">counsel-recentf-goto</td>
<td class="org-left">, r r</td>
</tr>


<tr>
<td class="org-right">397</td>
<td class="org-right">0.96%</td>
<td class="org-left">counsel-git-grep</td>
<td class="org-left">, g g</td>
</tr>


<tr>
<td class="org-right">376</td>
<td class="org-right">0.91%</td>
<td class="org-left">delete-other-windows</td>
<td class="org-left">, x 1, C-x 1</td>
</tr>


<tr>
<td class="org-right">372</td>
<td class="org-right">0.90%</td>
<td class="org-left">evilnc-comment-or-uncomment-lines</td>
<td class="org-left">, c i</td>
</tr>


<tr>
<td class="org-right">351</td>
<td class="org-right">0.85%</td>
<td class="org-left">eval-expression</td>
<td class="org-left">, e e, M-:</td>
</tr>


<tr>
<td class="org-right">326</td>
<td class="org-right">0.79%</td>
<td class="org-left">evilmi-select-items</td>
<td class="org-left">, s i</td>
</tr>


<tr>
<td class="org-right">320</td>
<td class="org-right">0.77%</td>
<td class="org-left">paredit-doublequote</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-right">307</td>
<td class="org-right">0.74%</td>
<td class="org-left">evil-filepath-outer-text-object</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-right">300</td>
<td class="org-right">0.72%</td>
<td class="org-left">steve-ido-choose-from-recentf</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-right">295</td>
<td class="org-right">0.71%</td>
<td class="org-left">split-window-horizontally</td>
<td class="org-left">, x 3</td>
</tr>


<tr>
<td class="org-right">283</td>
<td class="org-right">0.68%</td>
<td class="org-left">git-add-current-file</td>
<td class="org-left">, x v a</td>
</tr>


<tr>
<td class="org-right">279</td>
<td class="org-right">0.67%</td>
<td class="org-left">winner-undo</td>
<td class="org-left">, x u, , s u, C-x 4 u</td>
</tr>


<tr>
<td class="org-right">278</td>
<td class="org-right">0.67%</td>
<td class="org-left">describe-function</td>
<td class="org-left">, h d, C-h f</td>
</tr>


<tr>
<td class="org-right">278</td>
<td class="org-right">0.67%</td>
<td class="org-left">evil-goto-mark-line</td>
<td class="org-left">&rsquo;</td>
</tr>


<tr>
<td class="org-right">269</td>
<td class="org-right">0.65%</td>
<td class="org-left">ido-kill-buffer</td>
<td class="org-left">, x k, C-x k</td>
</tr>


<tr>
<td class="org-right">254</td>
<td class="org-right">0.61%</td>
<td class="org-left">evil-goto-definition</td>
<td class="org-left">g d</td>
</tr>


<tr>
<td class="org-right">253</td>
<td class="org-right">0.61%</td>
<td class="org-left">pop-tag-mark</td>
<td class="org-left">M-*</td>
</tr>


<tr>
<td class="org-right">251</td>
<td class="org-right">0.61%</td>
<td class="org-left">git-messenger:popup-message</td>
<td class="org-left">, x v b, C-x v p</td>
</tr>


<tr>
<td class="org-right">246</td>
<td class="org-right">0.59%</td>
<td class="org-left">my-goto-next-hunk</td>
<td class="org-left">, n n</td>
</tr>


<tr>
<td class="org-right">237</td>
<td class="org-right">0.57%</td>
<td class="org-left">evilnc-comment-operator</td>
<td class="org-left">, ,</td>
</tr>


<tr>
<td class="org-right">235</td>
<td class="org-right">0.57%</td>
<td class="org-left">flyspell-goto-next-error</td>
<td class="org-left">, f e, C-,</td>
</tr>


<tr>
<td class="org-right">214</td>
<td class="org-right">0.52%</td>
<td class="org-left">evil-exit-emacs-state</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-right">212</td>
<td class="org-right">0.51%</td>
<td class="org-left">browse-kill-ring-forward</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-right">210</td>
<td class="org-right">0.51%</td>
<td class="org-left">flyspell-buffer</td>
<td class="org-left">, f b</td>
</tr>
</tbody>
</table>

第三, 由于 Lisp 的强大 Leader 键的使用在 Emacs 中有无限可能

-   使用 [general.el](https://github.com/noctuid/general.el) 定义多个 Leader 键
-   可在切换文件时切换 Leader 键等等.


<a id="org4d54242"></a>

## Evil 兼容 Emacs 原生插件

如果你真正理解了我前面的章节, 这就根本不是问题.

之前我提到了要保持头脑开放, 要尽可能抄高手的代码, 积极地报 bug 等观点. 现在让我演示一下如何应用.

一开始我每装一个新的插件, 都要辛辛苦苦设置 evil 的快捷键.

有一天我问自己, Lisp 那么强大, Evil 那么优秀, 也许有更方便简洁的方案?许多人说不行不一定是真理, 只有实际调查过的人才有发言权.

我也没有自己钻研 Evil 的代码, 取而代之的是 [给 Evil 的开发者 Frank Fischer 报了个 bug](https://github.com/emacs-evil/evil/issues/511), 他给我了一个方案, 根本不需要重设快捷键.

这是这个方案在 [git-timemachine 中](https://github.com/emacsmirror/git-timemachine) 的 [完美应用](http://emacs.stackexchange.com/questions/9842/disable-evil-mode-when-git-timemachine-mode-is-activated).


<a id="org4289f02"></a>

## Evil 专用的插件介绍

我选择 [MELPA](http://melpa.org) 上最流行的5个Evil插件介绍一下, 类似优秀插件还有很多.

要点不在于你装了多少插件, 而在于理解由于 Lisp 的强大和 Emacs 的自由, 这些插件功能更多, 更容易拓展.


<a id="org710ce4c"></a>

### [evil-surround](https://github.com/timcharper/evil-surround)

对应 [vim-surround](https://github.com/tpope/vim-surround).

我通常用 [expand-region 选中一段文本, 然后按 `S` 或者 `M-x evil-surround-region` , 再按任意字符 (比如双引号) 就可以在文本](https://github.com/magnars/expand-region.el/blob/master/expand-region-core.el) 首尾两端附加该字符.

当然它也支持修改删除操作.

之前提到的 text object 也完美支持.

懂 Lisp 的话可以修改 `evil-surround-operator-alist` 自己定制操作.


<a id="orgd773a5c"></a>

### [evil-nerd-commenter](https://github.com/redguardtoo/evil-nerd-commenter)

对应 [vim-nerd-commenter](https://github.com/scrooloose/nerdcommenter), 这是我写的, 功能更强大.

你可以 `M-x 5 evilnc-comment-or-uncomment-lines` 快速注释当前 5 行或者取消注释当前 5 行.

你也可以选中一个区域 `M-x evilnc-comment-or-uncomment-lines`

由于 Emacs 的强大, 默认就支持所有世界上已知的语言, 而核心代码也就是 1 行而已. Vim 插件对应的功能代码要有 400 行.

如果你在 [org-mode 格式的单一文件中](http://orgmode.org/) 中混杂多种语言的话, 它也能智能识别.

这个功能在 Vim 中基本不可能实现.


<a id="orgd65fcb3"></a>

### [evil-matchit](https://github.com/redguardtoo/evil-matchit)

对应 [vim-matchit](https://github.com/tmhedberg/matchit). 又是我写的. 自然功能更强大.

本质就是你当前焦点在文件的某个位置 A, 你按 `%` 或者 `M-x evilmi-jump-items`, 焦点移到位置 B, 你再按同样的键, 又回到了位置 A.

比如在一个 HTML 文件中, 你就可以在 `<body>` 和 `</body>` 间跳来跳去. 其他各种编程语言都支持.

Vim 对应的代码我读过, 限制比较多, 比如你一定要先定义一对正则表达式来匹配 A 和 B 的位置. 这种限制在某些语言如 Python 中就会比较麻烦.

Emacs 的实现就完全体现了 Emacs 的自由精神, 我建立了一个动态查询的矩阵, 矩阵的元素就是函数对象而已. 用户可以在运行时替换这些函数对象, 所以怎么跳转, 跳到哪都是完全自由的.

所以 python 的支持就毫无问题. 想支持更多的语言或者对我的实现不满意, 在 `.emacs` 中写几行 Lisp 代码就可以了.


<a id="org9bcfcae"></a>

### [evil-escape](https://github.com/syl20bnr/evil-escape)

按自定义快捷键退出当前的各种状态, 相当于 Vim 中的 `ESC` 或者 Emacs 中的 `C-g`.

我定义自定义快捷键为 `kj`. 如果你想效率高的话, 取消的默认快捷键就太慢了.

让我给你举个例子说明什么叫效率高. 我移动手指去按 ESC 键需要 0.5 秒.

Sublime Text 默认的文本搜索要比我的 Emacs 设置慢 40 倍. 如果 Sublime Text 搜索需要 40 秒, 那么节省取消键的 0.5 秒毫无意义.

Emacs 只要 1 秒完成搜索, 所以取消键从 0.5 秒减少到 0.1 秒的感觉就完全不一样.


<a id="org94e1ffa"></a>

### [evil-visualstar](https://github.com/bling/evil-visualstar)

对应 [vim-visual-star-search.](https://github.com/bronson/vim-visual-star-search)

选择一段文本, 按 `#` 或者 `*` 搜索.


<a id="org7b547c1"></a>

## 在 Shell 和 Interactive Interpreter 中使用 Evil

可以 `M-x shell` 或者 `M-x term` 进入 Shell.

传统上大家都在 Shell 中用 Emacs 的默认快捷键.

不过仔细计算过后我发现 Vim 的快捷键更有效率.

Shell 的作用无非就是运行命令或脚本代码, 输出运算结果.

当我们在 Emacs 中运行 Shell 的时候, 命令和代码往往是从别的地方拷贝过来的.

粘贴命令和代码到 Shell 中, 分析/过滤/搜索输出的结果, 都是 Vim 的快捷键更方便.

我之前提到的所有关于 Evil 的技巧和插件都适用于此.

Interactive Interpreter 和 Shell 没有本质区别, 无非就是解释器支持的语言不一样罢了. 比如 [inf-ruby](https://github.com/nonsequitur/inf-ruby) 支持 Ruby.

可以按 `C-z` 切换回纯 Emacs 快捷键.


<a id="org46e1ff2"></a>

## Evil 的小结

对 Vim 用户来说, Evil 不仅提供了 Vim 的完美模拟, 还开辟了用 Lisp 拓展 Vim 的新世界.

对 Emacs 用户来说, Evil 也不仅仅是提供了新的快捷键, 而是提供了更多的可编程的数据结构和范式 (如 text object).

关键是发挥你的创造力, 自由地接合 Emacs 和 Vim 的长处, 发明新技术和新技巧. 这种机会目前是很多的, 赶快行动起来吧.


<a id="orgab537db"></a>

# 答疑


<a id="org2ad4661"></a>

## 新手怎么开始

到 <https://github.com/redguardtoo/emacs.d> 参考 &ldquo;Install stable version in easiest way&rdquo; 一节.

只要点击下载两个 zip 文件就可以了, 不需 git 的任何知识.


<a id="org8b73282"></a>

## 如和理解他人配置

除了官方文档外. 看 EmacsWiki 和源代码也很有效. 窍门是源代码文件的头部有使用指南和作者的联系方式.


<a id="org49a6fcf"></a>

## 他人配置是否太重量级?

成熟配置都是轻量级的, 因为优化过了.

例如有种叫 [Autoload](http://www.gnu.org/software/emacs/manual/html_node/elisp/Autoload.html) 的技术. 只有用到模块的某一功能时那个模块才会被载入内存.


<a id="org8fb3ce4"></a>

## 其他第三方配置

[搜 github](https://github.com/search?l=Emacs+Lisp&o=desc&q=emacs&ref=searchresults&s=stars&type=Repositories)

也可用 [我的配置](https://github.com/redguardtoo/emacs.d)：


<a id="orga01fc3a"></a>

## 该使用 Emacs 的哪个版本

目前稳定版是 27.2. 通常不用担心版本问题. 主流的 Linux 发行版会处理.


<a id="orgf29d0f3"></a>

## Vi 用户要转阵营吗?

嘿嘿, 我也是 Vi 精通后转到 Emacs 的. 就是因为 Emacs 的强大 (例如和 gdb 的完美结合) 以及其脚本语言是 Lisp.

当然 Vi 的多模式编辑和快捷键比 Emacs 要高效得多, 所以最佳方案是 Vi + Emacs.

目前我用 [Evil](http://www.emacswiki.org/Evil), 在 Emacs 下模拟 Vim, 结合两者优点.

现在我是 **神用编辑器之神**!


<a id="org1918f8d"></a>

## 为什么很多 Vi 用户不接受 Evil?

因为他们对 Vim 快捷键做了深度配置. Emacs 默认要经常按 Ctrl 键, 如自定义的 Vim 快捷键也用 Ctrl 键, 难免有冲突.

解决办法是大家都使 [Leader](http://stackoverflow.com/questions/1764263/what-is-the-leader-in-a-vimrc) (Vim 直接支持, Emacs 需 [第三方插件](https://github.com/cofi/evil-leader)).

还有一个办法是待在 Vim 的舒适区里. 如能忍受没有 Org-mode 和 Lisp 的生活, 那么不会有问题.

如犹豫不决, 请重读 &ldquo;态度决定一切&rdquo; 一节.

我一旦认识到 Evil 和 Evil-leader 的潜力, 立刻把我 Vim 的设置按 Emacs 的重设了一遍。

更光辉灿烂的例子就是Spacemacs作者了, 无数的 github 星星代表了他的成功.


<a id="org1cd5358"></a>

## 不习惯默认快捷键, 怎么办？

**忍**!

默认快捷键经过几十年考验相当高效, 未成为高手前还是要忍.

如一定要在用 Windows 快捷键的, 可考虑 [ergoemacs](http://xahlee.info/emacs/).


<a id="orgdd500c3"></a>

## 使用第三方配置后有些奇怪的 bug, 怎么改?

不要改! 参考上文 [站在巨人的肩膀上](https://github.com/redguardtoo/mastering-emacs-in-one-year-guide/blob/master/guide-zh.org#站在巨人的肩膀上) 一章, 你觉得奇怪是因为缺乏经验, 把某些特性误认为是 bug. 请坚持至少一年.

例如, 有人反映右边第 80 列处总有一竖线, 希望能去掉.

实际上这是一特性, 提醒用户一行宽度不要超过第 80 列. 这是 [每行不要超过 80 列的原因](http://www.emacswiki.org/emacs/EightyColumnRule).

我建议第一年应 **尽量理解而不妄加判断**.


<a id="orgc426d2d"></a>

## 已更新软件包, 但是没有任何作用, 也没有任何错误信息

删除 HOME 目录下的 `.emacs`, `~/.emacs.d/init.el` 取代原来的 `.emacs`.


<a id="org651868a"></a>

## 有配置问题

-   读官方教程
-   善用网络和我提供的信息

例如,
问：在 `.emacs.d` 中的 `init.el` 文件起什么作用？
答：搜索 &ldquo;emacswiki init.el&rdquo;.


<a id="org470243c"></a>

## 启动报错

先确认已装上了 **你需要的** 第三方命令行工具, 这些工具是可选的, 清单见 [我的 README](https://github.com/redguardtoo/emacs.d).

如排除了以上原因, 带上 `--debug-init` 参数重新启动, 然后将错误信息及环境报告到对应的开发者.

报告时应给出细节. 例如很多读者给我的 bug 都是由于第三方插件版本较新引起的, 我拿到版本号后, 才能下载特定版本以重现 bug. 否则只能靠猜, 来回邮件浪费很多时间.


<a id="orgf48784f"></a>

## 自己的简单配置好控制

那你就是走我后悔莫及的老路, 一个人在黑暗中摸索. 开头兴致很高, 但现实是残酷的, 碰到复杂问题解决不了. 只能逃避, 借口 Emacs 太复杂而放弃了.

我最终醒悟过来走上光明大道, 很多走上岐路的人恐怕就没这个觉悟和毅力了.

希望自己掌控坦率地说是一个非技术问题, 因为没有自信心, 所以有补偿心态. 希望通过一种错误的方式来证明自己. 结局无非是恶性循环.

正确地方法是放下身段至少一年 (我已反复强调这一点), 打好基本功, 读书, 虚心学习.


<a id="orge2344f5"></a>

## 自己加的插件无效

Emacs 是个开放平台, 其众多插件发布前并不一定有严格的测试. 所以插件之间可能有冲突.

这也是我为什么建议初学者直接使用第三方配置配置的原因, 众多兼容性问题已解决.

没解决的问题最好提交bug报告, 而不是自己去钻研 Lisp.


<a id="org05c6f00"></a>

## 我想用 Windows 版本的 Emacs 而不是 Cygwin 版本, 怎么做?

需对命令行操作熟悉. 关键知识点有两个：

1.  设置 `HOME` 环境变量, 因为 `.emacs.d` 中的某些 Lisp 脚本假定 `.emacs.d` 在 HOME 所指定的路径中.
2.  Emacs 的某些功能需要使用第三方的命令行工具, 这些工具的路径应该添加至环境变量 `PATH` 中 (可选, 原因见后面).

如你不知道如何在 Windows 下添加修改环境变量, 不知道如何安装第三方工具, 建议还是先用 Cygwin 中的 Emacs, 因它已自带工具, 没有的话安装也方便. 且在 Cygwin 下环境变量 HOME 默认已设.

第三方命令行工具清单请参考[我的配置](https://github.com/redguardtoo/emacs.d)中的 README.


<a id="org178da7d"></a>

## Emacs 在代码跳转和自动完成上和商业 IDE 有差距, 怎么办?

现在流行[基于LSP的方案](https://melpa.org/#/?q=lsp).

我通常用 `Ctags` 作为后端引擎, 因其通吃所有语言. 虽然解析效果差一点, 但是恰当的命名规范 (尽量少重名) 可以弥补.

Java 和 C# 语言的主力开发工具最好用 IDE 而不是 Emacs.


<a id="orga7e63f1"></a>

## 邮件

我用 [Gnus](http://www.gnus.org/). 但有很多其他方案.

如你必须访问 Microsoft Exchange Servers, 还要用 [Davmail](http://davmail.sourceforge.net/).

用了 Davmail 后, 还可以用 [Popfile](http://getpopfile.org/) 来分捡邮件. Davmail + Popfile 让我生活在天堂.


<a id="org7080547"></a>

## 为什么 Emacs 启动时从服务器 (elpa) 安装第三方软件包 (package) 会失败?

请启动 Emacs 后, 运行 `M-x package-refresh-contents` 以从服务器更新软件索引, 然后重启 Emacs 即可.


<a id="orgdb007d2"></a>

## 有些网站 Emacs 访问不了

在命令行中启动 Emacs 时加上 `http_proxy=your-proxy-server-ip:port` 前缀.

例如,

    http_proxy=http://127.0.0.1:8000 emacs -nw


<a id="org7ad80d4"></a>

## 是否应尽早学习 Emacs Lisp

不用,顺其自然最好.

Lisp 语法和通常的语言不同, 除非有相当编程经验 (至少 10 年), 一般人都会对其有一点负面情绪 (当然是毫无道理的偏见!). 学习任何新东西, 长期来说兴趣最重要. 一开始应避免任何负面情绪.

Emacs Lisp 又是只用于 Emacs 的语言, 有大量术语需要掌握. 如 &ldquo;Buffer&rdquo;, &ldquo;Yank&rdquo;, &ldquo;Font face&rdquo;, 只有资深用户才能理解.

所以在使用经验不足前学习软件拓展语言(Domain Specific Language)很低效.

参考前文关于找到切入点的一节, 我推荐的顺序是, 先用优秀的配置享受到好处, 有了兴趣后学习 Lisp 就水到渠成了.

选择适合自己的路, 一年以后天才和普通人达到的高度都是一样的.


<a id="orgca0eadd"></a>

## 掌握 Emacs Lisp 是否是成为高手的必要条件?

否. 但 Lisp 是很强大的语言, 特点是一切皆可改. 当我说 &ldquo;一切&rdquo; 的时候, 我就是指字面意义上的 &ldquo;一切&rdquo;, 不是修辞上的夸张.

我用过许多编辑器, 除了 Emacs 没有一个能做到 &ldquo;一切可改&rdquo; 这点 Vim 也不行.

学点 Lisp 对提高 Emacs 水平没坏处. 另外 Lisp 语法不错, 值得一学.

顺便说一下, Lisp 很简单, 比 VB 容易多了, 一旦你适应其语法, 就会发觉它其实蛮友好的, 至少少打很多字.


<a id="org34be8ec"></a>

## 有必要学习键盘宏 (Keyboard Macros) 吗?

没必要, Lisp 足够了.

但是键盘宏生成的 Lisp 代码有时候比较有趣, 建议你精通 Lisp 后再来玩玩键盘宏.


<a id="orgfc6e2a9"></a>

## 基本操作我会了, 下一步学什么迷茫中

关键是你打算用这把瑞士军刀做什么.

前文已强调过以兴趣和解决实际问题作为切入点.

举一些我自己的例子说明:

-   我有写博客需要, 懒得用 Wordpress 那个破界面, 所以用 [org2blog](https://github.com/punchagan/org2blog)
-   开发 Ruby on Rails 程序需要 IDE, 装了 rinari
-   做跨平台 C++ 桌面开发, 装了 cmake-mode
-   需在多个子窗口间跳来跳去, 所以装了 [window-numbering.el](https://github.com/nschum/window-numbering.el)
-   大项目需同时调试多种语言, 所以装了 [evil-nerd-commenter](https://github.com/redguardtoo/evil-nerd-commenter), 这样不用记特定语言的语法就可注释掉代码.


<a id="org631ae9e"></a>

## 如何学习 org-mode?

[Org-mode 简明手册](http://www.cnblogs.com/Open_Source/archive/2011/07/17/2108747.html) 是不错的中文教程.

最好的英文教程是 Carsten Dominik (Org-mode 发明者) 在 [google tech talks 上的演讲](http://orgmode.org/talks.html). 其要点为 org-mode 本质是一个文本文件, 只要记住按 TAB 展开或者缩进条目就可以了. 其他特性可慢慢学.


<a id="org61c8d8b"></a>

## 对于 &ldquo;一切都用 Emacs 来完成&rdquo; 的观点你怎么看?

不要走火入魔. Emacs 本质是个平台, 提供了无限可能性.

从实用角度讲, Emacs 和其他工具结合有时能更快完成工作 (不过在没有一年的修炼之前 **千万不要猜 Emacs 不能做什么**).

以下是 Emacs 不一定能吃独食的地方:

-   剪贴簿: 应结合命令行工具 xsel (Linux) /pbpaste (OSX) /putclip (Cygwin)
-   Web 浏览: 用传统浏览器配合其插件
-   远程登录管理: 用 screen/tmux
-   FTP: 用专门的 FTP 软件
-   文件管理: 用专用软件
-   Lisp 速度比较慢，如有大计算量的工作, 交给第三方工具来作.

重点是头脑灵活, 既坚信 Emacs 无所不能, 也适当变通.


<a id="orgb3d068b"></a>

# 联系我

这是我的 [Twitter](https://twitter.com/#!/chen_bin) 和 [Google Plus](https://plus.google.com/110954683162859211810) 以及 [微博](http://www.weibo.com/u/2453581630), 我在新浪微博账号&ldquo;emacsguru&rdquo;.

博客为 <http://blog.binchen.org>.

我不回答具体配置的问题. 如你通读本文, 应知道哪里找答案更好.


<a id="orge99e655"></a>

# 结语

再强调一下本文最重要的观点:

-   以 **解决实际问题** 产生的兴趣引导
-   **完全照抄世界顶尖高手如 Steve Purcell 的配置**, 尽量避免自己写 Lisp
-   给高手报 bug 就是最好的学习,
-   学习 Emacs 和 **学任何专业技能 (拉小提琴, 解数学题) 的方法论都是一样的**, 请参考 [一万小时天才理论](http://book.douban.com/subject/4726323/).

关键是你以严肃的态度把其当作专业技能学习.

很多人之所以不赞同我的核心观点, 是因为内心深处还有把 Emacs 当玩具来炫耀 &ldquo;我有多酷&rdquo; 的意识.

Emacs 强大到可以作为另类娱乐来博眼球. 但本质是专业人士使用的神器.

打个比方, 职业杀手对于刀只关心两件事:

1.  高效地杀人
2.  任何环境下都可靠

刀的装饰是否漂亮或技巧是否自己原创对他并不重要.

Emacs 就是那把刀.

