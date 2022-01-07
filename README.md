# FreeBSD 从入门到跑路

## 概述

(↓↓↓ 正文阅读请点击下方的项目预览 ↓↓↓)

[项目预览——如果你认为拼音显得奇怪，那么你应该点击此处。](https://book.freebsdcn.org)

PDF 请点击 “[Release](https://github.com/FreeBSD-Ask/FreeBSD-Ask/releases)”下载。请注意，PDF 仅供参考，且存在这样或那样的问题，应该以在线版本为主。

### 本书定位

我们的目标并非是 Handbook 的翻译，而是编写一本类似于《鸟哥的 Linux 私房菜：基础学习篇》+《鸟哥的 Linux 私房菜：服务器架设篇》二合一的基于 FreeBSD 的教程。也就说我们是 Handbook 的超集。

### 编辑指南概要

我们欢迎所有支持 FreeBSD 的人进行编写，并会将您添加到贡献者名单当中。

[详细的编辑指南，点击此处](https://github.com/FreeBSD-Ask/FreeBSD-Ask/wiki)。

## 前言

### FreeBSD 从入门到跑路

本书诞生于 2021 年 12 月 19 日。编写目的是为了促进 FreeBSD 的中国化与世界化。编写内容为 FreeBSD 的基础与高阶知识。对于章节安排，如果你有一定的计算机基础可以跳过第 〇 章，如果你对 FreeBSD 有一定认识，欢迎你加入我们一起编写本书，贡献自己的力量。

### 内容提要

本书是由道长发起，并由 FreeBSD QQ 群 731675387 的一些群成员参与编写的《FreeBSD 从入门到跑路》。我们尝试从 0 开始，带领普通人走进 FreeBSD 世界，充分参考了 FreeBSD Handbook，构建了一个完整、科学的目录体系。本书不是一个教程的大杂烩亦或者是大集合，而是为了构建一个自成体系的一本开源书籍。全书共分二十九章，既强调了学习 FreeBSD 的必要基础也提供了内核设计与实现等专业性较强的教程。本书可作为高等学校“FreeBSD 操作系统”课程的本科生教材，同时也适合相关专业研究生或计算机技术人员参考阅读。

### 开源维护与捐赠

![](.gitbook/assets/proud_donor.gif)

[点此捐赠 FreeBSD 基金会](https://freebsdfoundation.org/donate)。

为了能够更好地维护本书，我们采用了 Gitbook 平台来进行协作。对于无法直接从 GitBook 导出为 PDF 的问题（我们提供了 PDF 的参考版本于 release），我们深感抱歉，我们目前没有财力为其提供所需要的企业版本（15 刀一个月）。如果您想为我们提供捐助，请加入我们的 [TG 群](https://t.me/freebsdba) 或者 QQ 群 731675387。 如果您也想参与编写，具体请参考 [WIKI](https://github.com/FreeBSD-Ask/FreeBSD-Ask/wiki/%E3%80%8AFreeBSD-%E4%BB%8E%E5%85%A5%E9%97%A8%E5%88%B0%E8%B7%91%E8%B7%AF%E3%80%8B%E7%BC%96%E8%BE%91%E6%8C%87%E5%8D%97)，关于贡献者名单请参考 第一章 第九节。

### 意见反馈

由于编写者水平所限，书中缺点和谬误之处自不可免，希望同志们随时提出批评意见，以便修正。您可以利用 Github 的各种交互功能与我们联系：提交 Issue、Pull request 或者加入 QQ 群或 TG 群直接联系（yklaxds AT gmail DOT com）等。

### TODO / Wishlist

后续还有很多需要完善的工作，包括不限于:

* 完善教程
* 整理和上传配置文件和环境
* 对教程的格式目录进行优化调整
* 积极对外宣传并寻求正式出版

### 许可证

本书采用 [BSD-3-Clause License](LICENSE/) 许可证开源。我们在编写过程吸收了一些现有的研究成果，在此表示感谢。

### 同名小说

起点网——[《FreeBSD从入门到跑路》](https://book.qidian.com/info/1031738676)

## 关于

### FreeBSD 中文社区的愿景

我们成立于 2018年3月17日。由贴吧——FreeBSD 吧发展到了 QQ 群（主群 731675387），Telegram 群，乃至于微信群。

我们的成员具有非常大的广泛性和普遍性，能够代表绝大多数 FreeBSD 用户的平均水平：可能根本没有听说过何为 FreeBSD，但这并不影响我们的交流与沟通，也许有人觉得这是浪费时间，但是没有新生力量的培养，何来 FreeBSD 的明天呢？谁不知道新人可能有很多坏习惯呢。

同鲁迅先生说的那样，但愿每个人都是一束光，照亮 FreeBSD 在中国大陆地区前进的光荣的荆棘路。也希望，你可以加入我们，共同组成漫天星光亦或者是星星之火。

无穷的远方，无数的人们，都和我有关。

我曾无数次眺望远山，想要找到一汪清泉，天总是不随人愿，还是没有找到。

我是谁，我们是谁？这个问题永远也不会有结果。

我们选择 FreeBSD，是因为想选择一个清晰、明了、可靠、稳固的一个操作系统在工作上给我们带来收益以及在生活中给我们带来乐趣。当然 FreeBSD 还存在很多问题，有待大家积极发现、探讨、完善，社会在进步，技术在进步，热情丝毫不减在持续，未来越来越美好。

### 黑名单

在建设 FreeBSD 中文社区的时候我们遇到了许多困难：一些 Arch linux 邪教分子的恶意挑衅，上来就说“Arch 牛逼！”；还有一些完全没有使用过 BSD 的人，张口就说 FreeBSD 没有 JAVA、没有 JNI，更没有 Eclipse；还有部分华为花粉进入社区故意借套壳安卓的鸿蒙系统，试图引发内讧。为了社区，我们建立了黑名单制度。

名单如下：

#### 2021

|QQ 号|黑名单原因|
|:---:|:---:|
|3623404390|过河拆桥，得到问题答案就退群，下同|
|554412630|送上了高考大礼包，为了逃避权限退群|
|1354998|侮辱 BSD 且推广 Linux|
|156798543|寻衅滋事|
|1113749776|过河拆桥，华为海狗|
|2151722905|进群胡言乱语装萌新，装傻充愣，名字叫数据库，疑似一个人工智能，擅长问一些乱七八糟的拼凑起来的不存在的问题：比如`汇编语言  c 语言之间，存在一门语言。被忽略了。整个IT界失去了一次另外发展的模式。`再比如`数据库表之一行记录，是可看做，某个函数的参数么？这个函数名，为什么没出现在这条记录行？是省略了函数名么？它以这个表做参数吗？它用这个表的数据流做参数吗？`又比如`编程语言，可能可以不依赖代数 不依赖几何 在更广阔的观点，编程语言可以构造代数 构造几何。只不过，暂时还没想透彻。`和`框架  ， 是什么 ？ 是设备吗？在 看vue 对列  ，是设备吗？为什么，去电脑城，可以买到cpu  内存条 磁盘。买不到 对列？`以及`假设println()  是服务性函数与main一起启动不会关闭。参数流 随时可以  写入。传统对于函数的解释，可能是错误的。实用性  可行性掩盖了粗糙性荒谬性。很可能 ，函数禁用名称 函数禁用注释，才是对劲的。（不过，现在的实用观点不允许这么说这么做）。函数无名化，函数去注释，现实无法接受。`如需更多，请提交 issue|
|504658598|骂人|
|3458921559|侮辱 BSD 且推广`ArchLinux`，认为 BSD 没有`JAVA`、没有`JNI`、没有`Eclipse`等，拿出来被打脸又东拉西扯开始挑衅管理员，外号叫彩虹海盗，现在叫“大明酱”，其 github 地址为 https://github.com/mingmoe |
|2018456|侮辱 BSD，挑衅管理员|
|383925617|华为海狗，侮辱管理员|
|1510908166|过河拆桥|
|1771336464|寻衅滋事|
|595063679|提出与常识不符的文史哲观点，认为金字塔是水泥造的，认为外国历史都是虚假的，我大天朝的才是正史|
|273457914|提出与常识不符的文史哲观点，不认识阿拉伯百年翻译运动就敢妄论西欧历史，宣称同上|
|571060051|屡次阴阳怪气破坏氛围|
|3303672033|开源邪教，半瓶水晃荡，认为`LaTeX`在写小说方面优于`Word`，认为`libreoffice`不应该兼容`Word`，应该反过来由`Word`去兼容他,经典语录"你凭什么说 Libreoffice 兼容性不好?"，“你为什么不用 GIMP？为什么用 PS”，“你为什么用 Windows 10”。侮辱挑衅管理员，擅长各种举报打小报告，造成管理员手机号被封（目前已解）|

|微信名称|黑名单原因|
|:---:|:---:|
|彩虹海盗|侮辱 BSD 且推广`ArchLinux`。其他同上|

|贴吧 ID|黑名单原因|
|:---:|:---:|
|mechrtt|挑衅管理员|

#### 2022

|QQ 号|黑名单原因|
|:---:|:---:|
|||
|||
|||

|微信名称|黑名单原因|
|:---:|:---:|
|||
|||

|贴吧 ID|黑名单原因|
|:---:|:---:|
|||
|||
|||

希望各大论坛 QQ 群社区引以为戒，小心上述人员的恶意破坏。


### 申诉须知：

黑名单用户若要申诉方式有二，任选其一即可：

①手写 3 万字以上悔过书（要求使用“简体中文，现代汉语”，且字数不含标点符号）。必须予以录制视频（1080P 30FPS 为底线，要求看清所写内容与双手），以防机器抄写，且不允许视频快放。同时将电子版附上以便于查重。我们将视其情节严重与悔过程度（文本重复率等）考虑解禁，并将在 30 个工作日内给出解禁与否的回复。悔过书和视频以及电子文本请提交到 issue，附上被封渠道与账号。请注意，每次我们只能解禁一个渠道的账号，也即一份悔过书只能解禁一个平台的一个账号。每个人终身只有两次申诉的机会（包括申诉失败）。

②参与 FreeBSD 社区建设，完善本教程。Github 的提交数量在 300 次以上，即可解封一个账号。提交必须是有意义的，不得先删后增，否则不计入总次数且永久性拉黑。

