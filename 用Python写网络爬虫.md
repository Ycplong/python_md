／
写
［澳］RichLaarwds on 著
李斌 译
人民邮电出版社
北 京图书在版编目（CIP）数据
用Python写网络爬虫／（澳大）利理亚查德·劳森
(RichLaarwds 著o；n）李斌译． 一北京：人民邮电出
版社，2016.9
ISBN9 78-7-115-43179一0
I .①用…II.①理…②李…III①.软件工具一程
序设计N. ①TP31.156
中国版本图书馆CIP数据核宇（201）6第177976号
版权声明
Co严pgiht201P5ak cPtu ibslhFisipntrug b.l iitnsh Ehenel gdil sahan ggueunr dt ehteiW telSbec rawpiPitynhtg h on.
©
RgihtRserv seed.
All
本书由英国PakctPubl公i司s授h权i人n民g邮电出版社出版。未经出版者书许面可， 对本书的任何部分不
得以任何方式或任何手段复制和传。播
版权所有，侵权必究。
’ 著 ［澳R］cihaawrsdo nL
译 李 斌
责任编辑傅道坤
责任印制焦志炜
’ 人民邮电出版社出版发行
北京市丰台区成寿寺路II号
邮编 100164电 子邮件 3 5l@ ptpress.com.cn
网址 httwwpw:.//ptpress.com.cn
三河市海波印有务限公司印刷
’开本：
800x!O1O/O1 6
印张：10.75
字数z14千8字 2016年9月第l版
印数z1-3000册 2016年9月河北第1次印刷
著作权合同登号记 0-1201369-2号6
图字：
4050.元
定价：
读者服务热线：(01801)0 554印1装0质 量热线：（01801)055316
反盗版热线：（01801)055315内 容提要
本书讲解了如何使用P川lOil来编写网络爬虫程序，内容包括网络爬虫简
介，从页面中抓取数据的三种方法，提取缓存中的数据，使用多个线程和进
程来进行并发抓取，如何抓取动态页面中的内容，与表单进行交互，处理页
面中的验证码问题，以及使用 Scrpay 和Porti来a进行数据抓取，并在最后使
用本书介绍的数据抓取技术对几个真实的网站进行了抓取，旨在帮助读者活
学活用书中介绍的技术。
本书适合有一定Pytho编n程经验，而且对爬虫技术感兴趣的读者阅读。欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
关于作者
RicharLdaw so来n自澳大利亚，毕业于墨尔本大学计算机科学专业。 毕
业后，他创办了一家专注于 网络爬虫的公司， 为超过 50 个国家的业务提供远
程工作。他精通于世界语，可以使用汉语和韩语对话， 并且积极投身于开源
软件。他目前在牛津大学攻读研究生学位， 并利用业余时间研发自主无人机。
我要感谢 TiomthyBawlid教n授将我引入这个令人兴奋的领域， 以及
本书编写时在巴黎招待我的ηiara可Douc。欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
关于审稿人
MartBiunr 咄是一名常驻纽约的数据 记者，其工作是为华尔街日报绘 制
交互式图表。 他在新墨西哥州 立大学获得了新闻学和信息系统专业的学士学
位，然后在纽约城市大学新闻学研究院获得了新闻学专业硕士学位。
我要感谢我的妻子 Lisa励鼓我协助本书的 创作，我的叔叔Michael
耐心解答 我的编程问题 ，以及我的父亲 Richar发d了激我对新闻学和写
作的热爱。
WillSiaanmk 是e一y位数据 专业人士，也是一位业余开 发人员，生活在马
里兰州科利奇帕克市。 他于201 年2 毕 业于约翰·霍普金斯 大学，获得了公共
政策硕士学位， 专业方向为定量分析。他目前在LM&政策研究 有限责任公司
担任 健康服 务研究员，从事与美国医疗保 险和医疗补助服 务中心（CMS） 相
关的项目。这些项目包括责任医疗机 构评估以及精神病院住院患 者预付费系
统监 测。
我要感谢我深爱的妻子Juli和a顽皮的小猫 Ruby，给予我全部的爱和
支持。欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
关于审稿人
AyushT iwa是r一i名Python开发者，本科就读于印度 理工学院罗克 分校。
他自2013 年 起工 作于印度理工学院罗克 分校信息管理小组，并活跃于网 络开
发领域。对他而言 ， 审阅本书是一个非常棒的经 历。 他不仅是一名审稿人，
也是一名狂热的网 络爬虫学习者。 他向所有Python爱好者推荐本书，以便享
受爬虫的益处。
他热衷于Python网络爬虫，曾参与 体育直播订阅、 通用P川lOil电子商务
网 络爬虫（在Miarnj等）相关项目。
他还使用 Djanog应用开发了就业门户，帮助改善印度理工 学院罗克分校
的就业流程。
除了 后端开发之外， 他还喜欢使用诸如NumPy、ScPiy等Python库进行
科学计算和数据分析，目前他从事计算流体力学领域的研究。你可以在GiHtub
上访 问到他的项目， 他的用户名是 tiwariayush。
他喜欢徒步穿越喜马拉雅山谷，每年 会参加多次徒步行走活动。此外，他
还喜欢弹吉他。他的成就还包括参加国际知名的Supe3r0小组，并在其 中成
为排名保持者。 他在高中时，还参加了国际奥林匹克数学竞赛。
我的家庭成员（我的姐姐Aditi我、的父母以及Anand先生）我、在
V和I IMG的朋友以及我的教授都为我提供了很大的帮助。 我要感谢他们
所有人对我的 支持。
最后，感谢尊敬的作 者和Packt出版社团队出版了这些非常好的技术
书籍。我要对他们在编写 这些书籍时的所有辛苦工作表示赞赏。
2欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
..a.&.....1』．
刷昌
互联网包含 了迄今为止最有用的数据 集，并且大部分可以免费公开访 问。
但 是，这些数据难以复用。 它们被嵌入在网站的结构和样式当中， 需要抽取
出来才能使用。 从网页中抽取数据的过程又被称为网 络爬虫。 随着越来越 多
的信息被发布到网 络上，网 络爬虫也变得越来越有用。
本书内容
第1 章， 网 络爬虫简介，介绍了网 络爬虫，并讲解了爬取网站的方法。
第2 章， 数据抓取，展示了如何从网页中抽取数据。
第3 章， 下载缓存， 学习了如何通过缓存结果 避免重复下载的问题。
第4 章， 并发下载，通过并行下载加速数据抓取。
第5章， 动态内容，展示了如何从 动态网站中抽取数据。
第6 章， 表单交互，展示了如何与表单进行交互，从而访 问你需要的数据。
第7章， 验证码处理，阐述了如 何访 问被验证码图像保 护的数据。
第8 章， Scray，p学习了如何使用流行的高 级框架 Scrpay。
第9章 ，总结，对我们介绍的这些网络爬虫技术进行总结。欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
前言
阅读本书的前提
本书中所有的代码都己经在 Python2.7环境中 进行过测试，并且可以从
http://btibucket.rog/wspw/cod下e载到这些源代码。理想情况下，
本书未来的版本会将示例代码移植到Python3 当中。 不过，现在依赖的很多
库（比如 Scrpa/yTiwstedM、ecahinez和Ghots）还只支持Pytho2n。 为了帮助
阐明爬取示例，我们创建 了一 个示例网站，其网 址为 http://xeample.
websacpring.com。由于该网站限制了下载内容的速度，因此 如果你希望
自行搭建示例网站，可以从h ttp://bitbucket.org/swwp/places获取
网站源代码和安装说明。
我们决定为本书中使用的大部分示例搭建一个定制网站，而不是抓取活跃
网站，这样我们就对环境拥有了完全控制。这种方式为我们提供了稳定性，
因为活跃网站要比书中的 定制网站更新更加频繁，并且当你 尝试运行爬虫示
例时，代码可能已经无法工作。另外，定制网站允许我们自定义示例，用于
阐释特 定技巧并 避免其他干扰。 最后，活跃网站可能并不欢迎我们使用它作
为学习网 络爬虫的对象，并且可能会尝试封禁我们的爬虫。使用我们自己定
制的网站可以规避这些风险，不过在这些例 子中学到的技巧确 实也可以应用
到这些活跃网站当中。
本书读者
阅读本书需要有一定的编程经验，并且不适用于绝对的初学者。在实践中，
我们将会首先实现我们自己的网 络爬虫技术版本，然后才会介绍现有的流行
模块，这样可以让你更好地理解这些技术是如 何工作的。本书中的 这些示例
将假设你已经拥有Python语言以及 使用pip安装模块的能力。如果你想复习
一下 这些知识，有一本非常好的免 费在线书籍可 以使用，其作 者为 Mark
2欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
前言
Pilgirm，书籍网址是http://wwdwiv.eintopythonn.et。这本书也是我
初学Python时所使用的资源。
此外，这些例子还假设你己经了解网页是如何使用HTML 进行构建并通
过JavaSrictp更新的知识。关于HTTP、css、 AJAX、WebKi以t及M onogDB
的既有知识也很有用，不过它们不是必需的，这些 技术会在需要使用时进行
介绍。上述很多主题的详细参考资料可以从http://wwww.3schlso.ocom
获取到。
3欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
目录
第1章 网 络爬虫简介
1.1 网络爬虫 何时有用 .......................
1.2 网络 爬虫是否合法 ……………………………………………………………………·2
1.3背 景调研……………………………………………………………………………·…·…3
1.3.1 检查 robts.oxtt…..........….....................3. ......….............................
1.3.2 检查网站地图..........….............................4. .......…........................
1.3.3 估算网站大小..........…..…..….…………….….…………………………5…
1.3.4 识别网站所用技术 …………………………………………………………·7
1.3.5 寻找网站所有者…....·.·….….……………………………………………·7·
1.4编 写第一个网络 爬虫…..........................·..·..·..·.·.·8·.··.·.·.·.·.·.·.·…·.........…
1.4.1 下载网页….......…...................…........... 9.. .....................................
1.4.2 网站地图爬虫….......................….......1.2. ............…······················
14..3 ID遍历 爬虫····················································13· ························
1.4.4 链接爬虫………………………………………………………………………1·5·
本章小结…·…·……………………………………………………………………………n
1 5
.
2 23
第 章 数 据抓取
2.1 分析网页……...........…...........................·.2.3..................….....................…
2.2 三种网页抓取 方法 ...............................·.2.6................................….......…
2.2.1 正则表达式……………………………………………………………………·26欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
目录
2.2.2 BeatuilfuS oup·· ····…··..·..............·.…·.…·.·..2·8.· .·.·.·.·.·.·..·.·.·.·.......
2.2.3 Lxml·………………………………………………………………······3··0·· ·······
2.2.4 性 能对比.......….......…...............…..........…...…...·...·...·..3.2·...·..····
2.2.5 结论.........……............….··.·.3·.5·.·..·.·..........................................…
2.2.6 为链接爬虫添加抓取回调….........................................3.5.... ......
2.3本 章小结…....…....…..….….….….……………………………………………………38
第3 39
章 下 载缓存
31. 为链接爬虫添加缓存支持…· ······…····.…·.·.·.·.·.·..·.·.·.3·9.· ........................
32. 磁盘缓存............................................4..2... ..............................................
3.2.1 实现.........……………………………………………………·……4…4…………
3.2.2 缓存测试..............………………………………46……………………………
3.2.3 节省磁盘空 间……............................….…..·..·..·.46.·..·..·..·..·…...…
3.2.4 清 理过期数据…........................47.. ..............................................
3.2.5 缺点…………………………………………………..….........….......….·4.8....
3.3数 据库缓存..............................”.............................................................
3.3.1 N oSQL是什么....….....…...................….…......…..·..·5..·0..·..·.·......
3.3.2 安装M ongoDB…...................·..··..···..···..·..·.5.·…0.·….·..·..·..·.·…··
3.3.3 M ongoDB概 述 .......…....….......................5..0.....…....…...............
3.3.4 MongoDB缓存实现.....................……..........5.2...........…............
3.3.5 压缩................….............................................................”...........
3.3.6 缓存测试…·”….................·.·.·.5·…4·.·.·.·.·.·.·....…........................…
34. 本章小结…........….……….….….….….….….….….….….…….…….…….….…妇
4 57
第 章 并 发下载
41. 100万 个网页.......................….....…..........…..........5..7... ..........................
42. 串行爬虫..................................….........60…................…...................….....
4.3多 线程爬虫.............................….…................·..·..6..0..............…..….........
2欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
目录
4.3.1 线程和进程如何工作...............................................................“
4.3.2 实现.........................….....................…6...1.................................…
4 .3.3 多进程爬虫…......................6.3. ....................................................
性能 ….......…...................….................….............…....….............67.... ........
4.4
4.5本 章小结…··..….…..........….....................……......................6.8.. ................
第5 章 动 态内容 69
51. 动态网页示例..............….…...................6. 9.. ............................................
52. 对动态网页进行逆向工程.....….·..…....…........................7.2.….…............
5.3渲 染动态网页..........…..................….......................7...7... ........................
yQt还是PySdie……………………………………………………………78
5.3.1P
5.3.2 执行 JavaSrcpit······…·..·.·….·….….…….………………………………7.g.
使用WebKi与t网站交互..….............….......................…..8.0......
5.3.3
5.3.4 Seliuemn ........................85. ..........................................................
5.4 本章小结..….......…..….….….….…….….………………………………..gg. ............
89
第6章 表 单交E
6.1 登录表单 …....…......................................…....9..0.. ....................................
6.2 支持内容更新的 登录 脚本扩展 ….................…......................…... 9..7.. ....
6.3 使 用M ehcaniez模块实现自 动化表单处理....….......….............10..0.. ....
6.4本 章小结 …………………………………………………………………10…2…………·
第7章 验 证码处理 103
7.1 注册账号 …··…………………………………………………………1…0…3… …………·
7.2 光学字符识别 …………………………………………………………………………·106
7.3 处理复杂验证码 …...…......….................….................…........ 1.. 1.. 1.. .........
7.3.1 使用验证码处理服 务.........….............…...........1...21... ................
7.3.2 9kw 入门………………………………………………………………………112
3欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
目录
7.3.3 与注册功能集成…....….….·.·.·.·.·.·.·.·.····1·19· ································
本章小结...........….…..·..·.….….….….….……………………………12…0…………
7.4
第 8章 Scrayp 121
8.1 安装...........................…...............................…..…...................1..2.1.… .·.·..
8.2 启动项目 .............…....................................….1·.22·. ·.·.·.·.·.·.·.·............…...
8.2.1 定义模型....….….….….….…………………………………………………123
8.2.2 创建爬 虫...….….…….….….…………………………………………1·24· ·····
8.2.3 使用shell命令抓取….....…….….….….…….….……………………1·28
8.2.4 检查结果....…..........…..….….….….….……………………1…29…………
8.2.5 中断与恢 复爬虫”…..................….·.·…·…·1.3·2.· .·.·.·.·.·.·.··············
8.3 使用 Poriat编写可视化爬虫 .................….·.….·.·.·.··.·.··.·.···.···.·1··3·3··· ····
8.3.1 安装…..........................…·..·..·..·..·.·.·.·.·1.3·3.· .·.·.·…·······················
8.3.2 标注………………………………………………………………1…36…………··
8.3.3 优化爬虫…··…………………………………………………………………1·38
8.3.4 检查结果…...................….….….……………………………1…40… ……··
8.4使 用 Scprael实y现自动化抓取.....................….....................…..1.4.1.....
8.5 本章小结…..........…...................….......…...·..·.·.·.1·…42·. ·.·.·.·.·.·.·.·............
第9章 总结 143
07咽且 A鸣k搜索23擎 4·EAAιT句3
U 业…
叫
07咱，“ 吭h U句M m M网站 千· 唱’EAA丛T00
J
吭U ……
AP 唱BEAA件OO
U
马
07咱3 宝
章H －－EA，、dAU
本
…
－－EAF飞d
07AaT
唱－EAp气d’I
结
ZJ ，hu 唱·呵，
，、d
07 ，－ ·A句3，
町
4欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章
网络爬虫简介
本章中， 我们将会介绍如下主题：
· 网 络爬虫领域简介：
· 解释合法性质疑：
· 对目标网站 进行背景调 研1
· 逐步完善一个高级网络爬虫。
11. 网络爬虫何时有用
假 设我有一个鞋店， 并且想要及时了解竞争对手的价格。 我可以每天
访问他们的网站 ，与 我店铺中鞋 子的价格 进行对比。但 是，如果我店铺中
的鞋类品 种繁多，或 是希望能 够更加频繁地查看价格变化 的话，就需要花
费 大量的时间，甚至难 以实现。再举一个例 子，我看中了一双鞋， 想等它
促销时再 购买。我可能需要每天访 问这家鞋店的 网站来查看这双鞋是否降
价， 也许需 要等待几个月的 时间，我才能如愿盼 到这双鞋促销。 上述 这
两个重复性的手工流 程，都可以利用本书介 绍的网 络爬虫技术实 现自动化
处理。欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
理想状态下，网 络爬虫并不是必须品，每个网站都应该提供API，以结构
化的格式共享它们的数据。然而现实情况中，虽然一些网站 已经提供了这种
API，但是它们通常会限制可以抓取的数据，以及访 问这些数据的频率。另外，
对于网站的开发者而言 ， 维护前端界面比维护后端API接口优先 级更高。总
之，我们不能仅仅 依赖于API去访 问我们所需的在线数据，而是应该学习一
些网络爬虫技术的相关知识。
12. 网络爬虫是否合法
网 络爬虫目前还处于早期的蛮荒阶段，“允许哪些行为”这种基本秩序 还
处于建设之中。从目前的实践来看，如果抓取数据的行为用于个人使用，则
不存在问题：而如 果数据用于转载，那么抓取的数据类型就非常关键了。
世界各地法院的一 些案件可以帮助 我们确定哪些网 络爬虫行为是允许
的。在FeiPsutblicaItn起ic诉o.Rnusr,a Tlel写phSoenrevCioc的.e案 件中，美
国联邦最高法院裁定抓取并转载真实数据（比如，电话清 单〉是允许的。而
在澳大利亚，TelsCtorraporLaitmiidot起ne诉 PhoDnierectCoormipeaPsnty y
Ltd 这一类 似案件中，则裁定只有拥有明确作者的数据，才可以获得版权。
此外，在欧盟的ofir.d起k诉 home一.案d中k， 最终裁定定期抓取和深度链接
是允许的。
这些案件告诉我们，当抓取的 数据是现实生活中的真实数据（比如，营业
地址、电话清 单）时，是允许转载的。但 是，如果是原创数据 （比如，意见
和评论），通常就会受 到版权限制，而不能转载。
无论如何，当你抓取某个网站的数据时，请记住自己是该网站的访 客，应
当约束 自己的抓取行为，否则他们可能会封禁你的 IP，甚至采取 更进一步的
法律行动。这就要求下载请求的速度 需要限定在 一个合理值之内，并且还需
要设定一个专属的用户代 理来标识自己。在下面的小节中我们将会对这些实
践进行具体介绍。
2欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
13.
背景调研
关于上述几个法律案件的更多信息可以参考下述地址：
http://caslep.lafwid.nlaw.com/scripts/
•
· getcasep.l ?court=US&vol=499&invol=340
£
http:/w/.wawustlidiu..eau/acua/sest/hc/
FCA/2010/44.html
http://www.bvhd.dk/muopclaoratdsi/ctlxe s
•
/So gH adnelserttenasf gr elsie O fira-gsen.pdf
13. 背景调研
在深入讨论爬取一个网站之前，我们首先需要对目标站点的规模和结构进
行一 定程度的了解。网站自身的 robost.txt和Sitempa文件 都可以为我
们提供一定的帮助，此外还有一些能提供更详细信息的外部工 具，比如Googel
搜索和WHOIS。
1.3.1检 查robo.txstt
大多数网站都会定义robtost.xt文件，这样可以让爬虫了解爬取该网站
时存在哪些限制。这些限制虽然仅仅 作为建议给出，但是良好的网 络公民都应
当遵守这些限制。在爬取之前，检查robost.txt文 件这一宝贵资源可以最小
化爬虫被封禁的可能，而且还能发现和网站结构相关的线索。关于robost.txt
协议的更多信息可以参见 http://wwwr.obosttxt.rog。下面的代码是我
们的示例文件 robost.txt中的 内容，可以访 问 http://example.
webcsrpaing.com/robots.txt获取。
＃sect－on叮4
－
U D·工s er －4－ 1lea oq e ··n卡M ，／·· B a d户U r a w－ － e r
sa w
3欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
# sectio2n
Use-ragen:t *
Crwal-edla:y 5
Dislaowl:/ trap
# setcio3n
Sitemap: htpt://exapmlew.esbcarpin.cgoms/itemap.mxl
在section1中，robotst.xt文 件禁 止用户代理为BadCrawler的
爬虫爬取该网站，不过这种写法可能无法起到应有的作用，因为恶意爬虫根
本不会遵从 robotst.xt的要 求。本章 后面的一个 例子 将会展 示如何让爬虫
自动遵守robotst.xt的要 求。
section2 规定， 无论使用哪种用户代理，都应该在两次下载请求之
间给出5秒 的 抓取延迟，我们需要 遵从该建议以避免服 务器过载。这里还有
一个／trpa链接，用于封禁 那些爬取了不允许链接的恶意爬虫。如果你访 问
了这个链接，服 务器就会封禁你 的 IP一分钟！一个真实的网站 可能会对你
的 IP封禁 更长时间，甚至是 永久封禁。不过如果这样设置的话， 我们就无
法继续这个例子了。
section3 定义了一个Sitemap文 件，我们将在下一节中了解如何检
查该文 件。
1.3.2检 查网 站地图
网站提供的Sitemap文 件（即网站地图）可以帮助爬虫定位网站最新的
内容 ，而 无须 爬取每 一个 网页。 如 果 想要 了解更 多 信息 ， 可以从
http/:/wwswit.emapso.rg/prtoocol.html 获取网站地图标准 的定
义。下面是 在robotst.xt文 件中发现的Sitemap文 件的内容。
<?xmlv ersio＝n”.1。”encodg＝i”UnTF-8？”〉
<urlsextml ns”＝thtp://www.istmeaps.org/hseacms/istmeap/.0”9〉
<urlo>c<>lhpt:t//xeapml.ewesbcrpaing.com/viAefwg/nhiatsa-n1
</lco>/<url>
<url><loc:>//hextaptmlp.ewebscprian.cgom/v/iAelwanIds-lnad-s2
4欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
13.
背景调研
</olc>/<url>
<url><>lhtot:cp//exmapl.weebscprian.cgom/evwiA/lbnai-a3<l/o>c
<furl>
</urlset>
网站 地图提供了所有网页的链接，我们会在后面的小节中使用这些信息，
用于创建我们的第一个爬虫。虽然Sitema p文件提供了一种爬取网站的有效
方式，但是我 们仍需对其谨慎处理，因为该文 件经常存在缺失、过期或 不完
整的问题。
1.3.3估 算网站大小
目标网站的大小会影响我们如何进行爬取。如果是像我 们的示例站点这样
只有几百个URL 的网站，效率并没有那么重要：但如果是拥有 数百万个网页
的站点，使用串行下载可能需要持续数月才能完成，这时就需要使用第 4 章
中介绍的分布式下载来解决了。
估算网站大小的一个简便方法是检查Googel爬虫的结果，因为G oogel很
可能已经爬取过我们感兴趣的 网站。我们可以通过Google搜索的site 关键
词过滤域名结果，从而获取该信息。我们可以从 htt:p//wwwgo.ogel.
com/vaad口cedsearc了h解到该接口及其他高级搜索参数的用法。
图 1.1所示为使用site 关键词对我们的示例网站进行搜索的结果，即在
Googel中搜索site:example.webcsrapign.com o
从图 1.1中可以看出，此时Googel估算该网站 拥有202个网页，这和实
际情况差不多。不过对于更大型的网站，我们会发现Googel的估算并 不十
分准确。
在域名后面添加URL 路径 ，可以对结果进行过滤，仅显示网站的某些部
分。图 1.2所示为搜索site:examplew.ebscrpaing.com/viwe的结果。
该搜索条件会限制Googel只搜索国家页面。
5欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
Aboul202re田JltS伺45蕃emnds)
•
�
AF Exampwleeb s cranpgw ebsite
· · ·
辄酬阳.we民町，商ping.oomlcor世in回I/AF•
Exam阱嗣b阳叩ing Angela
＼￥盹脚.Arri 目，闻geria seninS otswa·刷n刷an a
R邱刷lc·Ch副．
Fa回·6田undl C副陌roon ca阳Verd·eC田11Arra1ri国n
NA－εxa『nplweeb scraP.wienbges 挂
ex翻F瑞e
An窜山l国 Anti凯iaar晴B酣bA阳ubad a
E翼田胃piweeb缸万冒pir咱w雹』画捶.IJ。曲Arr咀e拖a
Sahaπ、a&· Sa『1胁ad。S•B毫撼IZI>”Bl>伺11Ud握’哥。nal「·a, and.
SainEtu s恒屈JS
NE-E姐mpl�eesbc rawpeibnsgi te
e阻mpl且W创JSCI'胃病’g.oomllso/捋E•
Nalklnal Fl咽’M回：1,267,问00pul0aS如n嗯且:惜1据阳0阳,e6lli剧l7，s6o,:27专
NE.
CountryI:J 胁C，a.i就Nl醋a’m町C曲睛酣吐AF. J班Curr田，cy Code:X OF.
Tlcl:
-
NG Exampwleeb s αaping website
e刷脚.wet刷刷ng.comlisol闸，
NationFall啕 岛国：： 923,7s68qua阳闹。mPcψeutrle硝sor应.154,00口，000.1聪：NG.
C咀Jntry: N精制a巳apl国EAlli!由a con剧团提：AF.Tld:c u.rrencnyg .C时居 ：NGN.
图 1.1
(0.52 seam峭
About 117明ults
we部braping
Example website
就ami归”W确scraping.α：m1/view/Guemse·沪倪，
Natio捕’F陆g:A，回：76sqkull町oem钝国. Popula 6t 5i ,o 22n 苗: ，i GG四.：Cou晴y.
G佳emseC于a“pital: Currency
St Peter p。她Con伽ent EU.Tld : .gg. Code:G BP.
pig
Exampwleebs carn website
回am树e.w唾民臼撞倒ng.comfv梅w/Je陀曹y-113 ...
Nat阳nFa句l：阳明：116呵U脚扭llornet阳.P句“la切罚；阂，612l.s Jo E: .C ountry: Jerse沪
CapiSatianHell:i田 .Conti阴E阳Ut.T陆：C.urjer.ency
CodeG:B P.
-
Examp�e lebs crawpeibnsgi te
PK
e泪m阱.webscra酬g.comlv恒w/P副stan-1邸，
Fl句：A陌a:8部，S铅squa用kffomPeo悦psu.lation:
National 184,404,791.国：PK.
C由mtry:Pak陆；ta1n时.aCap幅m：a缸ad.Cont加剧1l:AS“lld:
.pk Currency Code ...
-
Exampwleebs crQa p ebi sn iW te eb Scraping.com
w
example.w盼scra阪ng....com/ view/Ma阳归卧134
Flag; squa阳kllometJ髓，Popi!翩。n:
Na悔自at Area: 329,750 28,27 4,I 盹7：2MY9精“
C皿miry: Ma姐ysia.Ca回国：KualL四npaur. Con11nentA S. Tld:C .町 mre yn . 町cy
图 1.2
这种附加的过滤条件非常有用，因为在理想情况下，你只希望爬取网站中
包含有 用数据的部分，而 不是爬取网站的每个页面。
6欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
13.
背景调研
13..4识 别网 站所用技术
构建网站所使用的技术类型也会对我们如何爬取产生影响。有一个十分有
一－
用的工具可以检查网站构建的技术类型 buitlwith模块。该模块的安装
方法如下。
pip installb uilttwhi
该模块将URL 作为参数，下载该URL并对其进行分析，然后返回该网站
使用的技术。下面是使用该模块的一个例子。
》＞ imp。rtbuilttwhi
》＞ builtwi.tpahrs（eh’ttp://example.ewbscrapin.g。cm’｝ I
{u’ajva scriptf-ramew，。rks’ ：［u’jQl且ery’Iu，’M 。derznri’，u’jQl且eryUI’］
u’pr。gamrmingl-anguasge’： ［’uPyth。’n］
u’web-framew。rks’ ：［u’Web2yp’，u’TwitterB。。ttsra’p］ ，
u’ewb-servers’ ：［u’gNin’x］ ｝
从上面的返回结果中可以看出，示例网站 使用了Python的Web2py框架，
另外还使用了 一些通用的JavaSciprt库，因此 该网站的内容很有可能是嵌入在
HTML中的，相对而言比 较容易抓取。而如果改用 AngulrJaS构建该网站，此
时的网站内容就很可能是动态加载的。另外，如果网站使用了 ASP.NET，那
么在爬取网页时，就必须要用到会话管理和表 单提交了 。对于这些更加复杂
的情况，我们会在第5章和第 6章中进行介绍。
13..5寻 找网站所有者
对于一些网站，我们可能会关心其所有者是谁。比如，我们已知网站的所
有者会封禁网 络爬虫，那么我们最好把下载速度控制得更加保 守一些。为了
找到网站的所有者，我们可以使用WHOIS协议查询域名的注册者是谁。Python
中有一个针对 该协议的 封装库，其文 档地址为 httsp://pypi.pytohn.
org/pypi/pyhton-whosi，我们可以通过 pip进行安装。
7欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第l章 网络爬虫简介
pipi nstallp yt。hn-hw。is
下面是使用该模块对 appspo.tcom这个域名进行WHOIS查询时的返 回
结果。
》＞ imp。rtwh。is
》＞ printwhois.wh。i（sa’pps。pt.ocm’｝
、四.e_servers": [
”NSl.。G。GL.EOCM”，
”NS2.。G。GL.EOCM”，
”NS3.G。。GLE.COM”，
”NS4.。。GGLE.C。M”，
”ns4.q。。ql.eocm”，
”ns2.q。。ql.eocm”，
”nsl.q。。ql.eocm”，
”ns3.q。。ql.ce。m”
］ ，
”。rq：””G。。qlIenc.”，
”e啤ai”l：s［
”abusecmoplaintmsa@rkm。nit。.crom”，
”dns-ad皿in@q。。g.locem”
从结果中可以看出该域名归属于 Googe，l实际上也确实如此 。该域名是
用于GoogAelppE ngine服务的。当我们爬取该域名时就需要十分小心，因为
Googel经常会阻断网络爬虫，尽管实际上其 自身就是一个网络爬虫业务。
14. 编写第一个 网络爬虫
为了抓取网站，我们首先需要下载包含 有感兴趣 数据的网页，该过程一般
被称为爬取 （crawl）。i爬n取g一个网站 有很多种方法，而选用哪种方法更加
合适 ，则取决于目标网站的结构。本章 中，首先会探讨如何安全地下载网页，
然后会介绍如下3种爬取网站的常见方法：
8欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
14. 编写第一个网络爬虫
· 爬取网站 地图1
· 遍历每个网页的数据库ID;
· 跟踪网页链接。
14.1. 下载网页
要想爬取网页，我们首先需要将其下载下来 。下面的示例脚本使用Python
的urllbi2模块下载URL。
imporutr lbl2i
def dowlnoad(rul) :
retuurrn lbl2.irulp。e(nrul) r.e a(d)
当传入URL 参数时，该函数 将会下载网页并返回其HTML。不过，这个
代码 片段存 在一个问题 ，即当下载网页时，我们可能会遇到一些无法控制的
错误 ，比如请求的页面可能不存 在。此时，urllib2会抛出异常，然后退出
脚本。安全起见，下面再给出一个更健壮的版本，可以捕获这些异常。
imporutr llib2
def donwloa(drul):
prin’tD。nwl。dain：g’ ，url
try:
htm=l urllib2.u rlpoe(n ur)lr.e a(d)
exceuptr lbl2.iRULErrora se :
prin’toDwnl。aderr。’r，：er.eas。n
htm=l None
retuhrtnm l
现在，当出现下载错误 时，该函数 能够捕获到异常，然后返回None。
1.重试下载
下载时 遇到的错误 经 常是临时性的，比如服务器过载时返回的 503
ServiecU navailable错误 。对于此类错误 ，我们可以尝试重新下载，因
为这个服务器问题现 在可能己解决。不过，我们不需要对所有错误 都尝试重
9欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
新下载。如果服务器返回的是404Not Found这种错误 ，则说明该网页目
前并不存在，再次尝试 同样的请求一般也不会出现不同的结果。
互联网工程任 务组（InternetEngienenrgi Tska oFre）c定义了Hπ？ 错误 的
完整列表 ，详 情可参考 httsp://tools.ietf.org/html/frc7231#
sectio-n6。从该文档中 ，我们可以了解到 4xx错误 发生在请求存 在问题时，
而 5xx错误 则发生在服务端存在 问题时。所以，我们只需要确保download
函数 在发生 Sxx错误 时重试下载即可。下面是支持重试下载功能的新版本
代码。
def donwlaod(rul, numr etrie)s:= 2
prin’tD。nwloadgin：’ ，url
tr:y
htm=l urlilb.2urlpoe(nrul). era(d)
exceuptr lbl2.iRULrEroars e :
prin’toDwnlaode rrro：’ ，e.reason
html= None
ifn umr etires> 0:
ifh asat(tre，’ocd’e ）a nd5 00 <=e c.od<e 600:
# recuresliyrv etrSyx xH TTePr rors
retudronnw loda(rul, numr eters-i1)
reutrnh tml
现在，当downlo函a数d遇到Sxx错误 码时，将会递归调用函数 自身进
行重试。此外，该函数 还增加了一个参数，用于设定重试下载的 次数，其默认
值为两次。我们在这里限制网页下载的 尝试次数，是因为服务器错误 可能 暂时
还没有解决。想要测试该函数 ，可以尝试下载htt:p//httpstat.us/500,
该网址会始终返回500错误 码。
》＞ d。wnl。（ahd’tpt://httpstat.us/50’0｝
Downl。adi:nhgtpt://htptsatt.us/500
D。wnloaedrr。:rIntenralS evrerE rr。r
D。wnl。ad:inhgtpt://htptsatt.us/500
Downloaedr r。:rInetrnalS evrerE rr。z
D。wnl。ad:ihngtpt://htptsatt.us/500
D。wnloaedrr。:rInetrnalS evrerE rr。r
10欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
14. 编写第一个网络爬虫
从上面的返回结果可以看出，dowlnoad函 数的行为和预期 一致，先尝
试下载网页，在接收到500错误 后，又进行了两 次重试才放弃。
2.设置用户代理
默认情况下，urllbi2使用 Python-urllib2/.7作为用户代理下载
网页内容，其中 2.7是Python的版本号。如果能使用 可辨识的用户代 理则
更好，这样可以避免我们的网 络爬虫碰到一些问题。此外，也许是因为曾经
历过质量不佳的Python网络爬虫造成的服务器过载，一些网站还会封禁这个
默认 的用户代 理。比如， 在使用 P同lO默il认用户代 理的情况下 ， 访问
htt:p//ww.wmeetup. com／，目前会返 回如图 1.3所示的访 问拒绝提示。
Accesdse nied
η1e owneorf t hwiesb s(iwwtwe. meetup.comb)a nhnaeysdo ur baseodn your
access
browsseigr'nsat( 1u 7r5e4 13467，仿Rlae4-ua48).
•
•Ra yI D1:7 54l34676eft>ae4
•Ti m臼饱mpM:on.06心ct-1418:55:G4M8T
•Y o咀IPra dresds:8 3.27.128.162
•Re queUs撞ReLdw:ww .mee灿p.com/
•E.π·or reference number: I 0 IO
•Serve r ID: FL 33F7
User-Agent：时也on-urllib/2.7
图1.3
因此 ，为了下载更加可靠，我们需要控制用户代理的设定。下面的代码对
downlo函a数d进行了 修改，设定了一个默认的用户代理 “wswp”（即Web
ScrapwiintPghy tohn的首字母缩写）。
def d。nwloa(drul,usearg en’tsw＝wp’，numr etrie) s=: 2
prin’tDonwloadgin：’ ，url
heardse＝ ｛U’serg-ean’t：usearg e}n t
reuqest= urlilb.2Reques(tur, lheadres=heeard)s
try:
•
htm=l urllbi2.u rlpoe(ne rquestr)e a(d)
exceuptrl lbi2.URLrEroars e :
prin’toDwnloade rrro：’ ，er.eans o
htm=l None
11欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第l章 网络爬虫简介
ifn umr etri>e 0s:
ifh asat(ter，’ocd’e） a nd5 00 <=e c.od<e 600:
# retr5yXX HTTePr rors
retudronnw l。a(drul,usearg e,n ntumr etersi1-)
retuhrtnm l
现在，我们拥有了一个灵活的下载函数， 可以在后续示例中得到复用。该
函数 能够捕获异常、重试下载并设置用户代理。
14..2网 站地图爬虫
在第 一个简单的爬虫中，我们将使用示例网站 robost.txt文件中发现
的网站地图来下载所有 网页。为了解析网站地图，我们将会使用一个简单的
正则表达式，从＜loc＞标签中提取出URL 。而 在下一章中，我们将会介绍一
一－
种更加健壮的解析方法 cs选s择器 。下面是该示例爬虫的代码。
def crawls itemap(rul) :
# donwl =oa tdh es itemapf ile
sitemap donwla。d(rul)
# ext =r atchtes itmeapl inks
links re.f inadl（l＜ ’loc(.*> ?<)/l oc’＞，sitema)p
# donwlaode aclhi nk
forl inikn l in:k s
=
html donwloa(dilnk)
# scrpaeh tmhle re
＃
现在，运行网站地图爬虫，从示例网站中下载所有国家页面。
》＞ craw_lsitema（ph’ttp://example.webscrapin.gocm/sitema.pxml’｝
D。wnload:inhgtpt://example.webscrapin.gocm/si阻t碍 .xml
D。，wnloadin:ghtpt://e xample. wecbrspa ing.c 。•m/view/Afgnhiasatn-1
D。wnl。ad:inhgtpt://xeample.ewbscrapin.gcomv/iew/Alda-nIslnads-2
D。wnload:inhgtpt://example.ewbscrapin.gcom/vie/wAlbaina-3
可以看出，上述运行结果和我们的预期 一致，不过正如前文所述，我们无
法依靠Sitemap文件提供每个网页的链接。下一节中，我们将会介绍另－个
简单的爬虫，该爬虫不再依赖于Sitemap文件。
12欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
l4. 编写第一个网络爬虫
14..3I D遍历爬虫
本节中，我们将利用网站结构的弱点，更加轻松地访 问所有内容。下面是
一些示例国家的URL 。
• htpt:I eIx mapl.ew esbcraip口.gcom/vi/eAwfhgainsta口－1
• htpt:I eIx mapl.ew ebscpriηag.com/vieuws/tAarli2a
• htpt:I eIx mapl.ew ebscpri口ag.com/vieBwra/zi3l-
可以看出，这些 URL只在结尾处有所区别， 包括国家名（作为页面别名）
和 ID。 在URL 中 包含页面别名是非常普遍 的做法， 可以对搜索引擎优化起到
帮助作用。一般情况下， Web服务器会忽略这个字符串，只使用D 来匹配数
据 库中 的 相 关记 录 。下 面我 们 将 其 移 除 ，加 载 htpt://exampl.e
wesbcrpai呵.com/ivew1/，测试示例网站中的链接是否仍然可用。测试
结果如图 14.所示。
NatioFnlaalg :
Area: 647,s5q0ua0『k eilometres
Population: 29,121.286
Isa: AF
Country: Afghanistan
Capital: K曰bul
Cot「linent: AS
Tld: .af
CuπencCyo de·: AFN
Cu「renNcayme: Afghani
Ph口ne 93
PostCaold eF ormat
PostCaold eR eg.e:x
Languages: fa”-AF,ps,uz-AF.tk
Neighbou「S TMC NI R T J PK UZ
Edrt
图1.4
13欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
从图 1.4中可以看出，网页依然可以加载成功，也就是说该方 法是有用的。
现在，我们就可以忽略页面别名，只遍 历ID来下载所有 国家的页面。下面是
使用了该技巧的代码片段。
imporitt ertools
forp agien i tretool.scou口(t1:)
url＝ ’thtp:/e/xmapel.wsebcrapi.cnogm/wv／i－宅ed’ 屯page
=
html donwloa(dur) l
ifh tmil sN on:e
break
els:e
# succe-scsa 口scrpaether esult
pass
在这段代码中，我们对ID进行遍历，直到出现下载错误 时停止，我们假
设此时已到达最后一个国家的页面。不过，这种实现方式存在一个缺 陷，那
就是某些记录可能已被删除 ， 数据库ID之间并不是连续的。此时，只要访问
到某个间隔点，爬虫就会立即退出。下面是这段代码的改进版本，在该版本
中连续发生多次下载错误 后才会退出程序。
# maixmumn ubmero fc onsueticved onwloaedr roarlsl woed
=
maxe rrors5
# currennutbm ero fc onseuctivdeo nwloaedr rors
=
nume rror0s
forp agie口 itetrooslc.oun(tl:)
url＝ ’thtp://exmpal.eewbscrapi.ncgom/vi宅edw’／屯－paeg
=
html donwloa(dur) l
ifh tmil sN on:e
# recieveadn e rrotrr yintogd onwloadt hisw epbage
nume rro+r=s1
==
ifn ume rrorsm axe rro:r s
# reahcedm aixmunmu bmero f
# consceutievero rrss oe xit
break
els:e
# sucecss- cans crapteh er esult
＃
=
nume rror0s
14欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
14. 编写第一个网络爬虫
上面代码中实现的爬虫需要连续5次下载错误 才会停止遍 历，这样就很大
程度上降低了遇到被删除 记录时过早停止遍历的风险。
在爬取网站时，遍历ID是一个很便捷的方法，但是和网站地图爬虫一样，
这种方法也无法保 证始终可用。比如，一些网站会检查页面别名是否满足预
期，如果不是，则会返回404Not Found错误 。而另一些网站则会使用非
连续大数作为ID，或是不使用数值作为ID，此 时遍历就难以发挥其作用了。
例如，Amaozn使用ISBN作 为图书ID，这种编码包含至 少10位数字。 使用
ID对Amaozn的图书进行遍 历需要测试数十亿 次，因此 这种方法肯定不是抓
取该站内容最高效的方法。
14..4链 接爬 虫
到目前为止，我们已经利用示例网站的结构特点实现了两个简单爬虫，用
于下载所有 的国家页面。只要这两种技术可用，就应当使用其进行爬取，因
为这两种方法最小化了需要下载的网页数量。不过，对于另一些网站，我们
需要让爬虫表现得更像普通用户，跟踪链接，访 问感兴趣的内容。
通过跟踪所有链接的方式，我们可以很容易地下载整个网站的页面。但是，
这种方法会下载大量我们并不需要的网页。例如，我们想要从一个在线论坛
中抓取用户账号详情页，那么此 时我们只需要下载账号页，而 不需要下载讨
论贴的页面。本节中的链接爬虫将使用正则表达式来确定需要下载哪些页面。
下面是这段代码的初始版本。
imporrte
def lin_kcrlawe(rsee_udr,l link_reg)e:x
””C”rwalf rmot hgei vesne eUdR Lf olwlionlgi nmkast chbeyld i nrke gex
craw14q－ueue＝ftseedurl］
－ －
w噜n ’l、4eCraw吁牛 －q－ueue－－
huz m14 ＝ ＝C dr oa ww nl －－ oq企 au deu ue z－ lp ）。 p （ ）
t l
f、
15欢迎加入非盈利Python编程学习交流QQ群783462347，群里免费提供500+本Python书籍！
第1章 网络爬虫简介
# filtfeorr limnatkcsh ionugr r euglaerx psrseion
for liinng ke tl in(khst lm):
ifr em.atch(ilnkr eg,e lxi口:k)
crwal_uqeeu.aeppn(dlink)
def getl ink(sh tm)l :
””Re”tura口lisotf l inkfsrm o html
# a reuglare xprsesiont oe xtarcta lll inkfsr mo the pwaegbe
=
wepbagree gexr e.mcpoil（e＜’a "[>]+href［＝＼”’（］丰．？）［＼”’’］，
reI.G NEOCRASE)
# lisotf a lll ikns ofmrt hew epbage
retuwre口bpargeeg.efxindla(hlt)m l
要运行这 段代码，只需要调用 likn crawler函数，并传入两个参数：
要爬取的网站URL 和用于跟踪链 接的正则表达式。 对于示例网站，我们想要
爬取的是国家列表 索引页和国家页面。其中，索引页链接 格式如下。
• http:I eIxa mple. wcerbapsi ng.c om/i nde/x 1
• http:I eIxa mple. wcerbpasi ng.c om／土d口ex/2
国家页链 接格式如下。
• http:I / example.w ebsracpingc.o mv/iewf/gAhainstan-1
• http:I / expalme.w ebcsra ping.c omv/iewl/aAn-dIsla口ds-2
因此 ，我们可以用／（inde[xvie）w／这个简 单的正则表达式来匹配这两
类网页。当爬虫使用这些输入 参数运行时会发生什么呢？ 你会发现我们得到
了如下的下载错误 。
》＞ likn crwaler（h’ttp://exmaplew.esbcrapnig.co’m，
’(Ii ndIev xi ew’））
Donwlodian:g htpt://exmaplew.ebscprian.gcom
Donwloaidn:g /index/1
Traceba(cmkso tr ececnat llla s:t )
ValueErr:ur noknowunr lt yp:e Iid口ex/1
161.4 编写第一个网络爬虫
可以看出，问题出在下载／index/1时 ，该链接只有网页的路径 部分，
而没有协议和服务器部分，也就是说这是一个相对链接。 由于浏览器知道你
正在浏览哪个网页，所以在浏览器浏览时 ，相对链接是能够正常工作的。但
是，urllbi2 是无法获知上下文 的。 为了让urllib2能够定位网页，我们
需要将链接转换为绝对链接 的形式，以便包含 定位网页的所有细节。如你所
愿，Pyhton中确实有用来实现这一功能的模块，该模块称为urlparse。下
面是linkcralwer的改进版本，使用了urlparse模块来 创建绝对路径。
imporutr plarse
defl ink_crlawe(resedu rll,i nrke egx:)
””Cr”awflr otmh eg ivesne eUdR Lf ollowilnign mkasct hebdyl inrke gex
crawlq企ueUe＝rLSeedurl1』
－ －
whE工 lecraW14 －q品ue Ue －－
u hrl t m＝ = l C r da w o－－ nw－qA lu oe u a(e－ dupO r) P （ l ）
for lin ikn g etl ink(sthml):
ifr e.amt c ( hl nik_reg,e lxin:k )
=
li口kurlrpsa.eruloji(nseeudr ,l link)
crawlq_ueu.epapen(dilnk)
当你运行这段代码时，会发现虽然网页下载没有出现错误，但是同样的地
点总是会被不断下载到。这是因为这些地点相互之 间存在链接。 比如，澳大
利亚链接 到了南极洲，而南极洲也存在到澳大利亚 的链接，此 时爬虫就会在
它们之间 不断循环 下去。 要想避免 重复爬取相同的链接，我们需要记录哪些
链接己经被爬取过。下面是修改后的 linkcrawler函数，己具备存储己发
现URL 的功能， 可以避免重复下载。
defl inkc rwale(resedu rll,i nrke gxe):
=
crawlq ueue [seeudr ]l
# keetpr acwkhi ch URL’hsa vse eebne froe
see口＝setf、czawlqueue）
－
wh－l14ec raw14 q－ueu··
fhu otr rml 14 14＝ E＝ lnc kdz－ oa W工Ew nn14 －－ qJoq4e au tde －u （ 14ue E工Z－p l 口1’咱K0 sp （（）
h←L m 14 ）
e
1 7第l章 网络爬虫简介
# chceki fl inkm atcsh eexpecterde gex
ifr e.mat(clhinkr eg,e lxin:k )
# fomr absoultel ink
link= urplars.uerloji(nse_eudr,l link)
# chceki fh avae lreadys eetnh si link
ifl innko ti 口see:n
see.andd(ilnk)
crwalq ueu.eappe(nlidnk)
当运行该脚本时，它会爬取所有地点， 并且能够如 期停止。最终，我们得
到了一个可用的爬虫！
高级功能
现在，让我们为链接爬虫添加一些功能，使其在爬 取其他网站时更加有用 。
解析 robst.toxt
首先，我们需要解析robtos.txt文 件，以避免下载禁止爬取的URL 。
使用Python自带的robotparse模r块，就可以轻松完成这项工作，如下面
的代码所示。
》＞ imp。rtz。b。ptarser
》＞ rp = r。b。ptarse.rRobt。FilePars(e)r
》＞ rp.se_turl( h'tpt:/ /ex四1ple.webscrapin.cg omr/ob。t.sxtt’）
》＞ rp.erad()
》＞ url＝ ’thtp://example.webscrpaing.ocm’
》＞ use_ragent＝ ’aBdCralwer’
》＞ rp.ca_nfetch(us�二eagen,turl)
False
》＞ use_ragent＝ ’。G。dCrwlaer’
》＞ rp.ca_nfetch(us_eargent, url)
True
roboatrpse模r块首先加载 robo.ttstx文 件，然后通过ca_nfetch ()
函 数确定指 定的用户代 理是否允许访 问网页。在本 例中，当用户代 理设置
为 ’aBdCrwaler’时，roboatrpse模r块会返回结果表明无法获 取网页，这
和示例网站 robotst.xt的定义一样。
1814. 编写第一个网络爬虫
为了将该功能集成到爬虫中，我们需要 在crawl循环 中添加该检查。
whilec rwalq ueu:e
url= craw_lqeuu.ep。(p)
# checku rl speassr obsot.xttr esttriinocs
ifr p.can_ftec(hus_eagren,t ur)l:
els:e
prin’tlB。cekdbyr obtos.xtt：’ ，url
支持代理
有时我们需要使用代理访问某个网站 。比如，Netflix屏蔽 了美国以外的
大多数国家。使用urlilb2支持代理并没有想象 中那么容易（可以尝试使用
更友好 的 PythonHTTP模块 requests来实 现该功能，其文 档地址为
http://dcos.ypthon-requests.rog／）。下面是使用urlilb2支持代
理的代码。
prxoy=
open=e ru rlbl2i. ubil_dopnee(r )
prx。yparmas= {urlpsae.rurlpsae(rur). lcshem:e prxoy}
。pen.earddhanedrl(urlbl2.PirxoyHanedr(lprxy。_parmas) )
repsonse= opnee.rp。e(nreqsute)
下面是集成了该功能的 新版本dow口ola函d 数。
def dowlnoa(drul, use_ragnet’＝wspw’，prxoy=Neo,nn u_mretrsi=e)2:
prin’toD wnloadi：n，’gurl
heardse＝ ｛U’serg-ean’t：u se_arge}n t
reqsute= urlbl2i.Reqsuet(rul, heaedrsh=eaedr)s
opeenr= urllib2.buil一d。epner()
ifp rxoy:
prxoyp armas= {urlaprs.erulaprs(eur). lcshem:e prxoy}
opeenr.addh anedrl(urlbl2.Pirx。yHanedr(lrpoxpyarmsa))
tr:y
htm=l opeenr.。pe(nerquste).r ea(d)
exceputr lbl2i.URLrEroars e :
prin’toDwnla。derrro：’ ，er.eason
19第1章 网络爬虫简介
htm=l None
ifn umr etri>e 0s:
ifh asat(te，r’ocd’e ）a nd5 00 <=e c.od<e 600:
# retrSyXX HTTPe rrors
htm=l dowlnoad(ur,l usearg e,n ptro,x y
numr etr-i1es)
retuhrtnm l
下载F民速
如果我们爬取网站的速度过快，就会面临被封禁或是造成服 务器过载的风
险。为了降低这 些风险， 我们可以在两次下载之间添加延时，从而对爬虫限
速。下面是实现了该功能的类 的代码。
clasTsh rtolt:e
”””Adda delayb etwedeonwl noadst ot hes amed omian
def一＿ini一＿t（eslfd,elay:)
# amounotf d elayb etwedeonnw loadfso r edaocmhia n
sel.fedla=y delay
# timestampo fw hean domianw asl asatc csesed
sel.fodmains= { }
def wait(selfu,r) l:
domian= urlpsae.rrulpares(url). entlc。
las_taccsesed= self.d。amin.gset(daomi)n
ifs el.fedla>y 0 andl asatc csesedi sn 。tNon:e
sleep sec=s s elf.edla-y( dateitm.eadteitm.eno(w)-
lasatc csese.de)sco nds
ifs leeps ec>s 0 :
# domianh asb eeanc csesedr eecnlty
# son eetdo s lepe
time.lseep(lsepe sec)s
# updtaet hel asatc csesedt ime
self.d。amin[ds。mian]= datemte.iadteitm.eno(w)
Throttle类记 录了每个域名上次访 问的时间，如果当前时间距离上 次
访 问时间小于指 定延时，则执行睡眠操 作。我们可以在每次下载之前调 用
Throtlte对爬虫进行限速。
2014. 编写第一个网络爬虫
thr。ltet= Thrtolt(eedlay)
throlte.tawi(tur) l
resu=l dto wlnoa(drul, heaedr,s proxyr=pox,y
numr etrineusmr= etire)s
避免爬虫陷阱
目前，我们的爬虫会跟踪所有之前没有访问过的链接。但是，一些网站会
动态生成页面内容，这样就会出现无限多的网页。比如，网站有一个在线日
历功能，提供了可以访问下个月和下一年的链接，那么 下个月的页面中同样
会包含访 问再下个月的链接，这样页面就会无止境地链接下去。这种情况被
称为 爬虫 陷阱。
想要避免 陷入爬虫陷阱，一个简单的方 法是记录到达当前网页经过了多少
个链接，也就是深度。当到达最大深度时，爬虫就 不再向队列中添加该网页
中的链接了。要实现这一功能，我们需要修改 see n变量。该变量原先只记
录访问过的网页链接，现在 修改为一 个字典，增加了页面深度的记录。
def linckr awl(.e .r, .ma xd epth)=:2
maxd ept=h 2
sene={ }
depth＝see口rLurl1』
if d e p rt h －l－－ n＝ m l－a inx n一ld －－e np t ts、n i．．．．
f
。 l f电k k
i l nk o ns ee:n
se en『Lli n 『k丁」 ＝depth＋14
craw14 一queU e append （ 14· 工n k ）
－
现在有了这一功能， 我 们 就 有信心 爬 虫 最 终 一定能够完成。如果想要禁用
该功能，只需将max_depth设为一个负数即可，此时 当前深度永远不 会与
之相等。
最终版本
这个高级链接爬虫的完整源代码可以在 https://bitbucket.org/
wspw/coed/srct/i/pcahpter01/link_crawler3.py下载得到。要测
21第1章 网络爬虫简介
试这段代码，我们可以将用户代 理设置为 BadCrwaler，也就是本章 前文所
述的被robots.txt屏蔽 了的那个用户代理 。从下面的运行结果中可以看出，
爬虫果然被屏蔽了，代码启动后马上就会结束。
》＞ see_durl＝ ’thtp:/ /ex四iple.webscrpaing.c。m/idnex'
》＞ link_rege＝x ’／in（dexvlie）w’
》＞ lin_kcrawelr(see_durl, link_rege,x use_ragent’B＝adrCawelr’｝
Blockebdy robot.sxtt: htpt://example.webscrapin.gocm/
现在， 让我们使用默认的用户代 理，并将最 大深度设置为1 ，这样只有主
页上的链接才会被下载。
》＞ link」crawrl(seee_durl,link_rege,x max_depth=l)
D。wnl。dain:ghtpt://example.webscrpain.gocm//index
Downl。dain:ghtpt://eamxple.webscrapin.g。cm/index/l
Downl。adi:nhgttp://example.webscrap.icnogm/view/Antiagunad--Barb-u1d0a
D。wnl。dain:ghtpt://xea皿1ple.webcsr apin.c g。m/vienwt/aArcitca9-
D。wnlodain:ghtpt://example.webscrapin.g。c皿／ivewA/nguilla-8
Download:i nhgtpt://example.webscraping.com/veiw/Angl。a-7
Downlodain:g htpt://example.webscraping.com/vie/wAndorra-6
D。wnload:ihngtpt://xe皿1ple.webscrapin.c g。mv/iew／e阳.ricna-S础。a-5
D。wnloandg:ihtpt://ex四ple.w，由scraping.com/vieAwl/greia-4
Downloadinhgt:pt ://example.webscrapin.gcom/vieAwl/bnaia-3
D。wnl。adingh:tpt://eamxple.webscraping.com/vie/wAlan工ds－lands-2
D。wnl。adingh:tpt://example.webscraping.c。m/view/Anfigshatan-1
和预期一样，爬虫在下载完国家列表 的第一页之后就停止了。
15. 本章小结
本章介绍了网络爬虫， 然后开发了一个能够在后续章 节中复用 的成熟爬
虫。此外， 我们还介绍了一些外部工具和模 块的使用方法，用于了解网站、
用户代理、网站 地图、爬取延时以及各种爬取策略。
下一章 中，我们将讨论如何从己爬取到的网页中获取数据。
22第2章
数据抓取
在上一章中， 我们构建了一个爬虫，可以通过跟踪链接的方式下载我们所
需的网页。虽然这个例子很有意思 ，却不够实用，因为爬虫在下载网页之后
又将 结果丢弃掉了。现在，我们需要让这个爬虫从每个网页中抽取一些数据，
然后实现某些事情， 这种做法也被称为抓取（scrpanig。）
首先，我们会介绍一个叫 做FierbuLgit的浏e览器扩展，用于检查网页内
容，如果你有一些网络开发背景的话，可能己经对该扩展十分熟悉了。然后，
我们会介绍三 种抽取网页数据的方法，分别是正则表达式、BeautiS削opu和
lxm。l最后，我们将 对比这三 种数据抓取方法。
21. 分析 网页
想要了解一个网页的结构如何， 可以使用查看源代码的方法。在大多数浏
览器中，都可以在页面上右键单击选择Viepwagsoeu rc选e工页，获取网页的
源代码，如图21.所示。
我们可以在H刊伍 的 下述代码中找到我们感兴趣的数据。
<tbale>
<tri d”＝plasc_neatoinala_gf_lrow”＜＞tdc lass2＝p”f_wl”＜＞lbael
for”＝plasc_entainoal_f”l ag第 2 章 数据抓取
id＝”placensa tionafll ag labe”l＞ NationaFll ag:
</label></td><ctlda ss＝”w2fpw ”＞＜img
src＝”／places/static/images/flag”s／/＞g＜b／.tpd口>g<td
class="w2fpc ”＞＜／td></tr>
<tr id＝”place口seighboursrow"><tdc lass＝”w2fpl ”＞＜label
for＝”placense ighbours”
id＝”placense ighboursl abel ”＞Neighbour<s/:l abel></td><td
' class＝”w2fpw ”＞＜div><har ef＝”／iso/IE”<＞/IaE> </div></td><td
class＝”w2fpc ”＞＜／td></tr></table>
•
Hon'.e 3号J「ci飞 l Lc;i.:ir1
NatioFnlaalg : 器重
Area: 244,8s2q0u akriel orne甘es
Population: 62,348.447
lso GB
叫
Country: Unit Back
Capital: London ForNa•d
Continent: EU Reload
Tld .uk
Savase . .
CurreCn创cey GBP
CurreNnacmye Poudn Print
Phone: 44 TranstloaE tneg lisl1
PostCaold Feo 『ma@t#:#@@t@
#@@#@!! @
Viepawg
PostCaoled R eg剧。＇（（［.舟苟明勾i
{ Z)2 \d[} A\ 'Z阴dZ 阳{'!I]2' �¥- ’.}， [nsA因 cwt1lFli1r eLbiulge •
(GIROA四 A）”J SONView
Languages: en-GB,c�y -uGsIe r-ASgweinttc her
Neigh也ours:IE 、
Inspecetl ement
Edit
图 2.1
对于浏览器解析而言， 缺失空白符和格式并无大碍，但在我们阅读时则会造
成 定困难 要想更好地理解该表格 我们将使用 FireLbiu扩tg展e。该扩展适
一 。 ，
用于所有浏览器，我们可以通过http:s//getfbiur.geocmf/irebluiget
页面获取到该扩展。如果愿意 的话，Fire用fo户x可以安装完整版的 Friebug
242.1分 析网页
扩展，不过Lit版e本己经包含了我们在本章和第6章中所用到的功能。
FireLbiu安tge装 完成后，可以右键 单击我们在抓取中感兴趣的网页部分，
然后在菜单中选择InpsecwtitFhie rbuLgi ，te如图 2.2所示。
NatioFnlaalg : 留罢
Area: nHI问3s1unU盯eL民OHHMM、
dH M
Population. 缸 BU FMm6 4斗a7 M、
lso: G
！ J
C Co au pn it tr ay l: U Um川 dB mdK HW－ ku 叶阳c i FB Ea wX
: fH
山 l
Continent: Eu RemJAU
－
Tld: .llk U
Cu厅encCyode: GBP － Sav ea s.
CurrencNya me: Pound Prmt...
Phone: TranslattoEe n glish
Viewp ages oume
Vi四＇／pageinfo
Languages: en-GB,cBjy-、IG Usere-nAStwg
itche「
Neighbou「BIE
Inspeeclte ment
Edit
图 2.2
此时，浏览器就会打开如图 2.所3示的 Fierbu面g板，并显示选中元素周
围的HTML层 次结构。
如图2.3所示，当选择国家面积这一属性 时，我们可以从Frieb面u板g中
清晰地看到，该值包含在 clsas为 wp2 fw的＜td＞元素中，而＜td元＞素又是
ID为placeasrear ow的＜tr元＞素的子元素。现在，我们就获取到需要
抓取的面积数据的所有信息了。
25第 2章 数据抓取
拼
Inspect
co1n画面可sm脚
ScriptD OM
百飞际aa>
臼＜bodydat-af<.> edlym-ini;y"es ">
臼＜divclass"=navbanra vb盯－inverse”〉
曰＜div class="container、
日＜sectioind＝可naicnl"ass＝阴阳irnow与
日＜divclasss=p·a n旦、
国＜fomraction＝”e＃n”ctype＝飞ultrti/pfaonn­
data”mεthod＝o’s＇tp”〉
曰＜table>
曰＜tbody>
<tri d=p"l ac_ensatioln_fa l ag_row＇、
<tr i=d"placse_area row"'>
_
<td class="_1"f2lp” 〉
隔嗣砸醋幅腼幽幽翩翩町
<tdc lass＝2”pw_cf"/>
</tr>
图 2.3
2.2三 种网页抓取方法
现在我们已经了解了该网页的结构，下面将要介绍三种抓取其中数据的方
法。首先是正则表达式，然后是流行的BeautifulSupo模块，最后是强大
的 lxml模块。
2.12 .正则表达式
如果你对正则 表达式还不 熟悉 ，或 是需要一些提示时禽 ，可 以查 阅
htpts://doc.sptyho.日rog/2/hwot/orege.hxtm获l得完整介绍。
当我们使用正则表达式抓取面积数据时，首先需要尝试匹配＜td＞元中素
的内容，如下所示。
》〉 工mportre
》＞ url＝ ’thtp://exampel.websrcapi口.gcom/ivew/Un工ted
-Kingdom2 39’
》＞ html= downloa(dur)l
>>> re.findall（＜’td clas＝s”w2pf w ”＞(. * ?<)/ td＞’ ，html)
［＜’imgs rc＝”p／lacse/satt工c/imgaes/lfag/sgb.png”／〉’ ，
262.三2 种网页抓取方法
’4248,20s quarkei lmoetre’s，
’26,34,8447 ’ ，
’BG’，
’UnitKeidn g。dm’ ，
'。Lndo’n，
’a＜ hrfe＝”le。口ti/nEe”U＞nEtU/<a’＞，
’u.k’ ，
’BGP’，
’Poun’d，
’44 ’ ，
’＠＃# @@I#@## @@I自由＃＃＠I日@@###@@I#@@ @@#I＠＠＃#自@@IGIROAA’，
『＂（［（-AZ]\\d{}2[AZ-]2{})I( A[-Z]\\d{3}[AZ-]{2})I ( A[-Z]2{}\\d{2}
[A-Z] 2}{)I ( [ AZ-] 2}{\ \ d{3)[A -Z]2 }){I ( A -[Z]\ \ d[ZA]\-\ d[』AZ] {})2
I( A[-Z]{2\}\dA[-Z]\\d[A-Z]{2})I ( IGROAA））$’ ，
’ne-BG,yc-BG,gd’，
’d＜iv><har e＝f”／isoE／”I工＞E</a>/<div’］＞
从上述结果中可以看出，多个国家属性都使用了＜tcdlasws2p= "fw">
标签。要想分离出面积属性，我们可以只选择其中的第二个元素，如下所示。
》＞ re.f inadl（l ’t＜dc lass2＝p”f w w”（＞•.？）＜／td＞’ ，htm)l[ l]
’4248,20s quarkei lm。etres’
虽然现在可以使用这个方案，但是如果网页发生变化，该方案很可能就
会失效。比如表格发生了变化，去除了第二行中的国土面积数据。如果我
们只在现在抓取数据，就可以忽略这种未来可能发生的变化。但是，如果
我们希望未来还能再次抓取该数据，就需要给出更加健壮的解决方案，从
而尽可能避免这种布局变化所带来的影响。想要该正则表达式更加健壮，
我们可以将 其父元素＜tr＞也加入进来。 由于该元素具有 ID属性，所以应
该是唯一的。
》＞ re.finadl（l’t＜ri d＝”placaerse ar ow”＜＞td
class＝”2wpf l”＞＜lbaelf or＝”plaarce”ea s
id＝”placaerse al abel”Ar＞e:a </lbael/>td<>t<d
class2＝p”f w w”（〉．？丰）＜／td＞’，htm)l
［2冒4,4820squarkei lmoetres’ ］
27第2章 数据抓取
这个迭代版本看起来更好一些，但是网页更新还有很多其他方式，同样可以
让该正则表达式无法满足。比如， 将双引号变为单引号，＜td标＞签之间添加多
余的空格，或是变更arealabel等。下面是尝试支持这些可能性的改进版本。
》＞ re.f inadl（l＜ ’tr
id="placaerse ar 。w”＞•.＜？tds\•clsa＝［s＼”’w］2pfw［＼”’〉］（＊？．）
</td＞’，htm)l
［’4248,20s quarkei lmoetre’s］
虽然该正则表达式更容易适应未来变化， 但又存在难以构造、可读性差的
问题。此外，还有一些微小的布局变化也会使该正则表达式无法满足，比如
在＜td＞标签里添加 titl属e性。
从本例中可以看出，正则表达式为我们提供了抓取数据的快捷方式， 但是
该方法过于脆弱，容易在网页更新后出现问题。幸好，还有一些更好的解决
方案，我们会在接下来的小节中继续介绍。
2.2.B2eu atliS foupu
Sou是p一个非常流行的Pytho模n块。该模块可以解析网页，并
Beautuilf
提供定位内容的便捷接口。如果你还没有安装该模块，可以使用下面的命令
安装其最新版本：
pipi nsatllb eautfiuls。up4
使用 BeuatfuilSuop的第一步是将 己下载的HTML内容解析为sopu文档。
由于大多数网页都不具备良好的HTML格式，因此BeuatfuilSuop 需要对其
实际格式进行确定。例如，在下面这个简单网页的列表中，存在属性值两侧
引号缺失和标签未闭含的问题。
<ulc la=scsountry>
<liA>rea
<liP>。pluation
</ul>
2822. 三种网页抓取法方
如果 Populaotni列表项被解析为Are列a表项的子元素，而不是并列
的两个列表项的话，我们在抓取时就会得到错误的结果。下面让我们看一下
BeuatfuilS opu是如何处理的①。
》＞ frmo bs4i mporBte aiuuftlSuop
》＞ br。kehtnm＝l ’u＜lc lascso=un>t<rlyiA>relai<>oPpulatni</oul’＞
》＞ # pasret heH TML
》＞ soup= BeauftuliSuop(breon_khtlm，’thm.laprs’er）
=
》＞ fixehdt ml sopu.rpettiyf()
》＞ prinfti xehdt ml
<ht>m l
<body>
<ulc lascso＝u”rnyt”〉
<liA>re／a＜工i>
<l>iPolpautni</oli>
</ul>
</body>
</htm>l
从上面的执行结果中可以看出，BeaiutfulSoup能够正确解析缺失的
引 号并闭合标签， 此外还添加了 ＜html＞和＜body标＞签使其成为完整的
HTML文档。现在可以使用 fidn（和）fidnal（l方） 法来定位我们需要的
元素了 。
》＞ ul= soup.ifn（du ’l’，attr｛sc’＝las’s ：co’u口yt’r｝）
》＞ ul.f in（d’ li#’ r）et urjnusst t hef irsmta tch
<liA>re/a<li>
》＞ ul.除fina…dl （了l ’土l’倒#） ret叫uranlslm at…ches …档 ］
[l<iA>re<a/li<>l,i o>pPluat口i＜／。li]>
［¢
其网址为：htpt:/w/ww.crummy.ocm/softwrae/
Beuatifu1Suop/b4s/doc。／
译者注2此处使用的是时也 on内置库，由于不同版本的容错能力有所区别，读者在实中践可能无法得到
① 正 确结果。相关内容可参考zhttp:s//www.rcummy.com/sfotawr/eBeuatifuu1p/Sbo4sd/oc/
#instailnlg-paar-s.e r
29第2章 数据抓取
下面是使用该方法抽取示例国家面积数据的完整代码。
》＞ frmo bs4 imporBte auftuiluSpo
》＞ url＝ ’thtp://exmpal.ewesbcrpain.gocmp/lac/evsiew/
UniteKdi ndgom2 3’9
》＞ htm=l donwloa(dur) l
》＞ soup= BeauftuliSou(pthm)l
》＞ #1 。cattheea rerao w
》＞ tr= soup.fin(dtatr＝s｛’di’：’lpac_earse_arow’｝）
》＞ td= tr.fin(dtatr｛sc＝’las’s：w 2’p_wf’））# loactet hea retaa g
》＞ are=a t d.tex#t e xtratchtet exftr mo thsi tag
》＞prinatr ea
2448,20s quarkei lmoetres
这段代码虽然比正则表达式的代码更加复杂， 但更容易构造和理解。而且，
像多余的空格和标签属性这种布局上的小变化，我们也无须再担心了。
2.2.L3xm l
Lxm是l基于 libxml2这一 XML解析库的 Pyth封o装n。 该模块使用 C
语言编写，解析速度比BeuatilSfuuop更快，不过安装过程也更为复杂。最新
的安装说明可以参考 htpt://Lxml.ed/instlaatlion.thmlo
和 BeuatfuilSoup 一样，使用 lxml模块的第一步也是将有可能不合法的
HTML解析为统一格式。下面是使用该模块解析同一个不完整 HTML的例子。
》＞ imporltxm l.h tml
》＞brkoenh tm＝l ’u＜lc las=scountlriyA>>r<elai<>oPpulation’< /ul＞
》＞ tre=e l xml.h tm.lf rmostrin(gb rkoe_nh tm)l p#a rsteh eH TML
》＞ fixehdt m=l lxml.thm.lt otsrnig( rte,e pret_tpyirnt=T)r ue
》＞ prinfti exd_html
<ulc lass＝c”ournyt">
<liA>re/a<li>
<l>iPopluatino</li>
</ul>
同样地，lxml也可以正确解析属性两侧缺失的引号，并闭合标签，不过
该模块没有额外添加＜html＞和＜boyd＞标签。
302.三2 种网页抓取方法
解析完输入内容之后，进入选择元素的步骤，此时 lxml有几种不同的方
法，比如XPath选择器和类似 BeuatfuilSuop 的fin（d方）法。不过，在本例
和后续示例中，我们将会使用 cs选s择器，因为它更加简沽，并且能够在第
5 章解析动态内容时得以复用。此外，一些拥有jQurye 选择器相关经验的读
者也会对其更加熟悉。
下面是使用 lxml的 css选择器抽取面积数据的示例代码。
》＞ tre=e l xml.h.tfmrmlostrnig(htm)l
》＞ td = tre.escsselec（tt’rp#lac_easre_ar。w> td.w2p_fw’）[O ]
》＞ are=a t d.textc ontent()
》＞ prinatr ea
2448,20s quarkeil omteres
css选择器的关键代码行己被加粗显示。该行代码首先会找到 ID为
placs earearo w的表格行元素， 然后选择 cla为sws2pf 的w表格数据
子标签。
css选择器
cs选s择器表示选择元素所使用的模式。下面是一些常用的选择器示例。
选择所有标签：＊
选择＜a＞标签： a
选择所有class”＝lnik的”元素： l.ink
选择clsas＝”li口k的”＜a标＞签： .alikn
选择id"=hom”e的＜a标＞签： Jfahome
选择父元素为＜a标＞签的所有＜span子＞标签： a> span
选择＜a标＞签内部的所有＜span标＞签： aspan
选择tilte属性为”Hom”e的所有＜a标＞签： a[tilteH=om]e
［�
W3C己提出CSS规3范，其网址为htt:pI/ ww.ww 3. o rg/ TR I
/20/1RE1C-css3s-elteorcs-02119029／。 E
Lxml已 经 实 现了 大部 分 CS3S属 性 ，其 不 支 持的 功 能可 以 参见
http:s//pythonshteod.rogc/ssseletc/s#upport-esdelteocr。s
31第 2 章 数据抓取
需要注意的是，以ml在内部实现中，实际上是将 css 选择器转换为等价
的XPtah选择器。
2..24性 能对比
要想更好地对本章中介绍的三种抓取方法评估取舍，我们需要对其相对效
率进行对比。一般情况下，爬虫会抽取网页中的多个字段。因此，为了让对
比更加真实，我们将为本章中的每个爬虫都实现一个扩展版本，用于抽取国
家网页中的每个可用数据。首先，我们需要回到Fireb中u，g检查国家页面其
他特征的格式，如图2.所4示。
lnesdp
l_＿！：！！：匹J
Console 1CSS Script DOM
�
曰 ＜table>
曰 ＜tb同ldy>
田 ＜t「id＝p“lace_snationafll_a g一＿row">
囡＜t「id＝p』l＇aceasrea＿「·ow">
因＜t「id=p"lacse_poupllati_or11ow与
<t「id=p"laces_i so_ rnw">
因＜trid＝p”laces_cou_nrtarwy刨 〉
田《t「id＝p”la仨ecsa伊工tal一＿row副〉
囚＜trid＝”place_cso咽ti凹E阳一t「ow"
囚＜t「id＝”plcaes一tld一rn制＂ '
囚＜t「i.d＝p‘ll曰cse_rnrE「盯cy_cocie『一口w”〉
曰 ＜t「id＝’pll acse_r nr扫ency＿问吕匹e一 『ow"〉
<t「 i.d="places_.ptlorne_ row">
[±} <t「id＝口”lace,_.postla_c m！悟＿fo「由at_row"·:,
囡 ＜t「 id＝”places_.p臼stal_cod一eregex＿ 「ow">
<t「 i.d＝”place_slanguages一「m1’、
IB <t「id=p"laecs._neighbours_row">
</t'body> 、，，
</：1也面le>
图 2.4
从 Fireb的u显g示中可以看出，表格中的每一行都拥有一个以places
起始且以 row结束的ID。而在这些行中包含的国家数据，其格式都和上面
的例子相同。下面是使用上述信息抽取所有可用国家数据的实现代码。
322.三2种 网页抓取方法
FIEDLS= （a’rea’，’oppluatni’o，’si。’ ，’ocunt’r，y’acpita’l，
’ocnitnen’t，’ ltd’，’ucrrenccoyed’ ，’ucrrenncamye’ ，’hpon'e,
’opst_acloed_froma＇t，’opstalc_oder_eg’ex，la’nguasg’ e，
’neighbuor’s ）
imporrte
def res crpear(thml):
resluts= ){
forf ielidnF IELD:S
resul[tifsel]d r=e.searc（h＜’t ri d＝”plac＿e毛ss一＿rwo”.＞？•＜td
•
class＝”2wpf w＞”< *?l< It d＞’ f毡ielhdtm,l). rgoup(s[)0 ]
returrne sults
frmo bs4i mporBte atuiuflSuop
def bs_scraepr(thml):
soup= BeatuiuflSuop(thm，l’thm.laprs’er）
reuslt=s { )
f。rfielidnF IELD:S
resul[ftise]l ds=oup.ifn（dt’abl’e. ）if n（dt ’r’，
id’＝lpace'毛ssro’w 毛fiel.dif)n（dt ’d’，
clas＝s’2 wpf w ’）. etxt
returrne sults
－mport14xml －htm14
－
－d ef 14 txm r14 e－s =ec r ap xme lr .（ h ＋」 thm m14
l .lfrmostri(nthgm)l
r e su t l s = { )
f。r fielidnF IELD:S
resul[tifsel]d t=r e.escssele（ct’tabl>e t r#pla宅cSersow
> td.w2pf w’ 毛fiel[d0).]etx tc 。nte(n)t
reutrnr esults
抓取结果
现在，我们已经完成了所有爬虫的代码实现，接下来将通过如下代码片段，
测试这三种方法的相对性能。
importtim e
NU_MITERAITONS= 100#0 n ubmero ft imes t。tesetahc scraper
htm=l d。nwloa（hd’ttp://exapml.ewebsrcapi.nocgm/plac/evsiew/
Unitedn-gdK。i-m239’ ）
33第2章 数据抓取
forn ame, scarpeirn ［ ’（eRgulaerx psrseion’s，re_scraepr,)
（B’eaiuftulSupo’，bs_rsacepr,)
（L’xml’，lxmls carper]):
# recd。srtarttim e。 fscrape
star=t t ime.t ime()
fori inr ang(eUNMI TERATIONS) :
ifs crape=r= r es craper:
re.purg(e)
resu=l tscrpear(thm)l
# chceks craperde suilsta se xpected
asser(tersu［lat’r ea’］＝＝’4248,20s quarkei lmoetre’s）
# recdo erndt imeo fs crpaea ndo utputth et 。tal
end= time.t ime()
pri口’ts屯：宅.f2secnod’s 毛（nmae,end- sta)r t
在这段代码中，每个爬虫都会执行 100次0，每次执行都会检查抓取结果
是否正确，然后打印总用时。这里使用的 dowlnoad函数依然是上一章中定
义的那个函数。请注意，我们在加粗的代码行中调用了re.uprge（ 方）法。
默认情况下，正则表达式模块会缓存搜索结果， 为了与其他爬虫的对比更加
公平，我们需要使用该方法清除缓存。
下面是在我的电脑中运行该脚本的结果。
$ pythno perf。rmance.yp
Regulare xperssi。:ns5.05 seconds
BeautfiulSu。p:42.48 sec。nds
Lxml : 7.60 sec。nds
由于硬件条件的区别，不同电脑的执行结果也会存在一定差异。不过， 每
种方法之间的相对差异应当是相当的。从结果中可以看出，在抓取我们的示
例网页时，BeuatfuilSuop比其他两种方法慢了超过 6 倍之多。实际上这一结
果是符合预期的，因为 lxml和正则表达式模块都是 C 语言编写的， 而
BeaiutfulSuop则是纯 Pytho编n写的。一个有趣的事实是，lxml表现得
和正则表达式差不多好。由于 lxml在搜索元素之前，必须将输入解析为内
部格式，因此会产生额外的开销。而当抓取同一网页的多个特征时，这种初
始化解析产生的开销就会降低，lxml也就更具竞争力。这真是一个令人惊叹
的模块！
342.三2 种网页抓取法方
2.2.结5论
表 2.总1结了每种抓取方法的优缺点。
表2.1
抓取方法 性能 使用难度 安装难度
正则表达式 困难 简单 （内置模块）
快
BaeutSiopfuu l 简单 简单 （纯P归ho)n
↑曼
Lxlm 简单 相对困难
快
如果你的爬虫瓶颈是下载网页，而不是抽取数据的话， 那么使用较慢的方
法 （如 BeuatfuilSuop）也不成问题。如果只需抓取少量数据，并且想要避免
额外依赖的话，那么正则表达式可能更加适合。不过，通常情况下，lxml是
抓取数据的最好选择，这是因为该方法既快速又健壮，而正则表达式和
BeuatfuilS uop 只在某些特定场景下有用。
2.2.为6链 接爬虫添加抓取回调
前面我们已经了解了如何抓取国家数据，接下来我们需要将其集成到上
一章的链接爬虫当中 。要想复用这段爬虫代码抓取其他网站，我们需要添
加一个 callbac参k数处理抓取行为。callbcak是一个函数，在发生某
个特定事件之后会调用该函数（在本例 中 ，会在网页下载完成后调用）。 该
抓取 callbac函k数包含 ur和l htm两l个参数，并且可以返回一个待爬
取的 URL列表。下面是其实现代码，可以看出在Pyth中o实n现该功能非
常简单。
def lin_kcrlawe(r. ., .sc rap_ceallbakc=No)n:e
=
links[ ]
ifs crpae_callba:c k
links.extend(scrap_ecallbac(kurl, ht皿1） 。r[])
35第2章 数据抓取
在上面的代码片段中，我们加粗显示了新增加的抓取callba函c数k代码。
如果想要获取该版本链接爬虫的完整代码，可以访问httsp://bibtucekt.
org/pw/scwoed/scr/tipc/hpatre02/linckr wale.ryp。
现在，我们只需对传入的 scrape callbac函k数定制化处理， 就能使
用该爬虫抓取其他网站了 。下面对 lxml抓取示例的代码进行了修改，使其
能够在 callbac函k数中使用。
def scrapcea llbcak(rul, htlm):
ifr e.searhc（ ／’vie'w,/u r)l :
tre=e l xml.thm.lfrmostrin(tghm)l
row= [rte.ecsssele（ct’table> trp#lac告essrow>
td.2wpf w’ 屯fiel[0d ]).t excto nte(n)ft orf ielidn
FIELD]S
print , urrolw
上面这个 callbac函k数会去抓取国家数据，然后将其显示出来。不过
通常情况下，在抓取网站时，我们更希望能够复用这些数据，因此下面我们
对其功能进行扩展，把得到的结果数据保存到csv表格中，其代码如下所示。
imporcts v
clasSscr apeCalbalc:k
def init( eslf:)
self.writ=e rc s.vwrit｛ep。re （nc’ouniter.scsv’，’w）’）
self.fileds＝ （a’rea’，’oppulatni’ o，『sio’，’ocuntr’y，
’acpilta’’，ocntitne’，n’ltd’，’ucrren_ccoyd’e，
’curre_nncaym’e，ph’on’e，po’slt_acoder_mtfa’ o，
’opsatlc odree g’ex，’alnugage’s，
’enihgbuor's)
sel.frwietr.writoew(resl.ffiled)s
def call( eslfu,r ,l htlm):
ifr e.searc（h／’ viwe／’， rul) :
=
treel xml.thm.lfrm。strin(ghmtl)
row= []
forf ielidns elff.iled:s
ro.wappen(drte.ecsssele（ct’table>
tr#pla{c}ers o w>
362.2三 种网页抓取方法
td.w2p fw’f.o rma(t field))
•
[0 Jt extc onten(t))
self.write.rwriterow(row)
为了实现该 calblac，k我们使用了回调类，而不再是回调函数，以便保
持 csv中 wrietr属性的状态。csv的 writ属e性r在构造方法中进行了实
例化处理，然后在 call方 法中执行了多次写操作。请注意， call
是一个特殊方法，在对象作为函数被调用时会调用该方法，这也是链接爬虫中
cachec allbac的k调用方法。也就是说，scrpaecalblac(kru l,h tm)l
和调用 scarpe callbac. kcall (rul,h tm）l是等价的。 如果想要了
解更多有关Pytho特n殊类方法的知识，可以参考 https://docs.pytnh.o
org/2/erferenc/edatamdoelh.tm#lpseci-amletdh-onmaes。
下面是向链接爬虫传入回调的代码写法。
linkc rawle（rh’ ttp://exampl.ewebscrapign.cmo／’，’／工（ndexlview）’，
maxd epth-=1,s crapec allbackc=rSapeCablalck( ))
现在，当我们运行这个使用了 calblac的k爬虫时，程序就会将结果写
入一个 csv文件中，我们可以使用类似 Exce或l者 LiebOrffic的e应用查看该
文件，如图2.所5示。
图 2.5
37第2章 数据抓取
成功了 ！我们完成了第一个可以工作的数据抓取爬虫。
2.3本章小结
在本章中，我们介绍了几种抓取网页数据的方法。正则表达式在一次性数据
抓取中非常有用，此外还可以避免解析整个网页带来的开销：BeatuiuflSuop
提供了更高层次的接口，同时还能避免过多麻烦的依赖。不过，通常情况下，
lxml是我们的最佳选择， 因为它速度更快，功能更加丰富，因此在接下来的例
子中我们将会使用 lxml模块进行数据抓取。
下一章，我们会介绍缓存技术，这样就能把网页保存下来，只在爬虫第一
次运行时才会下载网页。
38第 3 章
下载缓存
在上一章中，我们学习了如何从己爬取到的网页中抓取数据，以及将抓
取结果保存到表格中 。如果我们还想抓取另外一个字段，比如国旗图片的
URL，那么又该怎么做呢？要想抓取这些新增的字段，我们需要重新下载整
个网站。对于我们这个小型的示例网站而言，这可能不算特别大的问题。但
是，对于那些拥有数百万个网页的网站而言，重新爬取可能需要耗费几个星
期的时间。因此，本章提出了对已爬取网页进行缓存的方案，可以让每个网
页只下载一次。
31. 为链接爬虫添加缓存支持
要想支持缓存，我们需要修改第 1 章中编写的 dowlnoad函数，使其在
URL 下载之前进行缓存检查。另外，我们还需要把限速功能移至函数内部，
只有在真正发生下载时才会触发限速，而在加载缓存时不会触发。为了避免
每次下载都要传入多个参数，我们借此机会将 dowlnoad函数重构为一个类，
这样参数只需在构造方法中设置一次，就能在后续下载时多次复用。 下面是
支持了缓存功能的代码实现。
clasDson wloeard:
def一＿ini_t(eslfd,ela=yS,第3章 下载缓存
use_argent’＝swwp’，prxoieNso=en,
numr etires,= c!ache=N)。n:e
selft.hrtotl=e Thorttl(eedlay)
sel.fsuer_agen=t u se_ragent
self.prxoie=s proxies
self.numr etri=e nsu mr etries
self.cahce= cache
def call( eslfu,r )l:
resu=l Nto ne
ifs elf.c ach: e
tr:y
resu=l ts elfc.ach[uer]l
excpetK eEyrr:o r
t urli sn ota vailablei nc ahce
pass
els:e
ifs elfn.umr etri>e sa0 nd\
500< = res［cu’oldt’el 6<0: 0
t serveerr rors oi gnorree suflrtmo cache
t andr e-odwnload
resu=l Nt。 ne
ifr esuilstN 。n:e
# resuwlats nlootda edf rmo cache
# sos tilnle etdo d owlnoad
sel.tfhrott.lawei(trul)
prox=y rando.mhcoic(eesl.fproixes)i fs elfp.rxoies
elsNeo ne
heade＝r｛sU ’searg-en’t：self.use_ragen}t
resu=l ts elf.donwloa(drul, heaedr,s prx。y,
sel.nfumr etire)s
ifs el.cf ac:h e
# saver esutlotc ahce
sel.cfach[uer]l r=e sult
returrne su［lh’ttm l’］
def dowlnoad(selufr,,l heaedr,s pro,x ynumr_etire,s
data=N)o n:e
reutrn｛ h’tml’：htm，l’。cde’：coed}
403.为1链 接爬虫添加缓存支持
下载类的完整源码可以从http:s//bitbukcet o.rg/l
wspw/coed/scr/tip/chpatre03o/wpdloaedr.yp I
获取。 _J
前面代码中的Donwloa类d有一个比较有意思的部分，那就是 call
特殊方法，在该方法中我们实现了下载前检查缓存的功能。该方法首先会检
查缓存是否已经定义。如果已经定义，则检查之前是否已经缓存了该URL。
如果该URL 己被缓存，则检查之前的下载中是否遇到了服务端错误。最后，
如果也没有发生过服务端错误，则表明该缓存结果可用。 如果上述检查中的
任何一项失败，都需要正常下载该URL，然后将得到的结果添加到缓存中。
这里的 dowlnoa方d法和之前的donwload函数基本一样，只是在返回下载
的 HTML时额外返回了HTT状P态码，以便在缓存中存储错误码。当然， 如
果你只需要一个简单的下载功能，而不需要限速或缓存的话，可以直接调用
该方法，这样就不会通过 call 方法调用了 。
而对于 cach类e，我们可以通过调用resul=tcahce[ rul］从 cahce
中加载数据，并通过 cahce[rul]= result向 cahce中保存结果。大家
应该很熟悉这种便捷的接口写法，因为这也是ηthon内建字典数据类型的使
用方式。为了支持该接口， 我们的 cahce类需要定义＿ geittme一 （ ）和
settiem （这）两个特殊的类方法。
此外， 为了支持缓存功能，链接爬虫的代码也需要进行一些微调， 包括添
加 cahce参数、移除限速以及将 dowlnoad函数替换为新的类等，如下面的
代码所示。
def linkc rawl(.e .r, .ca hce=No)n:e
crwal_uqeu=e [ese_durl]
see=n {seeudr :l }0
numu rl=s 0
rp= ge_trobs。s(tee_dur)l
D =D onwlodear(edla=ydelayu,s e_ragenuts=e_arge,n t
proexsip=rxoies, nrume tr=inemus_retreis, cac=hceahce)
41第3章 下载缓存
whliec rwalq ueu:e
=
url crwal_queu.peop()
=
depths ee[nrul]
# chceku rl speasrs obo.txtstr esttriiocns
ifr p.can_eftc(hsue_rage,n utr)l:
=
html D( rul)
=
links []
到 目前为止，这个网络爬虫的基本架构已经准备好了，下面就要开始构建
实际的缓存了。
3.2磁 盘缓存
要想缓存下载结果， 我们先来尝试最容易想到的方案，将下载到的网页存
储到文件系统中。 为了实现该功能，我们需要将URL 安全地映射为跨平台的
文件名。表 3.所1示为几大主流文件系统的限制。
表3.1
操作系统 文件系统 非法文件名字符 文件名最大长度
Linux Ex尼tx3t4 ／ 和0＼ 255字节
HFPSl us ： 和0＼ 25个5UTF-1编6码单元
osx
Windows NTSF 25个5字符
飞、／、？、、：气、”、〉〈和｜
为了保证在不同文件系统中，我们的文件路径都是安全的，就需要限制其
只能包含数字、字母和基本符号，并将其他字符替换为下划线， 其实现代码
如下所示。
》＞ imporrte
》＞ url＝ ’thtp://exmapl.weebscrpain.cg。m/fdauel/tview/
Austra-l1i’a
》＞ r.esu（b ［’／《0-a9-Az-Z＼一．，； ］，’” ，ur)l
’thtp一／／exmapl.eewbcsrapin.cgom/fdaeu/lvtieAuws/tra-l1’ia
4232. 磁盘缓存
此外，文件名及其父目录的长度需要限制在25个5字符以内（实现代码如
下）， 以满足表 3.中1给出的长度限制。
》＞ filename＝ ’’／.jion(semgen[t:525] fors emgenit n
fielnmae.spilt（ ’’／） ）
还有一种边界情况需要考虑，那就是URL 路 径可能会以斜杠 （）／结尾，
此时斜杠后面的空字符串就会成为一个非法的文件名。 但是，如果移除这个
斜杠，使用其父字符串作为文件名，又会造成无法保存其他URL 的问题。考
虑下面这两个URL:
htpt:I eIx mapl.ew esbc arping.c omi/n edx/
•
htpt:I/ example.w esbc rpaign.co mi/nedx1/
•
如果我们希望这两个 URL 都能保存下来，就需要以 ind作e为x目录名，
以 1作为子路径。对于像第一个URL 路径这样以斜杠结尾的情况，这里使用
的解决方案是添加 inedx.htm作l为其文件名 。同样地，当 URL 路径为空
时也进行相同的操作。为了解析 URL，我们需要使用urplars.uerlstp( l)i
函数，将 URL 分 割成几个部分。
》＞ imporutr plasre
=
》＞ compo口ents
urlrpsa.eurlsp（lh’itttp://exapml.ewebscarpin.gocm/idne／x）’
》＞ princtom ponesn t
SpiltResu(lstcheem＝’htpt’，netlo’ecxa＝mpl.ewebsrcapgi.nomc’，
path’＝i／nd／e’x，quer＝y” ，frgamnet”＝）
》＞princtom ponesnp.tath
’i／ndxe／’
该函数提供了解析和处理URL 的便捷接口。下面是使用该模块对上述边
界情况添加 inedx.html的示例代码。
=
》＞ path compo口net.spath
》＞ ifn otp at:h
》＞ pat＝h ’i／nedx.html’
》＞ elipfa t.ehndsthwi（’’：／）
43第3章 下载缓存
》＞ path ’＋ni＝de.xthm'l
》＞ filaemne= copmo口es口n.tetlo+c pat+h copmonnet.suqery
》＞ filenmae
’xeapml.ewebscrpain.cgom/inedx/dien.xthm’l
3.12 .实现
上一节中，我们介绍了创建基于磁盘的缓存时需要考虑的文件系统限制，
包括允许使用哪些字符、 文件名长度限制，以及确保文件和 目录的创建位置
不同。把 URL 到文件名的这些映射逻辑结合起来，就形成了磁盘缓存的主要
部分。下面是DiskCa类c的h初e始实现代码。
imporots
improtr e
imporutr laprse
clasDsik sCac:h e
def init( eslfc,a hced ir’c＝ach’e：）
selfc.ahced ir= cahced ir
sel.famxl engt=h maxl e口tgh
def urlt op at(hesl,f ur)l:
””Cr”eatfei lseys temp atfho rt hsi URL
’，’’’
copmonen=t usr lpsae.rurlpslit(rul)
# append eix.nhdtmlt oe mptyp aths
pat=h copmones口p.tath
ifn otp at:h
pat＝h ’i／nde.xthm’l
elipfa t.ehndstwhi（’’：／）
pat＋h＝ ’nide.xthm’l
fielnmae= componenst.entlo+c p at+h copmones口.tuqery
# replaicneav licdha racters
fielnmae= re.sub （ ’［ ／＂ -0 9 a -z -ZA 一＼ ，． ； ］ ’， ” ， f i e l n m a e)
# r e s t r im ca txi m um u n mb e or f ah c r a c t e r s
filaemne＝ ’／.j’ oin(s emge口t[:525]fors emgenitn
filneame.spl（i’t’／ ） ）
r e t u ro .ns pa ht . ij se(on l f. ca hc _e rd ,i f i e nl am e)
4432. 磁盘缓存
在上面的代码中，构造方法传入了一个用于设定缓存位置的参数， 然后在
url tpoah t方法中应用了前面讨论的文件名限制。现在，我们还缺少根
据文件名存取数据的方法，下面的代码实现了这两个缺失的方法。
－mpOE如」p－ek－－ee
l l
c －a ESD－· s －Keach e
def _gettie_rn(selfu,r )l:
””Lo”add atfar mo diskf ort hsi URL
pat=h sel.frul_to_ptah(ur)l
if。s.apt.hxeis(tpsaht):
wiht 。pe(napt，h’br’） asf p:
reutrnp ick.lolea(dpf)
els:e
# URhLa sn 。tyetb eecna ched
raisKeeyE rro(rrul＋ ’doesn ote xsit’ ）
def seteirnt (eslfu,r ,l restu)l:
””S”aved attao d iskf ort hsi url
pat=h selfu.r_ltop_at(hrul)
fold=e ros.apt.hdirrnnea(ptah)
ifn 。tos.apt.hxeis(tosfledr):
os.arnkedris(ofledr)
witohp e(npa，t’hbw’ ）a sf p:
fp.writ(epic.kdluernsp(ersutl))
在一 settie（rn一 ）中，我们使用 ur_lto _ pa t（h方） 法将 URL 映射为
安全文件名，在必要情况下还需要创建父目录。这里使用的 pick模l块e会
把输入转化为字符串，然后保存到磁盘中。而在＿ getietm （ ）法方中， 首
先将URL 映射为安全文件名。然后，如果文件存在，则加载其内容，并执行
反序列化，恢复其原始数据类型：如果文件不存在，则说明缓存中还没有该
URL 的数据， 此时会抛出KeyErro异r常。
45第3章 下载缓存
3.2.缓2存 测试
现在，我们通过向爬虫传递 cache回调，来检验 DisCkache类。该类
的完整源代码可以从htpts://bibtucetko.rg/pw/scwoed/rsc/pt/i
chpater0/3diskc ach.eyp获取。我们可以通过执行如下脚本，使用链
接爬虫测试磁盘缓存。
$ timep ythodni sk_cach.eyp
D。wnlodain:ghtpt://example.webscrapign.com
Downlodain:g htpt://example.webscrapin.gcom/view/Anfigshatan-1
D。wnlodain:ghtpt://e xm晤 le.webscrapin.gcom/viwe/Zil曲曲，we -252
23m38.28s9
第一次执行该命令时，由于缓存为空，因此网页会被正常下载。但当我们
第二次执行该脚本时，网页加载自缓存中，爬虫应该更快完成执行，其执行
结果如下所示。
$ timep yth。dnisk_cach.eyp
Om0.816s
和上面的预期一样，爬取操作很快就完成了。 当缓存为空时，我的计算机
中的爬虫下载耗时超过23分钟1而在第二次全部使用缓存时，该耗时只有01.68
秒 （比第一次爬取快了超过 700倍0。。 由于硬件的差异，在不同的计算机中
的准确执行时间也会有所区别。 不过毋庸置疑的是，磁盘缓存速度更快。
3.2.节3省 磁盘空间
为了最小化缓存所需的磁盘空间， 我们可以对下载得到的HTML文件进
行压缩处理。处理的实现方法很简单，只需在保存到磁盘之前使用 zlib压
缩序列化字符串即可，如下面的代码所示。
fp.writ(elzib.c。mpers(spilce.kdumsp(erslut)))
463.磁2盘 缓存
而从磁盘加载后解压的代码如下所示。
returpni ck.lloedas( lzib.decompre(spfs.r eda() ) )
压缩完所有网页之后，缓存大小从4.M4B 下降到 2.3BM，而在我的计算
机上爬取缓存示例网站的时间是0.122秒，和未压缩时的01.68秒相比只是略
有增加。当然，如果你的项目对速度十分敏感的话，也可以禁用压缩功能。
3.2.清4理 过期数据
当前版本的磁盘缓存使用键值对的形式在磁盘上保存缓存， 未来无论何时
请求都会返回结果。 对于缓存网页而言，该功能可能不太理想，因为网页内
容随时都有可能发生变化，存储在缓存中的数据存在过期风险。本节中 ，我
们将为缓存数据添加过期时间，以便爬虫知道何时需要重新下载网页。在缓
存网页时支持存储时间戳的功能也很简单， 如下面的代码所示。
frmo dateitmei mpordta tiemt,e timedleta
clasDsi ksCac:k e
def _in一i（teslf.,., .exp ir=etsimeeldt(aady=s3)0) :
=
self.expirese xpires
def getitem( eslf,u r)l:
”””L。addatfar mo diskf 。zthsi URL
wiht ope(napt，h’br’） asf p:
=
resu,l ttiemstmap
piclke.lodas(lzib.decm。press(pf.reda() ) )
ifs el.fahs peixre(idtmestapm):
raisKeeE yrorr(ur＋l ’has peirxe’d ）
returrne sult
els:e
it URLh asn oty etb eecna ched
rasieK eEyrorr(rul＋ ’doesn ote xsit’ ）
def settiem( eslfu,r ,l restu)l:
47第3章 下载缓存
””Sa”ved attao d iskf ort hsi url
tiemst amp= datetmie.u tcno(w)
=
data pikcl.edumsp( r(esulttim,e stamp))
witohp e(npa，t’hbw ’a）s f p:
fp.writ(lezib.comprses(adta))
def hase xpire(edslft,i emstmap:)
”””Retunr whtehetrh si tiemstmaph ase xpired
retudrant iemt.etucno(w)> tiemstmap sel.fxe pries
+
在构造方法中，我们使用 timedlet对a象将默认过期时间设置为30天。
然后， 在＿se一t方法中，把当前时间戳保存到序列化数据中：而在＿ ge一t
方法中，对比当前时间和缓存时间，检查是否过期。为了测试过期时间功能，
我们可以将其缩短为 5 秒，如下所示。
》＞ cache=DiksCac(heexpiresm=edteilt(aescn。d=sS) )
》＞ url＝ ’thtp://exmpal.ewesbcrapi.nocgm’
》＞ resu＝lt｛ h’tml’：’ ． ． ． ’ ｝
=
》＞ cahce[rul] result
》＞ cahce[ulr]
｛h’tm’l ：’ ． ． ． ’ ｝
》＞ importtim e; tiem.slee(pS)
》＞ cahce[rul]
Traceb(aomcskt r ecencta lllas t:)
KeyEorr：r’thtp://exmpal.ewebscprian.gocmh ase xpire’ d
和预期一样，缓存结果最初是可用的，经过 5秒的睡眠之后，再次调用同
- URL， 则会抛出KeEyrorr异常，也就是说缓存下载失效了。
3.2.缺5点
基于磁盘的缓存系统比较容易实现，无须安装其他模块，并且在文件管理
器中就能查看结果。但是，该方法存在一个缺点，即受制于本地文件系统的
限制。本章早些时候，为了将 URL 映射为安全文件名， 我们应用了多种限制，
483.数3据 库存缓
然而这又会引发另一个问题，那就是一些 URL 会被映射为相同的文件名 。比
如，在对如下几个URL 进行字符替换之后就会得到相同的文件名。
htpt://exarnpl.ecom?/a+b
•
htpt:I eIxa mpl.ec orn?/a* b
•
htpt:I eIx mapl.ec orn?/a= b
•
htpt://exarnpl.ecom?/a!b
•
这就意味着，如果其中一个 URL 生成了缓存，其他 3 个URL 也 会被认为
已经生成缓存，因为它们映射到了同一个文件名 。另外，如果一些长URL 只
在 255个字符之后存在区别，截断后的版本也会被映射为相同的文件名 。这
个问题非常重要， 因为 U虹 的最大长度并没有明确限制。尽管在实践中U肚
很少会超过200个0字符，并且早期版本的IE浏览器也不支持超过 208个3字
符的U虹。
避免这些限制的一种解决方案是使用URL 的哈希值作为文件名。 尽管该
方法可以带来一定改善，但是最终还是会面临许多文件系统具有的一个关键
问题，那就是每个卷和每个目录下的文件数量是有限制的。如果缓存存储在
FA3T2文件系统中，每个目录的最大文件数是65553。该限制可以通过将缓存
分割到不同目录来避免，但是文件系统可存储的文件总数也是有限制的。我
使用的 ex4t分区目前支持略多于1050万个文件，而一个大型网站往往拥有
超过 1亿个网页。很遗憾，DiskCcah方e法想要通用的话存在太多限制。 要
想避免这些问题，我们需要把多个缓存网页合并到一个文件中，并使用类似
B＋树的算法进行索引。 我们并不会自己实现这种算法，而是在下一节中介绍
己实现这类算法的数据库。
3.3数 据库缓存
为了避免磁盘缓存方案的己知限制，下面我们会在现有数据库系统之上创
49第3章 下载缓存
建缓存。爬取时，我们可能需要缓存大量数据，但又无须任何复杂的连接操
作，因此我们将选用NoSQL数据库，这种数据库比传统的关系型数据库更易
于扩展。在本节中，我们将会选用 目前非常流行的Mongo作D为B缓存数据库。
3.13 .NoSQ是L什么
NoSQ全L称为 Not SQL，是一种相对较新的数据库设计方式。传统
Only
的关系模型使用的是固定模式，并将数据分割到各个表中。 然而，对于大数
据集的情况，数据量太大使其难以存放在单一服务器中，此时就需要扩展到
多台服务器。不过，关系模型对于这种扩展的支持并不够好，因为在查询多
个表时，数据可能在不同的服务器中。 相反，NoQSL数据库通常是无模式的，
从设计之初就考虑了跨服务器无缝分片的问题。在 NoQSL中，有多种方式可
以实现该目标，分别是列数据存储 （如 HBa）s、e键值对存储 （如 Red）i、s面
向文档的数据库 （如MongoD）B以及图形数据库 （如Neoj4。）
3.3.安2装 MagnoDB
Mongo可DB以从 htpts://www.mo口gobd.rogd/ownload下s载得
到。然后，我们需要使用如下命令额外安装其Pytho封n装库。
pipi nsatllp ym ong＇。
要想检测安装是否成功， 可以使用如下命令在本地启动 MongoD。B
$ mong。d-dbpa位l .
然后， 在Pyth中o，n使用 Mongo的D默B认端口尝试连接 Mongo。DB
》＞ frmo pymongiomp orMton goClnite
=
》＞ clinet MonogCilent（l’oaclho’s，t27071)
33..3M ognoDB概述
下面是通过 MongDoB存取数据的示例代码。
5033. 数据库缓存
》＞ url＝ ’thtp://exapml.ewesbcrpain.cgom/vienwi/tU-eKdidnogm2-3’9
》＞ htm＝l ’ ． ． ． ’
》＞ db = clien.ctache
》＞ db.wepbag.eniser（t’｛rul’：ur，l’thml’：htm)l)
Object（i5d’510864c4e08c744l42ca75）’7
》＞ db.wepbag.eifndo n(erulu=r)l
{u一’id’ ：Obejct（i5d’581c046e407c4484cl727a’）5，
u’thm’l： u’ ． ．， ． ’
u’rul’： u’thtp:/e/xampl.ewesbcrapi.ncgomi/evwn/iUetd-Kigndo-m293’｝
上面的例子存在一个问题，那就是如果我们对相同的URL 插入另一条不同
的文档时，Mongo会D欣B然接受并执行这次插入操作， 其执行过程如下所示。
》＞ db.webapg.eniser（t’｛ rul’：ur，l’thml’：htm)l)
》＞ db.wepbag.eifn(durulr=l). ocun(t)
2
此时，同一URL 下 出现了多条记录， 但我们只关心最新存储的那条数据。
为了避免重复，我们将 ID设置为 URL， 并执行 upsetr操作。该操作表示
当记录存在时更新记录，否则插入新记录，其代码如下所示。
》＞ db.wepbag.uepdtae（ ’｛i＿d’ ：url),｛♀ ’set’：｛h’tml’：htm}l,}
upser=tTr)u e
》＞ db.wepbag.feind一0口e(｛ ’id’ ：url})
{u’i＿d': u’thtp://exapml.ewebscprian.cgom/view/
UniteKdi ndgom2-39’ ，uh’tlm’：u’． ．｝． ’
现在，当我们尝试向同一URL 插入记录时，将会更新其内容，而不是创
建冗余的数据，如下面的代码所示。
》＞ newh tml＝ ’h＜tm>l</ht＞ml’
》＞ db.wepbag.uepdtae（’｛id’ ：ur}l,｛ $’se’t ：｛h’tml’：new
htm}l,} upsert=Tr) ue
》＞ db.wepbag.eifndo ne（’｛id’ ：rul})
{u＿冒i’d： ’uthtp:/e/xampl.ewebscrapi.cnogm/evwi/nUited-nKgid-om239’ ，
uh’tml’：u’h＜tm>l</htm＞l’｝
》＞ db.wepbag.eifn（d ’｛id’ ：ur}l)c o.u n(t)
1
51第3章 下载缓存
可以看出，在添加了这条记录之后， 虽然 HTML的内容更新了， 但该 URL
的记录数仍然是 1 。
Mongo官D方B文档可参考htpt:I/ doc.som ngbo.do rg/l
manaul／，在该文档中可以找到上述功能及一些其他功能更 I
详细的介绍． I
3.3.M4o gnoDB缓存实现
现在我们己经准备好创建基于Mongo的D缓B存了， 这里使用了和之前的
DiskCahce类相同的类接口 。
fromd ateitmei mpordta tiemt,e timedleta
frmo pymongoi mp。rMtongloieCnt
clasMs。 ngoC:ache
def一＿i口i一一t（eslfc,leintN=on,e expir=etsmieedlt(aadys0=)3) :
# ifa clien。tb ejctisn otp asstehde tnr y
# concnteintgo m ongobd att hed efaullto calhpoosrtt
sel.cflien=t M ongloiCnet（l’ochaoslt’ ，270)1 7
ifc lienits N 。neelscel inet
# creacte。 llteicotnos tore cawecbhapegdse ,
# which ist hee quivaleonfat t able
# ina relantailod atbaase
sel.fbd =c lien.ctahce
# creaitne detxo e xpircea chweedb pasg e
self.db.ewbpa.gcereaitned e（xt ’imes tamp’ ，
expriefAteroSnedc=sepxiers.totaslec ond(s))
def gettie_m(selfu,r )l:
””Lo”adv aluaet t hsi URL
reco=r dsel.fbd.ewbpag.feind_one（ ’｛＿id’：ur}l)
ifr ecdo:r
returrne cd。［r’resu'l)t
els:e
raisKeeE yrro(rrul＋ ’doesn ot setx’ i）
5233. 数据库存缓
def seteimt (eslfu,r ,l restu)l:
””Sa”vev alufeo rt hsi URL
reco=r d r｛e’su’l：tr esu，ltt’ imest amp’ ：
datiemt.etucno(w})
sel.fbd.wepbag.epudat（e’｛i＿d’ ：ur}l,｛ $’se’t ：reco}r, d
upsert=Tr) ue
在上一节讨论如何避免冗余时， 你已经见过这里的 getitem和
settiem 方法的实现了。 此外，我们在构造方法中创建了timestamp
索引。在达到给定时间戳一定秒数之后，Mongo的D这B一便捷功能可以自动
删除记录。这样我们就无须再像 DisCkahce类那样，手工检查记录是否仍
然有效了。下面我们使用空的 timedelta对象进行测试，此时记录在创建
后就会被立即删除。
》＞ cach=e M onCga。ch(exepirse=itmeldte(a))
》＞ resu＝lt｛ h’tml’： ．．’’．｝
》＞ cach[erul] r=e sult
》＞ cach[erul]
｛h’tml’ ：’．’．．｝
记录还在这里，看起来好像我们的缓存过期机制没能正常运行。但实际上
这是Mongo的D运B行机制造成的。MonogDB运行了一个后台任务，每分钟
检查一次过期记录， 所以此时该记录还没有被删除。让我们再等 1 分钟，就
会发现缓存过期机制己经运行成功了 。
》＞ importtim e; tiem.sleep(06)
》＞cach[erul]
Trcaeabck( omstr ecnetc allla s:t )
KeyrErro：’thtp://exmapl.weesbcrapi.ncgom/view/Unidt。em2d-3-9King
doesn ot setx’ i
这种机制下，Mongo缓D存B无法按照给定时间精确清理过期记录，会存
在至多 1分钟的延时。不过，由于缓存过期时间通常设定为几周或是几个月，
所以这个相对较小的延时不会存在太大问题。
53第3章 下载缓存
3.3.压5缩
为了使数据库缓存与之前的磁盘缓存功能一致，我们最后还要添加一个功
能：压缩。其实现方法和磁盘缓存相类似，即序列化数据后使用 zlib库进
行压缩，如下面的代码所示。
imporpti ckle
imporztl bi
frmo bso.bninarimyp orBti nary
clasMson goCa:c he
def getimt e(eslfu,r )l:
reco=r dself.bd.ewbpag.eifnd_one（ ’｛i＿d’ ：ur)l)
ifr ecdo:r
reutrnp ick.lloead(szilb.decompress(ercodr['resu’l］t） ）
els:e
raisKeeE yrro(rrul＋ ’doesn ote xsit『 ）
def settiem (eslfu,r ,l restu)l:
=
record{
’resu’l：Bti na(rzyilb.copmres(spic.kdluemsp(erslut)),)
’itmset map：’dateitm.etucn。(w)
sel.fbd.ewbpag.epudat(e
｛＿’id’ ：url)｛,$ ’se’t ：reco)r,du psert=Tr) ue
3.3.缓6存 测试
MongoChae类c的源码可以从htpts://bibtucket.orgs/wpw/coed/
src/tpi/chpatre0/3mongcoac h.eyp获取，和 DiskCahce一样， 这
里我们依然通过执行该脚本测试链接爬虫。
$ timep yth。mn。ng＿。cahce.yp
http://example.webscrpainq.ocm
htpt://xea:i呼le.webscrapin.qcom/view/Anfiqshatan-1
http://ex四1ple.webscrapin.qc om/veiw/Zimb曲，we-252
23m40.302s
5434.
本章小结
$ ti皿e pythm。。nng＿。cahce.yp
0.738s
可以看出，加载数据库缓存的时间几乎是加载磁盘缓存的两倍。不过，
MongoBD可以让我们免受文件系统的各种限制，还能在下一章介绍的并发爬
虫处理中更加高效。
3.4本章小结
本章中，我们了解到缓存己下载的网页可以节省时间，并能最小化重新爬
取网站所耗费的带宽。缓存的主要缺点是会占用磁盘空间，不过我们可以使
用压缩的方式减少空间占用。 此外， 在类似 Mongo等D现B有数据库的基础之
上创建缓存，可以避免文件系统的各种限制。
下一章，我们会为爬虫添加并发下载多个网页的功能，从而使爬虫运行得
邮
更快。
电
55第 4 章
并发下载
在之前的章节中，我们的爬虫都是串行下载网页的，只有前一次下载完成
之后才会启动新下载。在爬取规模较小的示例网站时，串行下载尚可应对，－
但面对大型网站时就会显得捉襟见肘了。在爬取拥有 100万网页的大型网站
时，假设我们以每秒一个网页的速度昼夜不停地下载，耗时也要超过 11天。
如果我们可以同时下载多个网页，那么下载时间将会得到显著改善。
本章将介绍使用多线程和多进程这两种下载网页的方式，并将它们与串行
下载的性能进行比较。
41. 100万个网页
想要测试并发下载的性能，最好要有一个大型的目标网站。为此，本章将
使用 Alex提a供的最受欢迎的 100万个网站列表，该列表的排名根据安装了
Ale工xa具栏的用户得出。尽管只有少数用户使用了这个浏览器插件，其数据
并不权威，但对于我们这个测试来说已经足够了。
我们可以通过浏览 Alxea网站获取该数据，其网址为 htt:p//www.
alex.acorn/otpsitse。 此外，我们也可以通过 htpt://s.3rnaazonaw.s
corna/leax-sttica/otp-rnl.csv.zpi直接下载这一列表的压缩文件，
这样就不用再去抓取Alxea网站的数据了。第4章 并发下载
41.1. 解析 Aelx列a表
Alex网a站列表是以电子表格的形式提供的，表格中包含两列内容，分别
是 排 名 和 域 名 ， 如 图 4 .1 示所 。
A B
1 l go !og e E_. o m
－
2f acboeokc.om
2
→3 3youtu国c.om
4·－
4y到� .OC!l_l
一
5baidu.com
5
－ － 旦旦i � i ped i o .� r g.
67 7
－ amazon. coπ1
8twi忧er.com
8
－－ 9t a.obao.com
9 lOqq om
c
m 图 4 .1
抽取数据包含如下4个步骤。
下载.zpi文件。
从.zpi文件中提取出csv文件。 2 .
3. 解 析 c s v文 件 。
遍历 csv文件中的每一行，从中抽取出域名数据。 4 .
下面是实现上述功能的代码。
imporcts v
frmo zipfiilmpeo rZti pFile
frmo StringimIpOo rStt rnigIO
frmo donwloader imporDto nwloader
=
D Dowlno daer( )
=
z pip d_e=s atd a D '( ptht /: / .s zaam3 no a .w sc o am l/ e sx ta -t a i c /o p -lt .m vcs z. ip ’）
u r l [ #] t o p 1 m li il o LR Un ’ sw li bl e s ot r e di n t ih s l i s t
witZhi pFil(Setrin(gzIpiOpedd aat)) asz f:
=
csvf ileanme zfn.a emli(s)t[ 0]
5841. 100万个网页
for, websitien c s.vread(efzr.poe(nscvf ielnmae)) :
url.asppe（nhd’ttp：／／’＋ websit)e
你可能已经注意到，下载得到的压缩数据是在使用 StrinIgO封装之后，
才传给 ZipFlie的。这是因为ZpiFlie需要一个类似文件的接口， 而不是
字符串。接下来，我们从文件名列表中提取出csv文件的名称。 由于这个.zpi
文件中只包含一个文件， 所以我们直接选择第一个文件名即可。然后遍历该
csv文件，将第二列中的域名数据添加到 URL 列表中。为了使 URL合法，
我们还会在每个域名前添加 htpt：／／协议。
要想在之前开发的爬虫中复用上述功能，还需要修改scrapecallback
接口。
clasAsl exalCbaaklc:
def init( eslfm,a xu rl=slO)OO:
sel.famxu rl=sm axu rls
selfs.eeudr l＝ ’thtp://s.a3mzaonaw.socm/aelxas-ttaic/
top-ml.cs.vzip ’
def call( eslfu,r ,l htlm):
ifu rl= =s elfs.eeudr :l
url=s [)
wiht ZipFil(etSring(IthmOl)) asz f:
csvf ielnmae= zf.namleis(t[)O J
for, websitien
cs.vread(efzr.poe(nscvf ielnmae)) :
urls.apepn（dh’ttp：／／’＋ websi)t e
ifl e(nulrs)= =s el.famxu rl:s
break
returunr ls
这里添加了一个新的输入参数maxurl，s用于设定从Ale文xa件中提取
的 U虹 数 量。默认情况下，该值被设置为 100个0U旺 ， 这是因为下载 100
万个网页的耗时过长 （正如本章开始时提到的，串行下载需要花费超过1天1
的时间）。
59第4章 并发下载
4.2串 行爬虫
下面是串行下载时，之前开发的链接爬虫使用AlexalClbaac回k调的
代码。
scrapcea llback= AleCxaallb(a)ck
lin_ckraewrl(ese_durlc=rspae_callba.cekse_dur,l
cahcec allbakc=oMngohCea(c,)
scrapec_allbak=cscpreac_alblack)
完整源码可以从 htpts://bitbucket.org/pw/scwoed/rsc/pt/i
chpater4/0sequent＿itaes工t.yp获取，我们可以在命令行中执行如下
命令运行该脚本。
$ timep ythons equenti_atlest.yp
26m41.41ls
根据该执行结果估算， 串行下载时平均每个URL需要花费16.秒。
4.3多 线程爬虫
现在，我们将串行下载网页的爬虫扩展成并行下载。需要注意的是，如果
滥用这一功能，多线程爬虫请求内容速度过快，可能会造成服务器过载，或
是 IP地址被封禁。为了避免这一问题，我们的爬虫将会设置一个 dela标y
识，用于设定请求同一域名时的最小时间间隔。
作为本章示例的Alex网a站列表由于包含了 100万个不同的域名， 因而不
会出现上述问题。但是，当你以后爬取同一域名下的不同网页时，就需要注
意两次下载之间至少需要 1 秒钟的延时。
604.3多 线程爬虫
43.1. 线程和进程如何工作
图 4.所2示为一个包含有多个线程的进程的执行过程。
进程
窗
E
’
－
图 4.2
当运行 Pytho脚n本或其他计算机程序时，就会创建包含有代码和状态的
进程。这些进程通过计算机 的一个或多个CPU来执行。不过，同一时
CPU只会执行一个进程，然后在不同进程问快速切换，这样就给人以多个程
序同时运行的感觉。同理，在一个进程中，程序的执行也是在不同线程间进
行切换的，每个线程执行程序的不同部分。这就意味着 当－个线程等待网页
下载时－，进程可以切换到其他线程执行，避免浪费CPU时间。因此，为了充
分利用计算机中的所有资源尽可能快地下载数据， 我们需要将下载分发到多
个进程和线程中。
4.3.实2现
幸运的是，在 Pytho中n实现多线程编程相对来说比较简单。我们可以保
留与第 1章开发的链接爬虫类似的队列结构， 只是改为在多个线程中启动爬
虫循环，以便并行下载这些链接。下面的代码是修改后的链接爬虫起始部分，
这里把 crawl循环移到了函数内部。
61第4章 并发下载
importtim e
imp。rtthreading
frmo dowlnoadre imporDto nwl。aedr
SLEEPT IEM = 1
def threadceradw elr(. ., .ma xt hraed=sl)O:
# theq ueuoef U RL’tsh astt ilnle etdo bcer awled
craw14queue＝『LseeduEl、j
一 －
S＃ De e t n咱b e =D－－ u sR eL t’ ns t飞 ［ dsat ee－n ea r(dt u－n ara lv ］e b ee e n s e e R
o w l o c－ c I’h =h ce, a d cela=ydelay,
use_rag e nst e=_ruaegn,t proixesp=rxoie,s
numr ertiensu=mr etersi, timeoute=outti)m
def proscseq ueu(e:)
whileT ru:e
tr:y
url= crwalq ueu.epop()
excpetI ndexrErro:
# crawqlue uei se mpty
break
els:e
htm=l (Du r) l
下面是 thraededcrwaler函数的剩余部分，这里在多个线程中启动
了proecssqueu，e 并等待其完成。
thrdesa= []
whilet hraedso rc rwalq ueu:e
# thec rawils s tilalci tve
for thirenta hdr ea:d s
ifn 。t thdr.iesaa liev)( :
# removte hes tpopetdh reads
threa.dersmov(tehre)a d
whliel e(nhtraed)s m<a x_rtehadasn dc rawl_quue:e
# cans tarstom em orteh reads
thre=a dt hread.ihTnrgea(datrgetp=rocse_suqeu)e
# setda emsonom aint hrecaadn e xiwthe nr eceicvters-l c
thre.aesdtDaem(orTnu)e
thre.as dta(rt)
624.多3 线程爬虫
threa.dpaspen(dhtread)
# all threadbse ephnra ovscesee d
# sleept epmorarisl。CyP Ucanf 。cuesxeciuont elswehree
time.lsee(pSLE_ETIPME))
当有URL 可爬取时，上面代码中的循环会不断创建线程，直到达到线程
池的最大值。在爬取过程中，如果当前队列中没有更多可以爬取的URL 时，
线程会提前停止。假设我们有2 个线程以及2个待下载的URL。当第一个线
程完成下载时，待爬取队列为空，因此该线程退出。第二个线程稍后也完成
了下载，但又发现了另一个待下载的 URL。 此时 thraed循环注意到还有
URL 需要下载，并且线程数未达到最大值，因此又会创建一个新的下载线程。
对 thraeddecrwaler接口的测试代码可以从htpts://bibtucekt.
org/pw/scwoed/scr/tpi/hcaptre04/threeadd stt.epy获取。 现
在，让我们使用如下命令，测试多线程版本链接爬虫的性能。
$ timep y由。nthread二etd:est.yp 5
4m50.645s
由于我们使用了 5个线程，因此下载速度几乎是串行版本的5 倍。在 4.4
节中会对多线程性能进行更进一步的分析。
4.3.多3进 程爬虫
为了进一步改善性能，我们对多线程示例再度扩展，使其支持多进程。目
前，爬虫队列都是存储在本地内存当中，其他进程都无法处理这一爬虫。为
了解决该问题，需要把爬虫队列转移到Mongo当DB中。单独存储队列，意味
着即使是不同服务器上的爬虫也能够协同处理同一个爬虫任务。
请注意，如果想要拥有更加健壮的队列，则需要考虑使用专用的消息传输
工具，比如 Ceryl。e不过，为了尽量减少本书中介绍的技术种类，我们在这
里选择复用Mongo。DB下面是基于MonogDB实现的队列代码。
63第4章 并发下载
frmo dateitmei mpordta tiemt,e tiemdleta
frmo pymongoi mportM onCgloien,t errors
clasMson goQuee:u
# possibles tatoefsa donwload
OUSTTA ND工,NGPROECSISN,G COMPLE=T rEang(e3)
def init( eslfc,l eint=N,o tnimeeou3t0=)0:
selfc.lien=t M 。nogCilent()ifc lienti sN oneel sceli ent
sel.fbd =s el.flc inet.cache
sel.tfimeout= timeout
def 口。zneor (eslf:)
”吨”eturnTsruief t heraer em orej obst op roscse
reco=r ds elf.bd.crawl_qeuu.eifn一d。口e(
｛s’tatu’s： ｛♀’ne’：selfC.OM PLE}T}E
retuTrrnu ief r ecoerld sFeal se
def push(eslfu,r )l:
”””Addn ewU RL qtuoe uei fd oesn ote xsit
tr:y
sel.fdbcr.awl_qeuu.einse（r’｛ti＿ d’ ：ur，l’tsatu’s：
sel.Of USTTANDIN}G)
excepetr ro.DrupslciateEKreyroars e :
pas#s t hsi isa lrdeyai nt heq ueue
def pop(e slf:)
”””Geta no uttsandiUnRgLf rom qtuheeu ea nds eti ts
statsu top roecsisn.g工ftheq ueuei se mptya KeEyrr。r
excpetion isr asied.
reco=r ds el.fdbcr.wal_qeuu.eifnd andm odfiy(
query＝｛s’tatu’s：sel.fUOTSATNDIGN},
updtae＝｛’s♀e’t： s｛ta’tu’s： selfP.ROECSISN,G
’times tmap’ ：dat etmie.n o(w}) }
644.多3 线程爬虫
ifr eco:r d
returrne co［r’di d' ]
els:e
self.r epra( i)
rasieK eEyrro(r)
def coprnlet(eeslfu,r )l:
sel.df b.c rwalq ueu.eu pdtae(｛ ’id’ ：ur)l, ｛$’set’ ：
｛s’tat’u：ss el.Cf OMPLE)T)E)
de手ιrePa’r（se14在牛）·
”””R el －－－e aseS· ←」 a 14 14 e d「」·0 bqM
reco=r dsel.fdbr.awcl_qeuu.eifnd_an_rndodfiy(
query{=
’itmset map：’｛$’lt' :da teitrn.eonw（） 一
tirneedlt(saecnods=sfet.lirneout}),
’stat’u：s｛ ♀’ne’ ：sel.fOCMPELT}E
updtae＝｛’丰set’： ’｛tsatu’s：self.UTOSATND工GN}}
ifr eco:r d
print’Releas：e，’dr ecor［d’ id’］
上面代码中的队列定义了 3种状态： UOTTSADNING、PROCESISNG和
COMPLET。E当添加一个新 URL时，其状态为 OUSTTANDING： 当URL从
队列中取出准备下载时，其状态为 PROCESSNIG； 当下载结束后，其状态为
COMPLET。E该实现中 ，大部分代码都在关注从队列中取出的 URL无法正
常完成时的处理，比如处理 URL的进程被终止的情况。为了避免丢失这些
URL的结果，该类使用了一个 timeout参数，其默认值为 300秒。在
reapi（r）法方中，如果某个 URL的处理时间超过了这个 timeou值t，我
们就认定处理过程出现了错误，U虹 的状态将被重新设为 OUTSTADNING,
以便再次处理。
为了支持这个新的队列类型，还需要对多线程爬虫的代码进行少量修改，
下面的代码中已经对修改部分进行了加粗处理。
65第4章 并发下载
def threadcerwdal er(. .).:
# theq ueueo fU RL’s thastt ilnle etdo b ec rawled
craw_lqueue = Mong。Que(u)e
craw_lqueue.push(ese_durl)
def proscseq ueu(e:)
whlieT ru:e
# keetpr actkh aatr ep roscsenigu rl
tr:y
url= crawqlu eu.eop p()
excepKte Eyrr:o r
# currenntolu yr ltso p roscse
break
els:e
craw_lqt且eue.ocmpleet(ur)l
第一个改动是将 Pytho内n建队列替换成基于 Mongo的D新B队列，这里
将其命名为 MongoQue。eu由于该队列会在内部实现中处理重复 URL 的问
题，因此不再需要see变n量。最后，在 URL 处理结束后调用 complet(e)
方法，用于记录该U肚 己经被成功解析。
更新后的多线程爬虫还可以启动多个进程，如下面的代码所示。
impormtu ltpiroscseing
def proscse_iln_kcrlawe(rrag,s **wkar)gs:
口u_mcpus= multpiroscsein.gcpuo_cunt()
prin’ttSarti{n}gp roecss’efs.orma(ntu_mcpu)s
proecsse=s []
fori irna ng（ue口mcpus) :
p =m ultiprsosicne.grPocses(targehtr=aetde_dcrawelr,
arg[sr=ag]s,kw argsw=arkg)s
p.sta(rt)
proscsees.papen(dp)
# waifto rp roecssetsoc opmlete
forp inp roecss:e s
p.joi(n)
664.性4能
这段代码的结构看起来十分熟悉， 因为多进程模块和之前使用的多线程模
块接口相似。这段代码中首先获取可用 CPU的个数，在每个新进程中启动多
线程爬虫，然后等待所有进程完成执行。
现在，让我们使用如下命令，测试多进程版本链接爬虫的性能。 测试
proscesl inkc rwaler的接口和之前测试多线程爬虫时一样，可以从
htpts://bibtucekt.org/wpw/scoed/scr/tip/hcapetr04p/roec
sst est.yp获取。
$ timeP Y位1。pnr。cses_test.yp 5
Starting2 proecsses
2m5.045s
通过脚本检测，测试服务器包含 2 个CPU，运行时间大约是之前使用单
一进程执行多线程爬虫时的一半。在下一节中，我们将进一步研究这三种方
式的相对性能。
4.4性能
为了进一步了解增加线程和进程的数量会如何影响下载时间，我们对爬取
1000个网页时的结果进行了对比，如表4.所1示。
表4.1
脚本 线程数 进程数 时间 相对串行的时间比
串行 28分5.99秒66
5 7 分l16.3秒4 4.03
多线程
10 3 分50.秒455 7.55
多线程
20 2分544.1秒2 1.052
多钱程
5 2 4分22.46秒 71.7
多进程
10 2 2 分.414秒5 1.433
多进程
20 2 l 分476.6秒3 16.16
多进程
67第4章 并发下载
表格的最后一列给出的是相对于串行下载的时间比。 可以看出，性能的增
长与线程和进程的数量并不是成线性比例的，而是趋于对数。比如，使用 1
个进程和 5个线程时，性能大约为串行时的4倍，而使用 20个线程时性能只
达到了串行下载时的10倍。虽然新增的线程能够加快下载速度，但是起到的
效果相比于之前添加的线程会越来越小。其实这是可以预见到的现象，因为
此时进程需要在更多线程之间进行切换， 专门用于每一个线程的时间就会变
少。此外，下载的带宽是有限的，最终添加新线程将无法带来更快的下载速
度。因此，要想获得更好的性能，就需要在多台服务器上分布式部署爬虫，
并且所有服务器都要指向同一个 Mongo队D列B实例。
4.5本章小结
本章中，我们介绍了串行下载存在瓶颈的原因，然后给出了通过多线程和
多进程高效下载大量网页的方法。
下一章中，我们将介绍如何抓取使用JavcarpSit动态加载内容的网页。
68第 5 章
动 态内 容
根据联合国全球网站可访问性审计报告，73%的主流网站都在其重要功能
中 依赖 JvaaSrcpit 参（考 htpt://www.nu.rog/essao/cdev/ebnla/e
docuemnts/xeecsmunomens.aodc。）和单页面应用的简单表单事件不同，
使用 JvaacSrpit时，不再是加载后立即下载所有页面内容。这样就会造成许多
网页在浏览器中展示的内容不会出现在 H刊.f L 源代码中，本书前面介绍的抓
取技术也就无法正常运转了。对于这种依赖 JavaScrpit的动态网站，本章将会
介绍两种抓取其数据的方法，分别是：
JvaaScrpti逆向工程：
•
· 渲染 JvaaScrpti。
51. 动态网页示例
让我们来看一个动态网页的例子。 示例网站有一个搜索表单，可以通过
htpt://exampl.eewbscrapin.gocm/searhc进行访问，该页面用于查
询国家。比如说，我们想要查找所有起始字母为 A的国家，其搜索结果页面
如图5.所1示。第 5章 动态内容
Name: IA
Pages i'ze: 10 ’
�
A旬hani瞌s叫tIasnlands
． 阳nia IG 阳 a
C! AmeriScaamnIo 唱aAn伽 a
圄 坷。＇la 矗田 间ulila
噩噩 Anictaarc曰t阳taiBngdau rabuda
<P『vieiouINs ext>
图 5.1
如果我们右键单击结果部分， 使用 Frieb查ug看元素 （参见第 2章〉，可
以发现结果被存储在 ID为 “resu”l的tdi元v素 中，如图52.所示。
让我们尝试使用 lxml 模块抽取这些结果， 这里用到的知识在第2 章和第
3 章的 Dow川oaedr 类中都已经介绍过了。
》〉 工mportlxml.html
》＞ fromd ownolader工mportDownolader
=
》＞ D D =ow nloade()r
》〉 html D（h’ttp://exmaple.webscpr工a口gc.om/searc『h）
=
》＞ tree lxml.hmtl.fromsrting(html)
》＞ tree.csssele（cd’ti v#ersultsa ’）
［］
705.1动 态网页示例
Nam:e IA
Pagsei z:e 10 咱．
Sea「ch
E僵
Agfhanistan AlanIdslands
II
Albania Algeria
Andαra
国国
ConsolL e 叮�JC SS ScirptD O咽 ’‘
曰＜divclass="ctoanin「e”〉
回＜headerclass="amstheader「ow"i"d＝“heard'"e"
曰＜secitonid＝”ma‘icnl＇as=s"aminr m•">
曰＜divclas气sp＝an2!">
因＜fOrll"l"
曰＜div工d="resutls与
曰＜ta'ble>
曰＜tbody,.
巳＜t�
巳 «td>
日＜div>
..,.iTl王u�irmr;:霄，虽lihr.1o1I:毫缸，..，，...，＿
</diV>
</td>
自<td>
</rt>
南＜t�
图 5.2
这个示例爬虫在抽取结果时失败了。检查网页源代码可以帮助我们了解抽
取操作为什么会失败。在源代码中，可以发现我们准备抓取的 div元素实际
上是空的，如下所示。
<divi d＝”results”〉
<Id工>v
71第5章 动态内容
而 Frieugb 显示给我们的却是网页的当前状态，也就是使用 JvaaScrpit动
态加载完搜索结果之后的网页。下一节中，我们将使用Fierbgu的另一个功能
来了解这些结果是如何加载的。
什么是 AJAX
AJXA是指异步JavaS和cXriMLpt(A synchrJoanvoauSsanc dr ipt
X孔1L）， 于200年5引入，描述了一种跨浏览器动态生成Web应
用 内容的功能。更重要的是，XMLHtptReques－一t 这个最
呼 初微软 为 Acti实v现e的XJavaS对c象r，i目p前t已经得到大多数
叫器 时该 技术九许叫“叫到 础服务器的 时
请求并获得响应，也就是说Web应用就可以传输和接收数据。
而传统的客户端与服务端交互方式则是刷新整个网页，这种方式
的用户体验 比较差， 并且在只 需传输少量数据时会造成带 宽浪费。
Goog的lGemia和lGoog地l图e是动态Web应用的早期实验者，
也对AJA成X为主流起到了重要帮助。
5.2对 动态网页进行逆向工程
到 目前为止，我们抓取网页数据使用的都是第2 章中介绍的方法。但是，
该方法在本章的示例 网页中无法正常运行，因为该网页中的数据是使用
JvaaScrpti动态加载的。要想抓取该数据，我们需要了解网页是如何加载该数
据的，该过程也被称为逆向工程。继续上一节的例子， 在Friegbu中单击
Conosle选项卡， 然后执行一次搜索，我们将会看到产生了一个 AJA请X求，
如图5.所3示。
这个 AJAX数据不仅可以在搜索网页时访问到，也可以直接下载，如下
面的代码所示。
=
>>>h tml
D（ht’tp://example.webscarpin.gocm/aajx/
725.2对 动态网页进行逆向工程
searc.hjson?page&=pOages ize=Ol&esarcht erm=a’ ）
Name: r�
10 ’
Pa!gesi :z:e
Sea「ch
Afghanistan 盟嚣 AlandIlsands
- Alabnai Algena
C! American Andorra
- A叩l a 疆. A吨ui阳
�
lnspde Cle却 国国国
� r
HTML css Scrti p DOM
曰 CET闭�aocfsearc:h.json?'&se.arch_term=a&pages�ize剖01&,pa�:;e;O2on OK 晶
ParnmsH eadetrs R导sponseJSO'N
{. 「.eco「ds'":［｛回P「erty_linlk.：＂ 啊＜Clilv><a
href＝＼”／view/Afghanistna－！＼副＞＜img
src＝＼”／placesfst:atiimca/gesf/lags/af.pnrg\"/ >
Afgha,nist:a＜l"I／画＞＜／div＞”， ··仨ou1rnyt:＂： “Afg1hanitsa阳”，Hid锢：’
1261}.{ "p「etty_lin.k”：”＜div><a href＝飞副／view/Alaru:J-
1 I·sliands- .2飞··〉〈工mg
src＝飞’＇／apcle.s/statiimca/·gesf/lags/axp.nig＼”／＞ Aland
I I骂ilancls<a:/:></div.＞”，”cm.mt「Y”： ”Alandlslands剧， ＂id":
卫262》， f俑’P「etty_link”："<div><a href＝＼”／viei.i/Alb.ania-
3飞＂＞＜imgs「C＝＼回Ip1a 一一ces一/satt: i•C/i1 m:age s/flagIas ' l－阉[np g飞” ／：〉
Alba扪ia</a></div>
二
》＞·
图 5.3
AJA响X应返回的数据是JSNO格式的，因此我们可以使用Pytho的nj
son
模块将其解析成一个字典， 其代码如下所示。
73第 5 章动态内容
》＞ imporjts 。n
》＞ josn.lodas(thm)l
{u’erorr’： u” ，
un’ump agse’ ：22,
u’recdosr’ ：［{ uc’outnr’y：uA’fghasntain’ ，
u’di’：126,1
up’ret_tliyn’k：u’＜div>h<reaf ＝／”vi/eAwfgnhiasatn1-＞”＜img
sr＝c”／pleascs/ttaicm/aiegsf/la/gas.fnpg”／〉
Afhgainsatn/<a>/<div’＞，｝
］
．．．
现在，我们得到了一个简单的方法来抓取包含字母 A 的国家。要想获取
所有国家的信息，我们需要对字母表中的每个字母调用一次AJAX搜索。而
且对于每个字母，搜索结果还会被分割成多个页面， 实际页数和请求时的
size相关。保存结果时还会遇到一个问题，那就是同一个国家可能会
page
在多次搜索时返回，比如Fiij会匹配 f, ij,三 次搜索结果。这些重复的
搜索结果需要过滤处理，这里采用的方法是在写入表格之前先将结果存储到
集合中， 因为集合这种数据类型不会存储重复的元素。
下面是其实现代码，通过搜索字母表中的每个字母，然后遍历 JSON响应
的结果页面，来抓取所有国家信息。其产生的结果将会存储在表格当中。
·mpoE＋」·son
－ －
－ lmpo s tr －l n qd
E←」
t e pmlae t _url=
’ thtp://xeample.websrcapi.nocgm/aajx/
sear.csjho?npag{e&}=pa_gseize=&lsOecahr_rtme{='}
c。urnite=s se(t)
f。rlettienrs tri.lnogwesrce:a
page= 0
whlieT ru:e
html= Dt(epmlatuer .lforma(tapg,e letrt))e
tr:y
ajax= josn.load(tshm)l
745.2对 动态网页进行逆向工程
exceVpatl ueErarseo r:
prinet
ajax= None
els:e
forr ecorinda jax［r’ecrod’s ：］
couniter.sad(dercor[dc'ount’r］y）
pag+e= 1
ifa jaxi sN onoer p ag>e= a jax［口u’mpagse’：］
break
ope（nc’outnri.exstt’，’w）.’ rwit（e’n ＼’.jion(sort(ceodurnite)s) )
这个 AJAX接口提供的抽取国家信息的方法，比第 2 章 中介绍的抓取
方法更简单 。这其实 是一个日 常经验：依赖于AJAX 的网站虽然乍 看起来
更加复杂，但是其 结构促使数据和表现层分离 ，因此 我们在抽取数据时会
更加容易。
5.12 .边界情况
前面的 AJAX 搜索脚本非常简单，不过我们还可以利用一些边界情况使
其进一步简化。目前，我们是针对每 个字母执行 查询操 作的，也就是说 我们
需要26次 单独的查询，并且这些查询结果又有很多重复。理想情况下，我们
可以使用一 次搜索查询就能匹配 所有结果。接下来，我们将尝试使用不同字
符来测试这种想法是否可行。如果将搜索条件置为空，其结果如 下。
》＞ url=
’thtp://exmaple.wesbcrapi.nocgma/jax/
seahr.csjo?npgae=&Opgae_iszeO=&sleracht erm’＝
》＞ josn.lodas(D(ur)l［)n ’ump agse’ ］
。
很不幸，这种方法并没有奏效，我们没有得到返回结果。 下面我们再来尝
试’申 ’是否能够匹配 所有结果。
》＞ josn.lodas(D(rul＋ ＊’’ ）［）n’um_apge’s］
。
75第5章 动态内容
依然没有奏效。现在我们再来尝试下’ ·，这’是正则表达式里用于匹配所
有字符的元字符。
》＞ josn.lodas(D(ur＋l ’·’ ）［）n’u_mpagse’ ］
26
这次尝试成功了，看来服务端是通过正则表达式进行匹配的。因此，现在
可以把依次搜索每个字符替换成只对点号搜索一次了。
此外，你可能已经注意到在AJAX的 URL 中 有一个用于设定每个页面显
示国家数量的参数。搜索界面中包含 4、 01、2。这几种选工页， 其中默认值为
10因。此，提高每个页面的显示数量到最大值，可以使下载次数减半。
》＞ url=
’thtp://exmaple.ewbscrapi.nocgm/aajx/
seahr.cjons?paeg=&Opagsei ez=02&saerhc_etrm＝. ’
》＞ josn.lodas(D(ulr))［ n『umpagse’ ］
13
那么，要是使用比网页界面选择框支持的每页国家数更高的数值又会怎
样呢？
》＞ url=
’thtp://exmaple.wesbcrapi.nocgm/aajx/
seahr.cjons?paeg=&Opa_gseiz=elOOeOar&cs_hterm.＝ ’
》＞ js o.nl oad(s D(ru l) ［)n’u mp age’s］
1
显然，服务端并没有检查该参数是否与界面允许的选项值相匹配， 而是直
接在一个页面中返回了所有结果。 许多 Web应用不会在AJAX后端检查这一
参数，因为它们认为请求只会来自 Web界面。
现在，我们手工修改了这个 URL，使其能够在一次请求中下载得到所有
国家的数据。进一步简化之后，抓取所有国家信息的实现代码如下。
FIELD=S 'a( r e’a，’oppluatni’o’，sio’， c’onutr’y，cap’it’al，co’nitnen’t ，
’ltd’ ， cu＇rre_nc coyd’e， ’currenncamye’ ， ph’on’e， po’st_acloder_mftao’ ，
’opst_acl。_dreegxe’， l’anugage’s，ne’ihgborus’ ）
765.渲3染 动态网页
writ=e rcs.vwrite(rpoe（nc’ournite.sscv’，’’w ） ）
wrietr.wrirtoe(wIFEL)D S
htm=l D(ht'tp://exmpal.ewebscrpain.gocm/aajx/
seahr.cjons?paeg=&Opagseiz e=OlOOs&earcthe mr＝.’ ）
ajax= josn.lodas(thm)l
forr ecorinda jax［’recdosr’ ：］
=
row [recor[fdielfdo]r f ielidnF IEL]D S
wrietr.wrtierwo(orw)
5.3渲 染动态网页
对于搜索网页这个例子， 我们可以很容易地对其运行过程实施逆向工程。但
是，一些网站非常复杂，即使使用类似Firuge这b样的工具也很难理解。 比如，
一个网站使用GoogWleebT oolki(Gt W T）开发，那么它产生的JvaaScptr代i码
是机器生成的压缩版。生成的JaavScptr代i码虽然可以使用类似 JSbaeutifier
的工具进行还原，但是其产生的结果过于元长，而且原始的变量名也已经丢
失，这就会造成其结果难以处理。尽管经过足够的努力，任何网站都可以被
逆向工程，但我们可以使用浏览器渲染引擎避免这些工作， 这种渲染引擎是
浏览器在显示网页时解析 HTML、应用 css样式并执行 JvaaScri语严句的部
分。在本节中，我们将使用 WeKbi渲t染引擎，通过 Qt框架可以获得该引擎
的一个便捷 Pytho接n口。
什么是 Web.Kit?
WebKi的t代码源于 199年8的KHTML项 目，当时它是
Konqu浏e览r器o的r渲染引擎。2010年，苹果公司将该代码衍
生为WebK，it并应用于Sfaar浏i览器。Goog在lCehreo2m7
可
之前的版本也使用 了WebK内i核t，直到2013年转向利用
WeKbi开t发的Blnik内核。Ope在r2a00年3到2012年使用 的
是其内部的Pre渲s染to引擎， 之后切换到WeKbi，t但是不久
又跟随Chro转m向eBlnik.其他主流渲染引擎还包括IE使用
的Treind和tFrifoex 的Gec.ko
77第 5 章动态内容
5.13 .PyQ还t是 PySide
Qt框架有两种可以使用的 Pyth库o，n分别是 PyQt和 PyiSde。PyQt
最初于 1998年发布，但在用于商业项目时需要购买许可。由于该原因，开发
Qt的公司（原先是诺基亚，现在是 Dig）i后a来在200年9开发了另一个 Python
库 PyiSde， 并且使用了更加宽松的LGP许L可。
虽然这两个库有少许区别， 但是本章中的例子在两个库中都能够正常工
作。下面的代码片段用于导入已安装的任何一种 Qt库。
tr:y
fromP ySeiQ.dtGuiimp or*t
fromP yiSdeQ.tCoriemp or*t
fromP ySeiQ.dtWKeibti mp。r*t
excepItmp orrtrE。:r
fromP ytQ4.QtGuiimp 。r*t
frmo PytQ4.QtCroei mpor*t
frmo PytQ4.QteWbKiti mpor*t
在这段代码中， 如果 PySied不可用，则会抛出 ImportEr异r常o，r
然 后 导 入 PyQt模块 。如 果 PyQt模块也不可用 ，则会抛 出 另 －个
工mportrEror异常，然后退出脚本。
qt-proecjt.org/w/iSektiitn_gup_yPSdie和
htpt://pyq.tosurcfeogre.ent/oDc/sPyQt4/
instlaaltnih.o tm.l
5.3.执2行 JavaSpctri
为了确认WebKi能t够执行JavaptS，c我们ri可以使用位于htpt:/e/xampl.e
webscarpin.gocmd/yanmci上的这个简单示例。
785.渲3染 动态网页
该网页只是使用JavcarSi在pdti元v素中写入了HellWoorl。d下面是
其源代码。
<html>
<body>
<diivd ＝”erslut＞”＜／idv>
<sc pEt工>
•
docmuent.getlEemenytiB（dr”esu”l）ti nnerT＝e’xeHtl lWoor l’d ；
</csript>
</body>
</htm>l
使用传统方法下载原始HTML并解析结果时，得到的 di元v素为空值，
如下所示。
》＞ url＝ ’thtp://xeapml.ewebsrcapi.cnogmd/ynacm’i
=
>>>h tml Du(r)l
=
》＞ treel xml.thm.lfrmostrnig(thm)l
•
>>>t re.escsselec（t＃’resu’lt[） 0t eJx cto nte(n)t
下面是使用 WeKbi的t初始版本代码，当然还需事先导入上一节提到的
PyQt或 PySied模块。
=
》＞ app QAplpiactio( nJ[ )
=
>>>w ebivew QWebiVe(w )
=
》＞ loop QEveLnoto(p)
>>>w evbie.woladFinsihe.doc口ne(cltoop.uqi)t
》＞ wevbie.wola(dUQr(lulr))
>>>l oop.xeec( )
=
》＞ html webive.wp ag(e.)am ifnrmae(.)t oHmtl( )
=
》＞ treel xml.thm.lfrmostrnig(thm)l
》＞ tre.escssele（c＃’tresu’lt[） O .tJ excto nte(n)t
’eHllWoo rl’ d
因为这里有很多新知识，所以下面我们会逐行分析这段代码。
· 第一行初始化了QAplpicati对o象n，在其他 Qt对象完成初始化之
前，Qt框架需要先创建该对象。
79第5章 动态内容
· 接下来，创建 QWeVbie对w象，该对象是Web文档的容器。
· 创建 QEvnetoLo对p象，该对象用于创建本地事件循环。
QWebeViw对象的 lodaFinsihe回d调连接了 QEevntLpo的o
•
quit方法，从而可以在网页加载完成之后停止事件循环。然后， 将
要加载的URL传给 QWebVeiwoPyQ需t要将该U肚 字符串封装在
QUrl对象当中，而对于 PySied来说则是可选工页。
· 由于 QWebVie的w加载方法是异步的，因此执行过程会在网页加载
时立即传入下一行。但我们又希望等待网页加载完成，因此需要在事
件循环启动时调用 lopo.xeec（。）
· 网页加载完成后，事件循环退出，执行过程移到下一行，对加载得到
的网页所产生的HTML进行数据抽取。
· 从最后一行可以看出，我们成功执行了 JavcarpSti,div元素果然抽
取出了HelloWorldo
这里使用的类和方法在 C＋＋的 Qt框架网站中都有详细的文档，其网址为
htpt://qt-proejc.torgo/cd/tq-4 8.／。虽然 PyQ和tPyiSde都有其
自身的文档，但是原始C＋＋版本的描述和格式更加详尽，一般的Pytho开n发
者可以用它替代。
5.3.使3用 WebKi与t网站交互
我们用于测试的搜索网页需要用户修改后提交搜索表单，然后单击页面链
接。而前面介绍的浏览器渲染引擎只能执行 JavcarpSti， 然后访问生成的
HTML。 要想抓取搜索页面，我们还需要对浏览器渲染引擎进行扩展，使其
支持交互功能。幸运的是，Qt包含了一个非常棒的 AP，I 可以选择和操纵
HTML元素，使交互操作变得简单。
对于之前的 AJAX搜索示例， 下面给出另一个实现版本。该版本己经将
搜索条件设为’·，’每页显示数量设为’010’0，这样只需一次请求就能获取
805.渲3染 动网态页
到全部结果。
=
app QApplciatni(。[ )]
=
wevbiew QWeVbie(w)
=
工。op QEveLnoto(p)
webvi.eolwadFisnhie.cdoncnte(olo.puqi)t
wevbiwe.ola(dUQr（lh’ttp://exrnapl.eewbscrapi.nocgm/serac’h） ）
lopo.e xec( )
webevwi.s ho(w)
=
frmae webevwi.p ag(e.)arn inFrnre(a )
frrnae.ifnFdirEsltmeen（t＃’searhc temr’ ．）
seAtttrib（uv’atleu’e， ’ ．｝ ’
frrnae.ifndFirEsltmeen（t＃’pa_gseize opti:。cnheck’e．）d
setPnlTaeix（t’010’0）
frmae.findFrisEtlrneen（t＃’searh’c ．）
evaluaatveaJScprti（t’hsic.li（ck’） ）
ap.pxee一c（）
最开始几行和之前的 HellWoorld示例一样，初始化了一些用于渲染
网页的Qt对象。之后，调用 QWebVeiwGUI的 show（方）法来显示渲染窗口，
这可以方便调试。然后，创建了一个指代框架的变量，可以让后面几行代码更短。
QWebFmrea类有很多与网页交互的有用方法。接下来的两行使用cs模s式在框
架中定位元素，然后设置搜索参数。而后表单使用 evaluaJtaeavScprti()
方法进行提交，模拟点击事件。该方法非常实用，因为它允许我们插入任何
想要的JavcarpSti代码，包括直接调用网页中定义的JvaacSrpti方法。最后一
行进入应用的事件循环，此时我们可以对表单操作进行复查。 如果没有使用
该方法，脚本将会直接结束。
图 5.所4示为脚本运行时的显示界面。
1 .等待结果
实现WeKibt爬虫的最后一部分是抓取搜索结果，而这又是最难的一部分，
因为我们难以预估完成 AJAX事件以及准备好国家数据的时间。有三种方法
可以处理这一问题，分别是z
· 等待一定时间，期望AJA事X件能够在此时刻之前完成：
81第 5 章动态内容
· 重写 Qt 的网络管理器，跟踪 URL请求的完成时－间；
· 轮询网页，等待特定内容出现。
Exam1plwee b
scar1pinwgeb siet
M川袋“mM鼻
－nunun门v jl
F，‘p3’A
n「，mm
ιM
Serach
盟Z
灿ncJIsla咄
Albania ·"' Algeria
图54.
第一种方案最容易实现，不过效率也最低，因为一旦设置了安全的超时时
间，就会使大多数请求浪费大量不必要的时间。 而且，当网络速度比平常慢
时－，固定的超时时间会出现请求失败的情况。第二种方案虽然更加高效，但
是如果延时出现在客户端而不是服务端时‘，则无法使用。比如，已经完成下
载，但是需要再单击一个按钮才会显示内容这种情况， 延时就出现在客户端。
第三种方案尽管存在一个小缺点，即会在检查内容是否加载完成时浪费 CPU
周期，但是该方案更加可靠且易于实现。下面是使用第三种方案的实现代码。
825.渲3染 动态网页
》＞ elmeents= None
》＞ whlien ote lmeetns:
ap.pp roscsevEenst( )
elmeents= frmae.ifndAllElmeetns（＃’resulats’）
》＞ cournite=s [e.toPlnaTiex(t.)ts ri(p)f ore ine lmeent]s
》＞ princto utnries
[u’Afghiastna’n，uA’lanIds lnad’s，. .,. u ’Zambi’a ，u’izmb abwe’］
如上实现中，代码不断循环， 直到国家链接出现在 result这个s dvi元
素中。 每次循环，都会调用 ap.pproscseEev口t（s，）用于给 Qt 事件循环
执行任务的时间，比如响应点击事件和更新GU。I
2.渲染类
为了提升这些功能后续的易用性，下面会把使用到的方法封装到一个类
中，其源代码可以从htpts://hitbucekt.org/pw/scwoed/scr/tip/
chpatre05/brwoserre nedr.yp获取。
importtim e
clasBsr owrsReeenrd(WQebeVwi):
def init( eslfs,h o=wTr)ue:
self.app= QAppliactino(yss.argv)
QWeVbie.w init( eslf)
ifs ho:w
selfs.ho(w)# shotwh eb roewrs
def donwlaod(eslfu,r ,l timeo=u6t)0:
”””Waifto rd onwloadt oc ompletaen dr eturrne su”l”t”
loo=p Q EvnetLpo( o)
timer =Q Tirm( e)
tiemr.estSingSlheo(trTu)e
timer.timeou.tconne(coltop.quit)
selfl.oadiFnsihe.cdonne(c。lto.pquit)
sel.lf oda( UQr(lru l))
timer.tsar(ttimeout* 1000)
lopo.xeec( )# delayh eruen tild onwloafdi nsihed
83第 5 章动态内容
ift iemr.siActiv(e:)
# donwlodaeds ucscseuflly
tiemr.s tpo( )
retursne l.fthml()
els:e
# timedo ut
pritn’eRquesttim edo u：t’ ＋ur l
def htm(lesl)f:
””S”hortctuort e utrnt hec urreHnTtLM ”””
retursnel fp.ag(e.)m ainFmrea( .)t oHmtl( )
def fidn(eslfp,a ttne):r
””Fi”nda ll meenltest hamta tcthh ep atetrn”””
retursne l.fap g(e.)am iFnrmae( .)f indAllElmeent(sp atnt)e r
def att(reslfp,a tt口e，rname,valeu):
”””eSta ttirbutfeo rm atchienlmgee nt”s””
fore ins el.ffidn(patnt)e: r
e.etsAttribut(enmae, val)u e
def tex(teslfp,a ttne,rv aleu):
”””eSta ttirbutfeo rm atchienglm eent”s” ”
fore ins elff.in(dapttne)r:
e.etsPlaTienx(tavlu)e
def cli(cekslfp,a ttne):r
”””Climcakt chienlmgee nt”s” ”
fore ins elf.fin(dpatnt)e: r
ee.valuaatveaJScprti（”hti.scli（ck） ”）
def wailto da(eslfp,a tte,r tnimeo=u6t0:)
”””Waiutn itlp atteirsnf ounadn dr etumrant ch”es” ”
deaidnle= time.time()+ timeout
whilet ime.itm(e)< deadlin:e
selfa.p.prpocseEvsetns()
macthse =s el.ffidn(aptte)r n
ifm atcehs:
retumrant hces
prin’taWitl oda timedo u’t
8453. 渲染动态网页
你可能已经注意到，在 dowlnoad（ ） 和waitloa（d方） 法中我们增
加了一些代码用于处理定时器。定时器用于跟踪等待时间， 并在截止时间
到达时取消事件循环。否则，当出现网络问题时，事件循环就会无休止地
运行下去。
下面是使用这个新实现的类抓取搜索页面的代码。
=
》＞ br BrowrsReeenrd()
》＞ br.dowlnoad（h’ttp://exmaplew.ebsrcapi.nocgms/erac’h）
》＞ br.att（r＃’seahr tcemr，，’avlu’e， ’ ＇) I
》＞ br.tex（t＃’ pa_gseizeo pito:ncheck’e，’d0 100 ’）
》＞ hr.cli（c＃k’s earhc’ ）
=
》＞ elmeents hr.awitl oa（d＃’r esulat’）s
=
》＞ coutnries[ e.t oPlnaTiex(t.) tsri(p)f ore ienl meenst]
》＞printc outnries
[uA’fgnhaisatn’ ，uA’landI slnad’s ，..., u ’Zmabi’a ，u’imZbabw’e］
5.3.S4e lieunm
使用前面例子中的WeKbi库t，我们可以自定义浏览器渲染引擎，这样就
能完全控制想要执行的行为。 如果不需要这么高的灵活性，那么还有一个不
错的替代品 Senlieu可m以选择，它提供了使浏览器 自 动化的 API接 口 。
Sleneimu可以通过如下命令使用 pip安装。
pipi nsatlls elenium
为 了演示 Sleneiu是m如何运行的， 我们会把之前的搜索示例重写成
Senlimeu的版本。首先， 创建一个到浏览器的连接。
》＞ froms eleunmii mporwte bidrver
=
》＞ driverw ebidrvre.iFrfeo(x)
当运行该命令时，会弹出一个空的浏览器窗口 ，如图55.所示。
该功能非常方便，因为在执行每条命令时，都可以通过浏览器窗口来检查
85第5章 动态内容
Senlieu是m否依照预期运行。尽管这里我们使用的浏览器是 Frifoex， 不过
Senlieu也m提供了连接其他常见浏览器的接口，比如 Chro和meIE。 需要注
意的是，我们只能使用系统中己安装浏览器的Sleneiu接m口。
v…T功 叭＋
＇ 捆
记 ，＇
t fo 阳arch Vj争 品命 古i i自
ore nte甜r自由S =
面Most
Visit副V
…�－＇～－－…,.,,...－.....叫.,＿ 一，一�一…－一一－……一…………·？咿－；，.：－－「：·旦－…～町咿～「＿＿一
，�，�－「
图 5.5
如果想在选定的浏览器中加载网页，可以调用 get（ ）法方：
》＞ drirv.eegt（h’ttp://exarnpl.ewebscprian.gocms/earhc’）
然后，设置需要选取的元素，这里使用的是搜索文本框的 ID。 此外，
Sleneiu也m支持使用 cs选s择器或 XPa来th选取元素。当找到搜索文本框之
后，我们可以通过sendkeys（ 方）法输入内容，模拟键盘输入。
》＞ drievr.finde lmeenbty _id（ s’eahr_tcernr’ .）es n_dkey（s.＇）冒
为了让所有结果可以在一次搜索后全部返回，我们希望把每页显示的数量
设置为 1000。但是，由于Seelni的um设计初衷是与浏览器交互，而不是修改
网页内容，因此这种想法并不容易实现。要想绕过这一限制，我们可以使用
JavcarpSti语句直接设置选项框的内容。
865.渲3染 动态网页
•
》＞js＝” odcrnuetng.etEmlenetBdyi（’paeg_isz’e）o piton[ls ]. t ex＝t’1 000’”
》＞ drievr.execustcerpit(j;s )
此时表单内容已经输入完毕，下面就可以单击搜索按钮执行搜索了 。
•
》＞ drievr.findelmeenbty i d(s'earc’h） c li(ck)
现在，我们需要等待 AJAX请求完成之后才能加载结果， 在之前讲解的
WebK实i现t中这里是最难的一部分脚本。幸运的是，Senlieu为m该问题提供
了一个简单的解决方法，那就是可以通过 impliciytwlait（ 方）法设置超
时时间。
》＞ drievr.implici_twlayi(t30)
此处，我们设置了30秒的延时。如果我们要查找的元素没有出现，Senlieum
至多等待 30秒，然后就会抛出异常。要想选取国家链接，我们依然可以使用
WeKbi 示t例中用过的那个 css选择器。
=
》＞ links drievr.fidn elmeentsb yc sss eelct。（＃r’resulat’）s
然后，抽取每个链接的文本，并创建一个国家列表。
=
》＞ coutnries[l in.tkexfto rl inikn l in]k s
》＞ princto utnries
[uA’fgnhiasatn’ ，uA’lanIds alnd’s ，. .' .u’Z ambi’a ，u’Zimbab’w］e
最后，调用 clos（方e）法关闭浏览器。
》＞ drievr.c lo(se)
本示例的源代码可以从 htpts://bibtucekt.org/pw/scwdoe/scr/
tip/chaeprt05s/elneiums_eahr.cyp获取。如果想进一步了解 Selenium
这个时由on库，可以通过htpts://eslenmi-puyth.oernadthdeocs.org/
获取其文档。
87第5章 动态内容
5.4本章小结
本章介绍了两种抓取动态网页数据的方法。第一种方法是借助 Friegbu
Lit对e动态网页进行逆向工程，第二种方法是使用浏览器渲染引擎为我们触
发 JavcarpSti事件。我们首先使用WebK创i建t自定义浏览器，然后使用更高
级的Sleneuim框架重新实现该爬虫。
浏览器渲染引擎能够为我们节省了解网站后端工作原理的时间，但是该方
法也有其劣势。渲染网页增加了开销，使其比单纯下载HTML更慢。另外，
使用浏览器渲染引擎的方法通常需要轮询网页来检查是否已经得到事件生成
的 HTML， 这种方式非常脆弱，在网络较慢时会经常会失败。我一般将浏览
器渲染引擎作为短期解决方案，此时长期的性能和可靠性并不算重要：而作
为长期解决方案，我会尽最大努力对网站进行逆向工程。
在下一章中，我们将介绍如何与表单进行交互，以及使用 cooike登录网
站并编辑内容。
88第 6 章
表单交互
在前面几章中，我们下载的静态网页总是返回相同的内容。而在本章中， 我
们将与网页进行交互，根据用户输入返回对应的内容。本章将包含如下几个主题：
· 发送 POS请T求提交表单：
· 使用 cook登i录e网站：
· 用于简化表单提交的高级模块 Mechan。ize
表单方法
HTML定义了两种向服务器提交数据的方法， 分别是GET和
POTS使.用GET方法时，会将类似？nmael=valule＆口mae2
=value2的数据添 加到UR L中这，串数据被称为“查询字符串”。
由于浏览器存在UR L 长度限制，因il:l:.i主种方法只 适用于少量数据
£
的场景。另外，这种方法应当用于从服务器端获取数据，而不是
修改数据，不过开发者有时会忽斗取主一 规定。而在使用POS请T
求时，数据在请求体中发送，与 URL保持分离．敏感数据只应使
用POS请T求进行发送，以避免将数据暴露在URL中.POST
数据在请求体中如何表示需要依赖 于所使用的编码类型。
服务器端还支持其他HTT方P法，比如 PUT和 DELEET方
法，不过这些方法在表单中均不支持。第6章 表单交互
想要和表单进行交互，就需要拥有可以登录网站的用户账号。现在我们需
要 手 工 注 册 账号 ，其 网 址 为 htpt://exampl.eewbscrapin.cgom/
usere/grsite。r本章目前还无法 自动化注册表单，不过在下一章我们会介
绍处理验证码问题的方法，从而实现自动化表单注册。
61. 登录表单
我们最先要实施自动化提交的是登录表单，其网址为 htpt://exmaple.
webscarping.com/suerl/ogion要想理解该表单，我们需要用到 Friebug
Lit。e如果使用完整版的 Friegbu或者 Chrom的e开发者工具，我们只需要提
交表单就可以在网络选项卡中检查传输的数据。但是，Lit版e本限制我们只
能查看结构，如图61.所示。
‘•formac tion圃＝，• enctey="papp\icatio-n-/-xfonn-urtenc。ded"methdo="post•,.
臼‘tabl>e
二 <tbody＇’
国<trid="auth_s "uer 啕e帽ial_ro‘，.，’
•'!'<:t dc \as=s"•2p_fl＂：’
国＜td ca\ss=w2p fw">
<inputc lasss=t"irng• id="aut_huse＿r酬， ail•name =•帽eil• type="text• val四＝＂＂／＞
</td>
<tdc \ass="w2p_fc">/
</tf"
El <tr id="auths_eu_rp ass嗣rd_row'>
全 <tdc\ass= " w2_pf l">
国＜tdc\as=s"w2p_fw＂＇’
<inputc lass"=passwodr" id=a"uth_use_rp assword" na胁e="paswosrd"type筐•password"valu＝e凰”I>
</td>
<tdc las=s"w2p_cf’／＞
</tr>
习民<tr id=’authu ser r冒，ember 『OW">
副司「id="sblulitrecord r剧与
需／tbody’
</table>
Iii� divs tyt=e"dipsta:y noen；飞
〈且npuntame＝悦next”type四·”hidde•n’value相•l"i'>
<ipnut＂ ＂＇晴d for1 1key"t ype’”hidde刷nval四�·fdl55d3-38b8l－锦de-86f8-6m22b6bcd781γ，
叫咱 ut 阳配＝飞formna酣‘typ＝e川hdiden。valu＝e气咽in'/>
</diV>
</fo�
图61.
图61.中包括几个重要组成部分，分别是fomr标签的actni..eo.n cptey
和 metho属d性，以及两个input域。actoin属性用于设置表单数据提交
的地址， 本例中为＃，也就是和登录表单相同的URL。 nectype 属性用于设置
9061. 登录表单
数据提交的编码，本例中为appliactionw/wwx-f-orm-urlceonedd。 而
metho属d性被设为 pots， 表示通过请求体向服务器端提交表单数据。对于
input标签，重要的属性是name， 用于设定提交到服务器端时某个域的名称。
表单编码
当表单使用 POST方法时，表单数据提交到服务器端之前有两
种编码类型可供选择。 默认编码类型为 applicatino/x­
www-form-urelncoedd，此时所有非字母数字类型的字
符都需要转换为十六进制的ASCII值。 但是，如果表单中包含
� 大量非字母数字类型的字符时， 这种编码类型的效率就会非常
低，比如处理二进制文件上传时就存在该问题，叫需要定
义multipartf/omr-data作为编码类型。使用这种编码
类型时，不会对输入进行编码， 而是使用MIME协议将其作为
多个部分进行发送，和邮件的传输标准相同。
该标准的官方文档 为http ://www.w3.o rg/TR/h mtl 5/
fomrs.thml#sleecitng-aform-submsisoin­
encodi。ng
当普通用户通过浏览器打开该网页时，需要输入邮箱和密码，然后单击登
录按钮将数据提交到服务端。如果登录成功，则会跳转到主页：否则，会跳
转回登录页。下面是尝试自动化处理该流程的初始版本代码。
》＞ imporutr lbl,iu rlilb2
》＞ LOGI_NURL＝ ’thtp://exrnaple.websrcapin.gocmu/selro/g’i n
》＞ LOIGN_EMAIL＝ ’xearnpl@ewesbcrapi.nocgm’
》＞ LOGI_NPASSWORD＝ ’xeample’
》＞ dat＝a ｛e’mail’ ：LOG_IENAMIL，’apsswor’d：L OIGN_PASSWOR}D
》＞ ence。dddat=a urlbl.uirelnocd(eadt)a
》＞ reuqes=turllib2.eRques(tOLGINU R,L encdoedd ata)
=
》＞ respnose urllib2.urlp。e(nerquets)
》＞ respoeng.setu(r)l
’thtp://exrnpal.ewesbcrapi.nocgm/suerl/og’i n
91第6章 表单交互
上述代码中，我们设置了邮箱和密码域，并将其进行了urleondec编码，
然后将这些数据提交到服务器端。当执行最后的打印语句时，输出的依然是
登录页的U阻，也就是说登录失败了。
这是因为登录表单十分严格，除邮箱和密码外，还需要提交另外几个域。
我们可以从图61. 的最下方找到这几个域，不过由于设置为 hidden， 所以不
会在浏览器中显示出来。为了访问这些隐藏域，下面使用第2章中介绍的工xml
库编写一个函数，提取表单中所有 inpu标t签的详情。
imporltxm l.html
def parsfeo mr(thml):
tre=e l xml.thm.lfrmostrnig(thm)l
data= { }
fore int re.escsesle（cft’o mr input') :
ife .egt（ n’ame’：）
dat[ea.etg（na『m’e]） = e.egt（’ avlu’e）
returdna ta
上述代码使用 lxml的 css选择器遍历表单中所有的妇put标签，然后
以字典的形式返回其中的name和 valu属e性。对登录页运行该函数后， 得
到的结果如下所示。
》＞ imporptp rint
》＞ htm=l urlbl2i.urlpoe(nOLGIN_)U. RerLa(d)
》＞ fomr =p ar_sfeomr(thm)l
》＞pprin.tpprin(tform)
’nex’t： ’／’，
’ ofrmkey’： 0『29lec-69533422e-6-b6a-ld97bb3la22’f8，
’ ofrmnam＇e：’olgni’，
’meail’： ”，
’apsswor’：d ”
’reemmber’ ：’口。’
其中， fo rmkey属性是这里的关键部分，服务器端使用这个唯一的ID
来避免表单多次提交。每次加载网页时，都会产生不同的ID， 然后服务器端
9261. 登录表单
就可以通过这个给定的 ID来判断表单是否己经提交过。下面是提交了
fo rmkye及其他隐藏域的新版本登录代码。
》＞ htm=l urlbl2i.u rlpoe(nO LGIUNR )L r.e a(d)
》＞ data= parsfeo mr(thm)l
》＞ dat［ae’m ail’ ］= LO工GNEMAIL
》＞ dat［ap’ asswor’d］= LOIGNP ASSWORD
》＞ encoddeadt=a urllbi.urelnceo(dadt)a
》＞ reqsute= urllib2.Reuqes(tOLGINU R,L enceoddd ata)
》＞ resnpsoe= urllib2.urlpoe(nerquest)
》＞ resnpso.eg etu(r)l
’thtp://exapml.ewesbcrapin.gocmu/serg/il’口o
很遗憾，这个版本依然不能正常工作， 运行时还是会打印出登录 URL。 这
是因为我们缺失了一个重要的组成部分一一 coo。ki当普e通用户加载登录表单
时， fo rmkye的值将会保存在 cooki中e，然后该值会与提交的登录表单数据
中的 formkye值进行对比。下面是使用urllbi2.THTPCooPrkoiecesosr
类增加了cokoi支e持之后的代码。
》＞ imporcto 。kliibe
》＞ cj= cookibe.Cl。ikoieaJr()
》＞ opene=rurlilb.2ubilodp eenr(urbl2.HlTiToPoCkPireoecsso(rjc))
》＞ htm=l opeenr.o pe(nOL GIUNR )L r.e a(d)
》＞ dat=a parsfeo mr(thm)l
》＞ dat［ae’ mail’ ］= LOIGNE MAIL
》＞ dat[ap'asswor’］d = LO工GNPASSWORD
》＞ encoddeadt =a urlbl.uirelnceo(dadt)a
》＞ reqsute= urllb工2.Reqeus(tOLGIUNR,L encoddeatda)
》＞ respnose=opener.ope(nerquets)
》＞ respnos.eg eutr(l )
’thtp://xeampl.weesbcrpain.gocm’
什么是 cookie?
� cook是i网e站在HTT响P应头中传输的少量数据， 形如：
Se一t叫e ：… io_nid＝…向 浏览器将
会存储这些数据，并在后续对该网站的请求头中 包含它们1.这
样就可以让网站识别和跟踪用户 。
93第6章 表单交互
这次我们终于成功了！服务器端接受了我们提交的表单值，resnpso的e
U 是主页。该代码片段以及本章中其他登录示例代 码都可以从 htpts://
也
bibtucket.org/pw/scwoed/scr/tpi/chpatre06l/ogi.npy获取。
6..11从 浏览器加载 cookie
从前面的例子可以看出， 如何向服务器提交它所需的登录信息，有时候
会很复杂。幸好，对于这种麻烦的网站还有一个变通方法，即先在浏览器中
手工执行登录，然后在Pyth脚o本n中复用之前得到的 coo，ki从而e实现自动
登录。不同浏览器采用不同的格式存储 cokoei， 这里我们仅以 Frifoex浏览
器为例。
Frifoex在 sqlite数据库中存储 coo，ki在eJSNO文件中存储 seisos,n
这两种存储方式都可以直接通过 Pytho获n取。对于登录操作来说，我们只需
要获取 sesns，i其存o储结构如下所示。
｛w”indow”s：［．．．
”oc。keis”： ［
｛h”。ts”：e”xarnple.wesbcrpain.gocm”，
”vael”u：”514351559602484:e59ea0bd-5b-l4fc66-a684”，
”pat”h：／””，
”name”：s”essni_oi_pdlac”e｝s
］
．．．
］ ｝
下面是把sesns解i析o到Cookiaer对象的函数代码。
J
def loafdf s esison(sessisonf ielnmae):
cj= co。kibe.Cloiokaire( J)
ifo s.apt.hxeis(tesssison_iflenaem):
josn_dat=a j osn.lodas（ p。e(nessison_iflenrnae，’br’）.erad())
forw indowin sj。n dat.aegt（w’indo’w，s［ ）］：
forc 。okiinew indo.wegt（c’。oki’e，［s）］：
c =c ookliibe.Cook(iOe,
co。k.ieget（n’ame’，冒）’，
cook.ieget（va’lu’e， 『）’，Non,e Fals,e
cook.giee（t’hos’t， ” ） ，
9461. 登录表单
cook.ieget（ho’s’t ，” ）. tsarwtist（h．’’ ） ，
cook.ieget（ho’s’t ，” ）. tsartshw（i．’t）『，
cook.ieget（p’ath’，” ）, Fasle,F als,e
st(rnit(itm.etime()) 3+6 0*0 2 4* 7),
Fasle,No n,e Non,e {)}
cj.setc ook(ice)
els:e
prin’teS ssoinf ielnmaed ose note xi：st’ s，esisonf ilaemne
retuCrJn
这里有一个比较麻烦的地方z不同的操作系统中，Frifoex存储 sesns文io
件的位置不同。在 Linu系x统中，其路径如下所示。
～I. omzilfliar/oexf/.d* efautl/ ssesionst.o rje s
.
在 OSX 中，其路径如下所示。
～L／ibrarAypp/liactioSnu pp/oFritefro/xPorfil/e*.dsefault/sie。snsst.ojrse
而在 WindoVwiss及t以a上版本系统中，其路径如下所示。
告APAPTAD毡／Roaminogz/iMl/lFaifroe/xProflies./d*fealut/sieosnsst.ojrse
下面是返回seisos文n件路径的辅助函数代码。
imporots , glbo
def findf fs esison(s:)
path=s [
’I～. omzilfliar/feo/x*.d efau’lt，
’／～Libr/aArppyliactioSnu ppor/tFifroe/xPorfil*ed.sef/aul't,
’宅APDPAAT毡／Rmoinag/oMzilla/Fifr。e/xPorfile.dsef/a*u’l t
forp atihn p ath: s
fielnmae= os.apth.jino(apt，h’essisonst.osjr’ e）
matcshe=g lbo.glbo(o.sapt.hexpanudse(riflneaem))
ifm atecsh:
returmna thce[sO]
需要注意的是，这里使用的 glbo模块会返回指定路径中所有匹配的文
件。下面是修改后使用浏览器 cokioe登录的代码片段。
95第 6 章 表单交互
》＞ sess工no filneame= findf fs ess口iso()
》＞ cj =loadf fs essoins(sesisonf ilename)
》〉 process=o ru rl工2工b.HTTPoCokiePreosscor(c)j
>>>opener= urllbi2.buildo peenr(proces)s or
》＞ url＝ =’ http://exmaple.webscraipng.com'
》＞ html opee口r.poe口（url).erad()
要检查 sess是io否n加载成功，这次我们无法再依靠登录跳转了。这时我
们需要抓取产生的 HTML， 检查是否存在登录用户标签。如果得到的结果是
Loig口，则说明sessio没n能正确加载。如果出现这种情况，你就需要确认一
下 Fire中fo是x否已经成功登录示例网站。图 6.2所示为Frieb中u显g示的用户
标签结构。
Cons。lIeHT 阳L IC SS Seri11tD OM
自《divclaso�＂nashs"� yl�e＂d1sp1a y:n one；”〉
8 <tllYcl ass="nvabarin ner">'
</a>
llJ <ulc ta.s＝s“dropdownme nu"s ·tyl”ed＝isplabyl:co 民1”＞
</li>
</ul>
图 6.2
Fierbu中g显示该标签位于 ID为 “navrba”的＜ul＞标签中，我们可以使用
第 2章中介绍的lxml库抽取其中的信息。
》＞ tree= lxml.html.fromstrin(ghmt工）
》＞ tre.ecsseslect（u’ln#avbarl ia ’[）O .Jte xtc onte口(t)
WelcomeT esta ccount
本节中的代码非常复杂，而且只支持从 Friefo浏x览器中加载seisos。n如
果你想支持其他浏览器的 coo，ki可以e使用browsecrooike模块。该模块
可以通过 pip instablrolws ercook命i令e进行安装，其文档地址为
htpts://pypi.ptyho.norgp/ypi/browesrcooek。i
966.2支 持内容更新的登录脚本扩展
6.2支 持内容更新的登录脚本扩展
自动化登录成功运行后， 我们还可以继续扩展该脚本， 使其与网站进行交
互 ， 更新 国 家数据。本节中 使用 的代码可以从 htpts://bibtucekt.
org/wps/wocde/scr/tip/chpatre06d/iet.yp获取。如图6.所3示，
每个国家页面底部均有一个 Edi链t接。
I ｜
Horr仓Ser:ich 川
NatiFolnaagl: �
!:dilll‘Z哩
Area: 244,s8q2u0a roem ektsir le
Popautlion: 624,83,447
lso: GB
Country: UnitKeidn gdom
Capital: Londor11
Continent:E U
Tdl: .uk
Cue厅门cCyode: GBP
CurrenNcaym e: Pound
Phone: 44
PosCtoadlFe o rma＠t＃:古f@ @I@###@@!@@@#!#@@#@#
#@@!@##@@ @!#@@@# @@IGRIOAA
PosCt口adlRe egexA:([ (A-ldZ{]2队｝－]Z{})2([1AZ]\d{3})(!AA(­-[Z]{2}
ZJ{22队}d((A{.2-)Z)]Zi]((d[2{A孙3}[2A}-JZl]({[A­
ZJ\d[司A＼d(句A。｝）([lA司｛2}\d[-AZ\]d[A之］
{)2)!O(AGAI)R)$
Languages:e n-G,Bc-GyB,gd
Neighbou厄：IE
Edit
图 6.3
在登录情况下，该链接会指向另一个页面，在该页面中所有国家属性都可
以进行编辑，如图64.所示。
97第6章 表单交互
Na摇onFall吨： 噩噩
Area:
244820.00
Population:
6234制47
lso:
GB
Country:
Un忧回Kingdom
1
Cap饱1I:
London
!
Con四nent:
:E υ
τId:
CurrenCcoyd e:
GBP
I
CurrenNcayme :
Pound
Phone:
44
PostalC odFeo rm：at:伊 咆 ＠｜＠＃棉＠＠晦＠＃啕＠I＠＠＃＃咆＠！
向幽ICodRe咿 x: ��（［A-ZJ可｛2HA-ZK2J>1u凡响｛3页A－写｛2})j([A-Z]{：可
r
Langu匈es:
,e nG-B,yGc-B,dg
Neigl田hrso:u
,I E
.pUdate
图6.4
这里我们编写一个脚本，每次运行时，都会使该国家的人口数量加 1。首
先是复用parsfeomr（ 函）数，抽取国家人口数量的当前值。
》＞ imporlto gin
》＞ COUNTURRYL ＝ ’thtp://exmaplew.esbcarpin.gocm/eidt/
United-Kdio口-mg23’9
》＞ opeenr=logi.nolgicno oki(e)s
•
》＞ cournyt mhlt= ope口reo.pe(nOC UNTRUYR )L rea(d)
986.支2持 内容更新的登脚录本扩展
=
》＞ data par_sfeomr(conutr_hytm)l
》＞ ppir口.tpprin(tadt)a
｛ ’fomrke’y：’c4f0924de a17-4dc8-aea2-34d4ca60ddd’，4
’ ofrmnaem’：’lpac/e5s420841051539848’ ，
’rae’a： 2’4408.200’ ，
'acpitla’：’oLndo’口，
’ocntitne’：n’UE’，
’conutr’y： ’UniteKdi gndo’m，
’ucrrenccoyed『 ：’BGP’，
’ucrr e口c口yame’：’oPun’d，
’di’ ：’4502480151838’59，4
’sio’： G’B’ ，
’alngueas’g： e’n-BG,cy-BG,gd’，
’neihgborus’ ：’EI’，
’hpone’ ：’44’ ，
’oppulatni’：o’26348'44,7
’opsatlc odfeo mrat’ ：’＠ JtJt @@ I＃自＃Jt@I@日日＃＃自由@I@HJt @@I@ Jt@
＃自由l@@Jt日 IJtG@IO@RAA’，
’opsatlc odree g’ex：’（＂［（-AZ)\\d{2}A -Z[]{2}) ([IA -Z)\\d{3}
[A ]2Z{}I)( [A -Z]2{}\ \ d{2}[- AZ)2} )I{( [ AZ-] {\\2 d{}3 )
[A-Zl { 2 }I)( [A -Zl\ \[Ad-Z l \ \[Ad-Z l { 2 }I)( [ A -Zl { 2 }\ \
d[A-Z)\\d[A-Z]2{}I)( 工G ROAA）） $ ’ ，
’tl’d：’.ku’｝
然后为人口数量加 1，并将更新提交到服务器端。
=
》＞ dat［ap’ opluati『o）nin(tadt［ap ’opluat口i’l。 ) 1
= +
》＞ encoddeadt a urlbl.uirelnocd(eadt)a
=
》＞ reuqest urlbl2工.Reqsuet(OCUTNRYUR,L encoddeatda )
=
》＞ rsepnose opeenr.poe(nreuqest)
当我们再次回到国家页时，可以看到人口数量己经增长到62,348，,4如48
图 6.5 所示。
NationaFll ag: ‘’”团
结副噩届四
Area: 244,82s0 quakirloem etres
Populoant:i 62,,344848
图 6.5
99第6章 表单交互
读者可以对任何字段随意进行修改和测试，因为网站所用的数据库每个小时
都会将国家数据恢复为初始值，以保证数据正常。 本节中使用的代码可以从
http:s//bibtucke.torg/swwp/coed/src/pt/ihcapetr06d/ite.yp
获取。需要注意的是，严格来说，本例并不算是网络爬虫，而是广义上的
网络机器人。不过，这里使用的表单技术可以应用于抓取时的复杂表单交
互当中 。
6.3使 用 Mechiaz模ne块实现自 动化表单处理
尽管我们的例子现在已经可以正常运行， 但是可以发现每个表单都需要大
量的工作和测试。我们可以使用 Mehcani模z块e减轻这方面的工作，该模块
提供了与表单交互的高级接口 。Mecnhiaz可e以通过 pip命令进行安装。
pipi nstall mechanize
下面是使用Mecnhiaz实e现前面的人口数量增长示例的代码。
＞》 impormtecnhiaze
》＞br二mechaznei.Broewrs()
》＞ br.ope（口OLGIUNR)L
》＞ br.selte fcomr(n=rO)
》＞ br［e’mail’ ］= LOGIENMA IL
》＞br［p’asswodr'] L=O IGN_PASSWORD
》＞ resp口ose= br.s ubmti()
＞》br.ope(nOC UNRTYU_R )L
》＞ br.selte fcomr(rn=)O
＞》br［p’opluatio’口］= st(rnit(b[rp'opulatni’lo)+ 1)
》＞br.submti()
这段代码比之前的例子要简单得多，因为我们不再需要管理cokoi，e而且
访问表单输入框也更加容易。 该脚本首先创建一个 Mechan浏i览z器e对象，
然后定位到登录URL，选择登录表单。我们可以直接向浏览器对象传递名称
1006.3使 用Mechanei模z块实现自动化表单处理
和值，来设置选定表单的输入框内容。调试时，我们可以直接调用br.fomr,
获取提交之前的表单状态，如下面的代码所示。
》＞prinbtr. fomr
<POSTh tpt://exampelw.esbcrpain.gocm/suerl/ogianpp# liacti/o n
x-www-fmo-rrulencoded
<TextCooln(mtearil=)>
<PasswordCooln(tprasswo=r)>d
<ChcekboxConltr(remoebmer[=no])>
<SubmtiCont(rN<ooln e>o=gLi)n (eradloyn>)
<SbumtiButtonCo(nN<torn>oe=l) ( eradnoly>)
<HiddennCtoro( nlex/t=)( eradonly>)
<HiddenCornot(l fomrkeyf=aS628b04d-f-d4e-3a2f74-e7b37cec6548)
(eradolny>)
<HiddennCtoro(fl_ormanme=log) i(neradolny）》
设定好登录表单的参数之后，调用br.submti（ 提）交选定的登录表单，
然后脚本就处于登录状态了。现在，定位到国家的编辑页面，继续使用表单
界面增加人口数量。需要注意的是，人口数量的输入框需要字符串类型的值，
否则Mecnhiaz会e抛出 TyperEro异r常。
要检查上面的代码是否运行成功， 可以使用 Mechan返i回ze到国家表单，
查询当前的人口数量，如下所示。
》＞ br.ope(CnOUNTURRY)L
》＞ br.selte fcor(mn=rO)
》＞ br［p’ouplati’o］n
62438449
]
和预期一样，人口数量再次增加，现在是 62,348。,449
以于 M h i……… M��
取，网址为htpt://wwwseahr.cosurecforg.ee口t/
mechaniz／。e
110第6章 表单交互
6.4本章小结
在抓取网页时，和表单进行交互是一个非常重要的技能。本章介绍了两种
交互方法z第一种是分析表单，然后手工生成期望的 POST请求：第二种则
是直接使用高级模块 Mechan。ize
下一章，我们将会继续扩展表单相关的技能，学习如何提交需要发送验证
码的表单。
120第 7 章
验证码处理
验证码 （CAPTCH）A的全称为全自动区分计算机和人类的公开图灵测
试 （Comepetlyl AutmoatedP ubilcTu ringt esttot elClom putresand
HumanAsp at）r。从其全称可以看出，验证码用于测试用户是否为真实人
类。一个典型的验证码由扭曲的文本组成，此时计算机程序难以解析，但
人类仍然可以 （希望如此）阅读。许多网站使用验证码来防御与其网站交
互的机器人程序。比如许多银行网站强制每次登录时都需要输入验证码，
这就令人十分痛苦。本章将介绍如何自动化处理验证码问题，首先使用光
学字符识别 （OptilCchaaarctReerc otgoinn,i OCR），然后使用一个验证
码处理 AP。I
7t. 注册账号
在前一章处理表单时，我们使用手工创建的账号登录网站，而忽略了
自 动化创建账号这一部分，这是因为注册表单需要输入验证码。注册页面
为 htpt://exapml.eewbscrapin.gocm/usere/grsite，r如图 7.1
所示。
请注意，每次加载表单时都会显示不同的验证码图像。为了了解表单需要
哪些参数，我们可以复用上一章编写的parsfeomr（ 函）数。第 7 章 验证码处理
》＞ improt cookieliubr,l ilb2, pprint
》＞ REGISTERURL＝ ’thtp://exmpale.webscrap工n.gcom/userr/egsite’r
= _
》＞ cj cookiebli.Cook工aerJ()
》＞ open =e=r urllbi2.buildo pene(rurlbl2i.HTTPoCoke工Proecsso(rc)j)
》＞ html ope口re.open( REGISTERU RL). r ea(d)
》＞ fomr = parsef omr(html)
》＞ pprnit.pprin(ftomr)
｛ ’fomrkey＇： l’ed4e4c4b-cf6-4d8a20d-3-77218df9866’1，
’一formnam『e： r’eg工stre’，
’ enxt’： ’ ／’，
’meail ’： ” ，
’ifrst口ame’： ”
’alst口ame＇： ”，
’passwor『d： ’『F
’passowrd two’：None,
’ercaptchra epsonse fiedl’：None}
前面的代码中， 除recaptchraespo口sfeiel之d外的其他域都很容
易处理，在本例中这个域要求我们从图像中抽取出stra字n符g串e。
Regisetr
r l
Fi「们ame:
Lasntam e:
一一
Email:
一一__J
Passwo「d·
VeriPfays sowrd: pleaisen pyuotup「 assw口a「gdain
Typet htee xt
一－－，
Register
图 7.1
才0471. 注册账号
71.1. 加载验证码图像
在分析验证码图像之前，首先需要从表单中获取该图像。通过 Firgeb可u
以看到，图像数据是嵌入在网页中的，而不是从其他 URL 加载过来的， 如图
7.所2示。
图 7.2
为了在Pyth中o处n理该图像，我们将会用到 Pillow包， 可以使用如下
命令通过 pip安装该包。
pip instalPli llw。
其他安装 Piwll的o方法可 以参考 http ://pilwl.oredathdeoc.s
org土／ηtsallant.hitom。l
Pilwl提o供了一个便捷的 Imag类e，其中包含了很多用于处理验证码
图像的高级方法。下面的函数使用注册页的 HTML作为输入参数，返回包含
验证码图像的工mag对e象。
from工0工mportBytseIO
importl xml.html
from PILi mportI mage
def getc apthca(html) :
tree= lxml.html.frmostrin(hgtml)
imgd ata= tre.ecsseslec（td’iv#rceaptchiam g’）[ O.Jge t（ ’rsc’ ）
imgd ata= imgd ata.parttiion（＇’，）( -1]
binar工ymgdata= imdg ata.decode(b'ase6’4）
fil_el工ke = BytseIO(bina_riymg_da)t a
工mg= Imag.epoen(iflel iek)
returinm g
105第7章 验证码处理
开始几行使用 lxml从表单中获取图像数据。图像数据的前缀定义了数据
类型。在本例中，这是一张进行了 Ba6s4e编码的 PNG图像，这种格式会使
用 ASCI编I码表示二进制数据。我们可以通过在第一个逗号处分割的方法移
除该前缀。然后，使用 Base解6码4图像数据，回到最初的二进制格式。要想
加载图像，PIL 需要一个类似文件的接口，所以在传给 Imag类e之前，我们
又使用了ByteIsO对这个二进制数据进行了封装。
在得到这个格式更加合适的验证码图像后，我们就可以尝试从中抽取文
本了。
Pill与oPwIL的对比
Pillow是知名的Pytohn图像处理库（PytohnI mgaeL irbar,y
，
� PI）L的分支版本 不过PIL从200年9开始就没有再是新过。
Pilwl使o用了和原始PIL 包相同的接口，并且拥有完善的文
档，其文档地址为htpt:/p/illow.readthedso.c
or。g本章中的所有示例在Pilwl和oPIL 中都可以正常运行。
7.2光 学字符识别
光学字符识别 （OptciaClharacRteecro tginno,iO CR）用于从图像中抽
取文本。本节中，我们将使用开源的 TesesraOcCtR引擎。该引擎最初由惠普
公司开发，目前由Goolg主e导。Tesse的r安a装c说t明可以从 http:s//code .
goog.lceom//ptessearcto-c/rwi/kReiadMe获取。然后，可以使用
pip安装其Pyth封o装n版本 pyetssreacat
pipi nstallp ytseseract
如果直接把验证码原始图像传给 pytsesearc，t解析结果一般都会很
糟糕。
1607.2光 学字符识别
》＞ importp ytseseract
》＞ img= getc apctha(html)
》＞ pytesseacrt.image_tot_rsin(gmig)
上面的代码在执行后，会返回－个空字符司抖，也就是说 Tessreac在t
抽取输入图像中的字符时失败了。这是因为 Tesesra的c设t计初衷是抽取
更加典型的文本，比如背景统一的书页。如果我们想要更加有效地使用
Tessrea，c需t要先修改验证码图像，去除其中的背景噪音，只保留文本部
分。为 了 更好地理解我们将要处理的验证码系统，图 7.3中又给出了几个
示例验证码。
图 7.3
① 译者注：返回值也可能是一个错误的解析结果。
107第 7 章 验证码处理
从图7.中3的例子可以看出，验证码文本一般都是黑色的，背景则会更加
明亮，所以我们可以通过检查像素是否为黑色将文本分离出来，该处理过程
又被称为阁值化。通过 Pilwl可o以很容易地实现该处理过程。
》〉 工mg.save（ c’aptchoar 工q工anl.png’ ）
=
》＞ gray img.convret（ ’IL)
》＞ gra=.ys ave（c’apcthag ra.ypng『 ）
》〉 bw gra.ypo工口（ta工mbda x: 0 if x < 1e lse2 55,『 l『）
》＞ bw.asve（c’aptchtah reshoeld.dp口9’）
此时，只有｜淘值小于1的像素才会保留，也就是说，只有全黑的像素才会
保留下来。这段代码片段保存了 3张图像，分别是原始验证码图像、转换后
的灰度图以及阔值化处理后的图像。图 7.所4示为每个阶段保存的图像。
st�1a11 ge
图 7.4
最终，经过阔值化处理的图像中，文本更加清晰，此时我们就可以将其传
给 Tesesra进c行t处理了。
1087.2
光学字符识别
》＞ pytsesearc.timgae__tsotrin(gwb)
’tsrang’e
成功了 ！验证码中的文本已经被成功抽取出来了。在我测试的100张图片
中 ，该方法正确解析了其中的 84个验证码图像。由于示例文本总是小写的
ASC字I符I，因此我们可以将结果限定在这些字符中，从而进－步提高性能。
》＞ imp。rsttring
》＞ word=pyetsesra.citmgaet os tri(nwbg)
》＞ asciwio r＝d ”.j oin( cf orc iwn。 ridfc in
stri.nelgtetr)s. olwe(r)
在对相同的 100张图片的测试中，其识别率提高到了 88。% 下面是目前
注册脚本的完整代码。
imp。rctookliibe
imporutr llib
imporutr lbl2i
imporstt rnig
imp。rptytesesract
REG工STERURL＝ ’thtp://exapm工.eewbscprian.g。cmu/se/rresgteir’
def regist(eifrrs_tnam,e las_tnam,e emai,l passwor:d )
cj c=o okliibe.C ookaire( J)
opeenr= urlbl2i.ubidl opeenr(urlb2l.HiTTPCkoiP。eroscseo(rjc))
htm=l opeenr.o pe(nER GSITE_RU R)L r.e a(d)
=
fomr parse m(fthomr)l
fomr［ f’irsntae m’］ f=i rsntam e
fomr［ l’asnta m’eJ= lasntam e
fomr［ e’mail’ J= email
fomr[ p'asswor’d］= fomr[p'a sswo_rt dwo’］ p=a ssword
img= extraicmta g(ethm)l
captch=a o c(rmi g)
fomr［ r’ecaptcrheas ponfsiee ’ldJ= capctha
encoddeadt =a urlbl.uirelnceo(d。frm)
reuqes=t u rllbi2.Reqsuet(ERGISETRU R,L encoddeadt) a
resnpsoe= opeenr.。pe(nerquest)
sucscse＝ ’u／sere/griesrt’noti nr esp。sne.getu(r)l
returs口ucecss
190第7章 验证码处理
def。c(rmig) :
=
gray im.gconrvte（L’’）
=
bw gra.pyoin(talmdba 0 if < e1 ls2e5 5’，1’）
= x: x
w。rdpytsesera.citmagteo s trnig(bw)
ascii_wrod＝ ” .join(cf orc inw oridf c in
strin.geltetr)s. olwre()
reutrna sciwio rd
regsite（r函） 数下载注册页面，抓取其中的表单，并在表单中设置新账
号的名称、邮箱地址和密码。然后抽取验证码图像，传给 OCR函数，并将
OCR函数产生的结果添加到表单中。接下来提交表单数据，检查响应URL
确认注册是否成功。如果注册失败，响应URL 仍然会是注册页，这既可能是
因为验证码图像解析不正确，也可能是注册账号的邮箱地址己经存在。现在，
只需要使用新账号信息调用regsite（r函）数，就可以注册账号了 。
》＞ regsiter(ifrs_tnam,e lasntam e, emali,p asswo)r d
True
7.12 .进一步改善
要想进一步改善验证码OCR的性能，下面还有一些可能会使用到的方法：
· 实验不同阙值：
· 腐蚀阙值文本，突出字符形状：
· 调整图像大小 （有时增大只寸会起到作用）：
· 根据验证码字体训练OCR工具：
· 限制结果为字典单词。
如果你对改善性能的实验感兴趣，可 以使用该链接 中的示例数据：
htpts://bibtucket.org/pw/scowed/src/pt/cihpatre07s/maple／s。
不过，对于我们注册账号这一 目 的，目前8%8的准确率已经足够了，这是因
为即使是真实用户也会在输入验证码文本时出现错误。实际上，即使1%的准
确率也是足够的，因为脚本可以运行多次直至成功，不过这样做对服务器不
1107.3处 理复杂验证码
够友好，甚至可能会导致 IP被封禁。
7.3处 理复杂验证码
前面用于测试的验证码系统相对来说比较容易处理， 因为本文使用的黑色
字体与背景很容易区分，而且文本是水平的，无须旋转就能被 Tesse准r确act
解析。一般情况下，网站使用的都是类似这种 比较简单的通用验证码系统，
此时可以使用 OCR方法。但是，如果网站使用的是更加复杂的系统，比如
Goog的lreeCAPATC,OHCR方法则需要花费更多努力，甚至可能无法使用。
图 7.所5示为网络上找到的一些更加复杂的验证码图像。
图7.5
在这些例子中，因为文本被置于不同的角度，并且拥有不同的字体和颜色，
所以要使用 OCR方法的话，需要更多工作来清理这些噪音。 即使是真实人类，
解析这些图像也可能会存在困难，尤其是对于那些视觉障碍人士而言。
AltAIE－第 7 章 验证码处理
7.3使.1用验 证码处理服务
为了处理这些更加复杂的图像，我们将使用验证码处理服务①。验证码处
理服务有很多， 比如 2captcha.ocm和 deathbyccahp.atocm一，般其服
务价位在 1 美元 1000个验证码图像左右。当把验证码图像传给它们的 API
时，会有人进行人工查看，并在 HTTP响应中给出解析后的文本。一般来说
该过程在 30秒以内。在本节的示例中，我们将使用 9kw.ue的服务。 虽然该
服务没有提供最便宜的验证码处理价格， 也没有最好的 API设计，但是使用
该 AP可I能不需要花钱。这是因为 9kw.ue允许用户人工处理验证码以获取
积分，然后花费这些积分处理我们的验证码。
73..29 wk入门
要想开始使用 9k，w首先需要创建一个账号，注册网址为http:s//www.
9kw.eur/egsiter.html，注册界面如图 7.所6示。
Regisrt e
E·阳ti:• I ltE-ml副ad由icesh臼ed悟d)
Ref:C二 二二� （Refsu｝町
TOS户 口ac川四（旦旦旦且捏 ｝
l坦延旦旦旦且驾皇 ）
C呻.c二三二1
•
Requl应昼�r�回
图 7.6
① 译者注：一般也称为打码平台。
1127.3处 理复杂验证码
然后，按照账号确认说明进行操作。登录后，我们被定位到http:s//www.
9kw.eu/urscepathca.htm，l其页面显示如医I7.所7示。
Captcshoal ve
CurrCenatp lc3h7a) 5171 321b7xb01 ”lotOfy:
革科马重吾芝 Captcha Status
jUXHVGY ，崎奄＠民
gamdlthae
cotpsa )omo?s '
whuwee
s。un�dPopup口’:,peed
•-DesktoNopt lfl由tloo
15se conds
坐业坠E
Typ：也τext／.飞回世；臼己c。nnnh
In
lnoc归toslevceon ds
图 7.7
在本页中，需要处理其他用户的验证码未获取后面使用 API时所需的积
分。在处理了几个验证码之后，会被定位到 http:Is/ www.9 1α1.e ui/nd e.x
cg?iactni=osuearpinew&suorce=ia来p创建 APkIeoy
9kw验iiH 马API
9kw的AP文I档地址为htt:p/s/ww.w9kwa.p.eihu t/mlb#maipti。-s我tu们a用b
于提交验证码和检查结果的主要部分总结如下。
提交验证码
URL:h tpts:I / www.9 kw.eu /inde.xc gi( OPST)
apikey你的APkIey
：
actni：必o须设为 “usrecaptIco ha”ad up
filepl嗣oua1d-：需0要处理的图像 （文件、ur或l字符串）
base：6如4果输入是 Base编6码4，则设为 “1”
113第7章 验证码处理
matxiemo：ut等待处理的最长时间 （必须为60～399秒9）
self：s如o果lv自e己处理该验证码，则设为 “ 1”
返回值z 该验证码的 ID
请求己提交验证码的结果
URL : htpts:I / www.9 kw.e u/ diexn.c gi (GET)
apeiyk你：的APkIey
act：io必须n设为 “userptccahacdoart”raect
i：d要检查的验证码 ID
ifon：若设为 1 ，没有得到结果时返回 “NODATA"（ 默认返回空）
返回值：要处理的验证码文本或错误码
错误码
。00A1PkIey 不存在
0020没有找到APIkey
000没3有找到激活的APkIey
003账1号被系统禁用 24小时
003账2号没有足够的权限
003需3要升级插件
下面是发送验证码图像到该API的初始实现代码。
imporutr lbl i
imporutr lbl2i
1147.处3理 复杂证验码
AP!U RL＝ ’thtp:s//www.9kw.eui/nd.exgci’
def sencda ptc(hpaai_kye,i mgd ata) :
=
daat {
’cati口。’： u’secraptchauopadl’，
’paieky’：apie_yk,
’file-up0l1o’a：idm-gd_at.anec。d（e’abse46）’ ，
’abse6’4：’1’，
’eslfs。vel’：’1’ ，
’amxt imeotu’：’06’
encoddeadt =a urllib.urelnocd(eadt)a
reuqes=t u rlbl2i.Reques(tAPUIR_,L enceod_ddat)a
respon= suerl lib2.urlpoe(nerquest)
reutrnr espn。s.erea(d)
这个结构应该看起来很熟悉， 首先我们创建了一个所需参数的字典， 对其
进行编码，然后将其作为请求体提交。需要注意的是，这里将 seflsolve
选项设为’1’这，种设置下，如果我们正在使用9kw的Web 界面处理验证码，
那么验证码图像就会传给我们自 己处理，从而可以节约我们的积分。如果此
时我们没有处于登录状态，验证码则会像平时一样传给其他用户 。
下面是获取验证码图像处理结果的代码。
def ge_tcpatch(apai_eky,c apcth_aid:)
=
daat {
’acti’o：n’u searpcthcacroerctd’a，t a
－d，－caPteha－－·d
’
l a p ．l－k e va’·· ap－ l一 唱K eV4
u－
enco dde ad t =a r l bl.uirelnocd(eadt)a
# notteh is ia sG ETr euqest
# sot hed atias a ppendetdot heU RL
=
respnose urllib2.urlpoen(IA_UPRL＋ ’？’＋ encoddeatda)
returrnes posne.r ea(d)
9kw的 API有一个缺点是其响应是普通字符串，而不是类似 JSON 的结构
化格式，这样就会使错误信息的区分更加复杂。例如，此时没有用户处理验
证码图像，则会返回 ERRORNOU SE字R符串。不过幸好我们提交的验证码
图像永远不会包含这类文本。
115第7章 验证码处理
另 一个 困难是 ，只有在其他用户 有时 间 人工处理验证码图 像 时，
getc aptc ha（ 函）数才能返回错误信息，正如之前提到的，通常要在30秒
之后。 为了使实现更加友好，我们将会增加一个封装函数，用于提交验证码
图像以及等待结果返回。 下面的扩展版本代码把这些功能封装到一个可复用
类当中，另外还增加了检查错误信息的功能。
importtim e
imporutr lbl i
imporutr lbl2i
imporrte
fr。mi。imporBtytseIO
clasCsa pcthaIAP:
def _ini一一t（eslfa,pik eyt,im eou6t0=:)
sel.fpaik ey= api key
sel.tfimeou=t t imeout
sel.ufrl＝ ’thtp:s//www.9kw.eui/nde.xgci’
def solv(eeslfi,m )g:
””S”umbitC APTCAH andr eturrne suwlhte rne ady
img_bfufe=r B ytseI(O)
im.gasve(migb uffer,f omrat”＝NPG”）
imgd_at=a imbguf fer.getavlu(e)
capthca_i=d s elf.s end( mig_adt)a
starttim e= time.itm(e)
whilet ime.time()< starttim e+ selft.imeou:t
tr:y
tex=t sel.fegt(capt_cihda)
exceCpatp tcEhrar:o r
pas#s C APTCAH stilnlo tr eady
els:e
ift ext！ ＝’ON DAAT’：
ift ex＝t＝ ’RERORN OU SRE’：
raisCeap thcarEro（rE’rro:r nuos er
availbalet os olveC APCTH’A）
els:e
prin’tAC PTAC Hsolve！d’
1167.处3理 复杂证验码
retutrenx t
print’aWiitngf orC APTAC H
raisCea ptcrhraoE（rE’rr:o ArP!t imeou’t）
def send(eslfi,m gd aat):
””Se”ndC APTCAH fors 。飞rling
prin’StubmtitinCgAP TCAH’
dat=a {
’actni’ o：’usecraptcphlaodua’ ，
’paik ey’：sel.fpaik ey,
’ifle-upl。-a01d’：imgdat.eanocd（eb ’ase’64） ，
’abse6’4：l’’，
’eslsfo vle’： 1’’ ，
’amxteiomu’t：st(resl.ftiemout)
enocdedda ta= urlbl.uirelnco(dadet)a
reuqes=t u rlbl2i.eRques(tesl.fru l, encoddeadt) a
resposne= urlbl2i.urlpoe(nerquest)
resu=l rte sposne.era(d)
sel.cfhcek(ersu)l t
returrne sult
def ge(teslfc,a pt_cihda):
”””Getr esu。lfts olevdC APTAC H
dat=a {
’acti’o：n’u secraphtaccorrdeact’ta，
’di’：captcihda,
'paieky’ ：sel.fpaik ey,
’inof’ ：’1’
enc。deddata= urlbl.uirelnco(dadet)a
reps。sne= urlbl2i.urlp。e(nesl.furl＋ ’？’ ＋en ocde_ddtaa)
resu=l tre spn。s.erea(d)
self.chcek(erslut)
retnu rresult
def chcek(eslfr,e stu)l:
117第7章 验证码处理
””Ch”ecrke su。lftA P!a ndr aiseer roirf e rrocro de
ifr e.amtc（h0’0\d\\dw＋ ’，restu)l:
raisCea pctharEro（rA’P!e rr：or’ ＋re slut)
clasCsa ptcrhra。E(rxEcepnti) o:
pass
CapcthAaPI 类 的源码可 以 从 htpts://bibtucekt.orgw/spw/
coed/scr/tpi/hcapetr70/api.yp获取，该链接中的代码会在 9k.wue
修改其API时保持更新。这个类使用你的APIkye以及超时时间进行实例化，
其中超时时间默认为 60秒。然后，sovle（方）法把验证码图像提交给 AP,I
并持续请求， 直到验证码图像处理完成或者到达超时时间。 目前，检查 API
响应中的错误信息时，chcek（方）法只检查了初始字符，确认其是否遵循错
误信息前包含 4 位数字错误码的格式。要想该 API在使用时更加健壮， 可以
对该方法进行扩展，使其包含全部 34种错误类型。
下面是使用 CapcthaAI类P处理验证码图像时的执行过程示例。
=
》＞ AP!K EY
=
》＞ captchCaa ptAcPhIaA(P工KE＿Y)
=
》＞ img Ima.gpe。e（n’acptch.anpg' )
=
》＞ text captc.hosalv(emig)
SubmtitinCgA PCTHA
Watii nfgo rC APTAC .H. .
Waitifn。grC APTAC H
WaitifnogrC APTAC H
Waiitngf 。rCAPCTH A
.
Watii 口fqorC APTAC .H.
Watii nfgo rC APTAC .H..
WaitifnogrC APTAC H
WaitifnogrC APTAC H
Waiitngf orC APTAC H
Waitign forC APTAC H
Waitgi fnorC APTAC H
CAPTCAH s。lve!d
》＞ text
jxuhvgy
1187.处3理 复杂证验码
这是本章前面给出的第一个复杂验证码图像的正确识别结果。如果再次提
交相同的验证码图像，则会立即返回缓存结果，并且不会再次消耗积分。
》＞ tex=tcapthca.oslv(iemg_tda)a
SubmtitinCgA PCTHA
》＞ text
juxhvgy
7.3.与3注 册功能集成
目前我们已经拥有了一个可以运行的验证码 API解决方案，下面我们可
以将其与前面的表单进行集成。下面的代码对 regstier函数进行了修改，
使其将处理验证码图像的函数作为参数传递进来，这样我们就可以选择使用
OCR方法还是API方法了。
def regsiter(ifrsntam e, las口tame,emai,l passw。rcda,ptcfhn)a :
cj= cookliie.bC ookJiae(r )
opneer= urlbl2i.ubilodp eenr(rullbi2.HTTPCkoioePersosco(rjc))
html= open.epore(nERGSITERU R)L. erad()
fomr=p asre_fomr(thm)l
fomr［ f’irsntam e’ ］= firsntam e
fomr［ l’as口tame’ ］= lasntam e
fomr［ e’mail' ] em=a il
fomr［ p’asswor’dl= f。mr［’passwortdwo’=l p assw。rd
img= extr_aicmta(gthem)l
fomr［ r’ecpatchraes poen sfie’ld］= captcfhn(am ig)
encoddeadt =a urlbl.uirelnocd(eofrm)
reuqest= urlbl2i.Reqeus(tERG工TSE_RUR,Lenocde_ddtaa)
resnpsoe= opeenr.ope(nerquest)
sucecss＝ ’u／sere/griesrt’noti nr esnpso.egetu(r)l
returs口ucecss
下面是使用该函数的例子。
》＞captch=a C apcthAaPI(APKIE )Y
》＞regsite(rifrst_na,m leas_tnaem,e mali,p asswo,r cdaptc.hosalve)
SubmtitinCgA PCTHA
Waiitngf orC APTCAH .
119第7章 验证码处理
.
WaitifnogrC APTAC H
Waitinfgo rC APTAC H
WaitingC AfPoTArC H
WaitifnogrC A PTAC H
• • •
Waiting CfAoPrTA C H
• . •
Watii nfgo rC APTCAH
True
运行成功了！ 我们从表单中成功获取到验证码图像，提交给 9k:w的AP,I
之后其他用户人工处理了该验证码，程序将返回结果提交到Web服务器端，
注册了一个新账号。
7.4本 章小结
本章给出了处理验证码的方法：首先是使用OCR， 然后是使用外部AP。I
对于简单的验证码，或者需要处理大量验证码时，在 OCR方法上花费时间是
很值得的。否则，使用验证码处理AP会I更加经济有效。
下一章中，我们将介绍Srcpay，这是一个流行的高级框架，可以用于创建
抓取应用。
102第 8 章
Scra
py
Scrap是y一个流行的网络爬虫框架，它拥有很多简化网站抓取的高级函
数。本章中，我们将学习使用 Srcpay抓取示例网站，目标任务与第2 章相同。
然后，我们还会介绍 Potri，a这是一个基于 Srcpay的应用，允许用户通过点
击界面抓取网站。
8.1安 装
我们可以使用 pip命令安装 Srcpay，如下所示。
pipi nstallS crapy
由于Srcap依y赖一些外部库，因此如果在安装过程中遇到困难的话，可
以从其官方网站上获取到更多信息，网址为 htpt://doc.csrap.yrog/
enl/aetstn/tior/instlah.ltm。l
目前，Srcpay仅支持Pyth2o.n版7本①，比本书中介绍的其他包条件更加
苛刻。如果想支持更低的Pyth2o.版n6本，需要降级到Srcap0y.2版0本。 而
由于依赖的 I飞111site的d原因，目前还无法支持Pyth3o版n本，不过 Srcap团y
＠译者注：Scr从a1p0.y版1本.开始加对入时也on3的支持，但目前仍处于验试阶段， 分部功能还未得到
有效支持。Scr1a0.p版1y本.需要时也on3.及3以上版本、Twis1t.5e及5d以上版本。详细信息以可参考Scrapy
的官方文档：htpt:/d/o.cscrap.y可。／en/tlesat/ne.whstml#be-tpayth-o3sn-upprot.第8章 Scrapy
队向我确认他们正在解决这一问题。
如果Srcpay安装成功，那么就可以在终端里执行 scarpy命令了 。
$ scrapy -h
Scrpay 0.42.4- no actvie pr。ject
Usage:
scrapy <cmmoand> ［＞p。ti。n]s[arqs]
Availablec 。mmand:s
bench Runqu ickb ench皿atrekst
check Checks piedrc 。ntracts
crwal Runa spider
本章中我们将会使用如下几个命令。
statrproejc ：t 创建一个新项目：
•
genspeird：根据模板生成一个新爬虫：
•
crwal：执行爬虫：
•
]
shell启：动交互式抓取控制台。
•
……… …… II
do.ccsrap.yrog/en/laetstt/opic/csornmands
.h tm.l
8.2启动项 目
安装好 Srcpay以后，我们可以运行startopjrec命t令生成该项目 的默
认结构。具体步骤为：打开终端进入想要存储Srcpay项 目 的目录，然后运行
scrapsyt atrporject<p roejctn ame＞。这里我们使用 exmaple作
为项目名。
1228.启2动项目
$ scrpay starptrojecte xample
$ cd example
下面是 scrap命y令生成的文件结构。
scarp.yfcg
exmaple/
init .yp
itmes.yp
pipe14－nesPy
－
s se －·tt·l口 Sqd frs·D＆
Y
p d eE
Eln l－ p y
←」－
－
其中，在本章比较重要的 几个文件如下所示。
item.sy p：该文件定义了待抓取域的模型。
•
settgis.pn y：该文件定义了一些设置，如用户代理、爬取延时等。
•
spiedrs／该：目录存储实际的爬虫代码。
•
另外，Srcap使y用 scrap.yfcg设置项目配置，使用 pipelnies.yp
处理要抓取的域，不过在本例中无须修改这两个文件。
8.12 .定义模型
默认情况下，exmapl/eietmsp.y文件包含如下代码。
imporstc rapy
clasEsxm apltee!(msrcap.Iytem:)
# definteh ef iledsf ory ouirt me herlei ek:
=
# name scrap.yiFel(d)
pass
ExmaplIete m类是一个模板，需要将其中的内容替换为爬虫运行时想要
存储的待抓取国家信息。 为了更好地聚焦 Srcpay的执行过程，接下来我们只
会抓取国家名称和人口数量，而不是抓取国家的所有信息。 下面是修改后支
132第8章 Scyrap
持该功能的模型代码。
clasEsxm aplIete m(s crap.Iy tem:)
name= scrpay.iFeld()
poupltai口o＝scrap.Fy ie(ld)
定义模型的详细文档可以参考 http://.docsrcpay.org/
enl/a etstt/opics/it ernsh.tm l.
8.2.创2建 爬虫
现在，我们要开始编写真正的爬虫代码了，在 Srcpay里又被称为spdeiro
通过 genspeird命令，传入爬虫名、 域名 以及可选的模板参数，就可以生
成初始模板。
$ scrapy gnespiedrc ountreyx ample.webscrpain.gocm --template=crawl
这里使用内置的 craw模l板，可以生成更接近我们想要的国家爬虫的初
始版本。运行 genspeird命令之后 ，下面的代码将会在 exmapl/e
spider/scoutnr.yyp中 自动生成。
imporstc rapy
frm。scrpay.contr.iilnbkextracitmpoorrsLt i nEkxrtactor
frmo scrpay.ocntr.isbpiedrsi mp。rCtrwalSpiedr,R ule
frmo exapml.eitmesi mporEtx maplietem
clasCson utrySepr(iCdrawlSepr:i) d
name＝ ’ocutnr’y
starutr l=s ［h’ttp:/w/ww.xeamlpe.wesbcrapin.gocm’／］
allwoedd oamin＝s ［e’xmapl.ewebsrcapin.gocm’］
ruels= (
Rule(LinEkxrtact(。larlwo=’rItem／s）’ ，
calblac＝k’aprsiete m’ ，folwl=oTr)u,e
1428.启2动 项 目
def pasrei tem(eslfr,es p。sne:)
=
i ExmaplIete m( )
#i［d ’。mianid’ ］＝
•
reps。ns.epxat（h／’／inpu[ti@d＝”sid”］＠／valu’e）extra(c)t
= •
#i［ n’am’e］ respoenx.spat（h／’d／iv[i@d”＝nam”e］）’ extra(c)t
#i［d’escripnti’］。＝
•
respnos.expat（h／’d／i[vi@d＝”edsrciptin”。］’ ）extra(c)t
return
1
最开始几行导入了后面会用到的 Srcpay库 ，包括 8..12 节中 定义的
ExmaplIete m模型。然后创建了一个爬虫类，该类包括如下类属性。
． 口am：e该属性为定义爬虫名称的字符串。
startu rsl该：属性定义了爬虫起始URL 列表。不过，starutrsl
•
的默认值与我们想要的不一样，在 exmapl.eewbscrapin.gocm
域名之前多了WWW前缀。
allwoedd oamin：s该属性定义了可以爬取的域名列表。如果没有
•
定义该属性，则表示可以爬取任何域名。
rule：s该属性为一个正则表达式集合， 用于告知爬虫需要跟踪哪些
•
链接。
rules属性还有一个 callbcak函数，用于解析下载得到的响应，而
parsiete （m示 ）例方法给我们提供了一个从响应中获取数据的例子。
Srcap是y一个高级框架，因此即使只有这几行代码，也还有很多需要了解
的知识。官方文档中包含了创建爬虫相关的更多细节， 其网址为htt:p//do.c
scrapy.rog/ne/ltaest/tpoic/spsiedr.shtmla
1 .优化设置
在运行前面生成的爬虫之前，需要更新Scra的p设y置，避免爬虫被封禁。
默认情况下，Srcpay对同一域名允许最多 8 个并发下载，并且两次下载之间
152第8章 Scrapy
没有延时，这样就会比真实用户浏览时的速度快很多，所以很容易被服务器
检测到。在前言中我们提到，当下载速度持续高于每秒一个请求时，我们抓
取的示例网站会暂时封禁爬虫，也就是说使用默认配置会造成我们的爬虫被
封禁。除非你在本地运行示例网站，否则我建议在 exmapl/esettgisn.py
文件中添加如下几行，使爬虫同时只能对每个域名发起一个请求，并且每两
次请求之间存在延时：
=
CONUCRERNTR EQSUETSP ERD OAMIN 1
=
DOWNALDOD ELAY 5
请注意，Srcap在y两次请求之间的延时并不是精确的，这是因为精确的延
时同样会造成爬虫容易被检测到，然后被封禁。 而Srcpay实际使用的方法是
在两次请求之间的延时上添加随机的偏移量。要想了解更多关于上述设置和
其他设置的 细 节，可 以参考 htpt://doc.csrpay.orgn//eltaest/
topic/s setitng.hstm。l
2.测试爬虫
想要从命令行运行爬虫，需要使用 craw命l令，并且带上爬虫的名称。
$ scrapy crawlc 。untr-ysL 。气LEVEL=ERR1。R
[c。untry]ERROR: Err。dr。wnl。adin<gGETh tpt:I / www.e xample.w ebscrpaing.
com/>: DNlS。 。ukpfailed: addrses ’www.xeample.webscrapin.g。cm’not
f。un:d[Errn。－5]No addrsesa ss。ctieadwith h。stna皿.e.
和预期一样，默认的爬虫代码运行失败了， 这是因为 htt:p//www.
exmapl.eewbscrapin.gocm并不存在①。此外，你还会注意到命令中有一
个 －sLOGL EEVL=ERROR标记 ，这 是 一 个 Srcpay设 置 ，等 同 于在
setitng.psy文件中定义 LOG_LEVLE＝ E’RROR’ 。默认情况下，Srcpay
会在终端上输出所有 日 志信息，而这里是将 日 志级别提升至只显示错误
信息。
译者注： 在书本翻译时，该域名己经配置了DNS解析，此时返回结果应该为空而，不是错误信。息
①
1628.2启 动项 目
下面的代码更正了爬虫的起始URL，并且设定了要爬取的网页。
=
starutr ls ['thtp://exmapl.weebscarpin.gocm’／］
=
rules (
Rule(LinEkxtrac(tlaolwro＝’i／nd／ex）’ f,o lwl=。Tr)u,e
Rule(LinEkxtrac(tlaolwro＝’／vie’w,）／ c allbac’kap＝rsiet me ’ ）
第一条规则爬取索引页并跟踪其中的链接，而第二条规则爬取国家页面并
将下载响应传给 callback函数用于抓取。下面让我们把日 志级别设为
DEBU以G显示所有信息，来看下爬虫是如何运行的。
$ scrapy crawlc 。untr-ysL OG_LELVE=DEBUG
[c。untr]yDEBU:G Crawled( 200<)G ETh tpt://example.webscrpain.q。c，m/>
[ocuntry] o：固UG: Crwaled( 200<)1钮 Thttp://examplew曲.scrapin.gomc／扭曲x/1>
[ocuntryD]E BU:GF ilterdeupdl icatreequ est:< GET http:I Iex ample.we bscrpain.q
C惆Iindex/l>- no more dupliactesw illb e sh。wn(ese DUPEFLITE飞DEBUG
t。sh。walld upliactes)
[c。untr]yDEBU:G Crawle(d2 00<)G ET
htpt://example.webscrapinq.c。m/view/Antuiaq-and-Babruda-1>0
[c。untry]DEBU:G Crawled( 200<)G ET
htpt://xe血1ple.webscrapin.qc om/usre/lqoin_?n ex=t%F2index%2lF>
[。cuntry]DEBU:G Crawled( 200<)G ET
http://example.webscrapinq.com/userre/qisetr?_nex%t2=Finxd%e2Fl>
输出的 日志信息显示，索引页和国家页都可以正确爬取，并且已经过滤了
重复链接。但是，我们还会发现爬虫浪费了很多资源来爬取每个网页上的登
录和注册表单链接， 因为们它也匹配 rule里s的正则表达式。前面命令中的
登录 URL 以 口ex%t2=Finedx%F2l结尾， 也就是 nex/t=i口de/xl经过
URL 编码后的结果，其目的是让服务器端获取用户登录后的跳转地址。 要想
避免爬取这些 URL，我们可以使用规则的 de口y参数，该参数同样需要一个
正则表达式，用于匹配所有不想爬取的U肚。下面对之前的代码进行了修改，
通过避免URL 包含／use来r防／止爬取用户登录和注册表单。
172第8章 Scrapy
rule=s (
Rule(LinEkxtrac(tlaolwro＝’／index’／，deny'=u/se’r／） ，
follow=T)r,ue
Rule(LinkExtra(caltloowr＝’／vie’w，／deny’＝u／se’r／） ，
callbac’kap＝rsiete m’ ）
想要进一步了解如何使用该类， 可以参考其文档，网址为
htpt://doc.csrap.yrog//elntaesttop/ic/s
linekxrtacto.hr tsm.l
8.2.使3用 shel命l令抓取
现在 Srcpay已经可以爬取国家页面了，下面还需要定义要抓取哪些数据。
一－
为了帮助测试如何从网页中抽取数据，Srcpay提供了一个很方便的命令
sr时工， 可以下载URL 并在 P严ho解n释器中给出结果状态。下面是爬取某
个示例国家时的结果。
$ scrapy shellh tpt://example.webscrapin.gcom/vienwi/tUedK-ingdmo-239
[s ]A vailbaleS crapy。，bjects:
[s]c rawler< scrapy.rcawler.Crawelr。bjectat Ox7f1457da5390>
[s]i tem {}
[s]re quest＜ 钮Thttp://example.webscrap.iomcng/view/United-Ki3n9g>d om-2
[s]re sp。n<s2e00h ttp://example.w由scrpaingc.om/view/Unitiendg-omdK-23>9
[s]s ettigns <scrpay.estting.sSetitngs。bjectat Oxf7l47cbl49f0>
[s]s pide<rS piedr’edfault’ ta Oxf714725eb590>
[s]U seufl sh。trcut:s
[s]s hepl ()S hellh epl (printthi sh el)p
[s]f etch(re龟－。r_url)Fetchr equest （。zURL) andu pdatle oca。lbjects
[s]v iew(respn。se)Viewr esp。nseai bnr owser
现在我们可以查询这些对象，检查哪些数据可以使用。
In[ l:] resposne.rul
’thtp://xeampl.ewesbcrapi.cnogm/vienwi/tU-eKding-d2o3m’9
工n[2:] respos口e.tsatus
200
1828.启2动 项 目
Srcpay使用 lxml抓取数据，所以我们仍然可以使用第 2 章中用过的css
选择器。
In[ )3:r espon.ssces（t’r#placcoeusn trryo w .wt2dpf w:t:ex’t）
[S<electxopra th"=duecsenda-onrt-s:el:f
tr[@id＝ ’lpacecso u口trryow’］／desecndant-osre fl::
*t/d[@clasasn dc onta(i ns
conc（a”t，normlaize-psac(ec@la）ss，” ） ，
’w2pf w’）) t/ex（t”） data=’unUiteKdi ndgo’m］〉
该方法返回一个 lxml选择器，要想使用它，还需要调用extra（c）t法方。
In[ 4：）ηamec ss＝ ’rt#placceousn 一＿trroywtd.w2_pfw::etx’t
In[ )5 :re psons.escs(nmaec ss.)xe tra(c)t
[u’nUiteKdin gdo’m ］
In[ )6:p o_pcss＝ ’rt#plapcoeupsl aotni_rotwd .w2_pf:wt:ex’t
In[ )7 r:es pnos.ec sso p(c pss).e xtra(c)t
[u’26,348,44’7］
然后，可以在先前生成的 exmapl/epsiedr/scountr.yyp文件的
parsiete m（ 方）法中使用这些 cs选s择器。
def parsiete m(eslfr,e psos口e) :
item= Examlpetie(m)
namec ss＝ ’rt#placcoeusn trryo wt d.w2pf w::etx't
=
item［ n’ame’）r epsosne.scs（口amecss).e xtra(c)t
popc ss＝ ’rt#plsa_cpeolpautoin一＿rowtd.w2_pfw::tex’t
item［ p’ouplatni’o）= respos口e.scs(oppc_s)s.xetra(c)t
retu工rntern
8.2.检4查 结果
下面是该爬虫的完整代码。
clasCso urnytSpeir(dCrwalSpiedr:)
口ame＝ ’ocunt’r y
starutr l=s ［h’ttp://exmapl.weebscrapi.nocgm’／］
allwoedd omians= ［e’xampl.ewebsrcapin.gocm’］
rule=s (
192第8章 Scrapy
Rule(LinExktrac(tlaolrwo＝’i／nedx’／，deny’＝u／se’r／） ，
f。llow=Tr)u,e
Rule(LinExktrac(tlaolrwo＝’／vie冒w，／edny『＝u／se’r／） ，
callbac’kap＝rsiet me’ ）
def pasre_ite(meslfr,e snpso)e:
item= Exmaplee!m(t)
name_scs＝ ’rt#pclesa_coun_trroywt d.w2_pfw::etx’t
item［ n’ame’=］ r esposne.cs（sa口mecs)s e.x tra(c)t
po_pcss＝ ’rt#plapcoepslu atoin一＿r。twd.w2_pfw:t:ex’t
ite［m’。 ppulatni’oJr=es posne.c s(sp po_c s)s e.x tra(c)t
retnu irtme
要想保存结果，我们可以在 parsietem（ 方）法中添加额外的代码，用
于写入己抓取的国家数据，或是定义管道。不过，这一操作并不是必需的，
因为Srcap还y提供了一个更方便的一－ouptut选项，用于自动保存己抓取的
条目，可选格式包括 csv、JSNO和XM L。下面是该爬虫的最终版运行时的
结果，该结果将会输出到一个 csv文件中，此外该爬虫的日志级别被设定为
INFO以过滤不重要的信息。
$ scrapy crawlc 。untr-y-outupt=cournite.scsv- sL 。G_LEL＇四=NIJ!I。
[scrap]y INE：。Scrapy0.24 . s4 tarted( bo:t example)
[c。untr］y工NF：。Spiedropened
[ocuntry] INFO: Crawle0dp ages( at0p a伊s／：皿叫 ，sc吨回r O it剧S (ta i0 t回s/ min)
[ocuntry]INFO : Crawle1d0p ages( a1t0 p ages/mi时 ，scrpead9it四S (ta 9t剧s /i min)
[c。untr］y工NF：。Crawled264 paqse (at1 0p aqse/min), scraped2 38i tems
(at9 items/min)
[c。untr]yINF：。Crawled274p aqse (at 10p aqse/min), scraped2 48i tems
(at1 0i tems/min)
[c。untr]yINE：。Cl。isnqspiedr (finished)
[countr]y INF：。Storedcsvf eed( 225 items) in: coutnreis.csv
[c。untyr]INF：。DumpinqScrapy stats:
｛d’。wnl。aedr/erques_tbytes’ ：1550,01
’。dwnl。aedrr/eques_tc。un’t：27,9
’。dwnl。ader/reques_tmeth。dc_outn/EGT’ ：279,
’。dwnlodaer/resp。n_sbeyets' :9431,9 0
’。dwnloaedr/ersp。sne_c。un’t：27,9
1038.启2动项 目
’odwnl。aderr/esp。n_ssetatu_sc。unt/20’0：27,9
’udpefiletr/filetred’：61,
’ifnisrhe asno’： ’ifnishde',
’tie_mscrpaed_c。u’nt：252,
’。1g_c。nut/IJi。N’：36,
’erquest:二depth_mxa’：26,
’ersp。sne_recieve二d;coutn’：27,9
'csheudler/edqueued’：27,9
’csheudlerd/equeued/mem'。r:2y7,9
’cshedulere/nqueude’：279,
’csheudler/equneued/m础。yr『：27}9
[c。untr]yINJi℃：Spiedrc l。se(dfinished)
在爬取过程的最后阶段，Srcpay 会输出－些统计信息， 给出爬虫运行的一
些指标。从统计结果中，我们可以了解到爬虫总共爬取了 279个网页，并抓
取到其中的25个2条日 ，这与数据库中的国家数量一致，因此我们知道爬虫
己经找到了所有国家数据。
要想验证抓取的这些国家信息正确与否，我们可以检查 counrtise.scv
文件中的内容。
name,oppluation
Afghastnai，n2 ”91,2,1826”
Antiugaa ndB arbud，a8” 67,5”4
Anatrcti，c。a
Anguilal，”132,54”
Angloa”，130,6,816"1
Androra，”840,0。”
AmreicanS amoa，”57,881”
Alegri，”a34,5861,8”4
Albaan， i2”,9869,5”2
AlanIdsl and，s” 267,1 1”
和预期一样，表格中包含了每个国家的名称和人口数量。抓取这些数据所
要编写的代码比第2 章中的原始爬虫要少很多， 这是因为Srcpay 提供了很多
高级功能。在下一节中，我们将使用 Porat重i新实现该爬虫，而且要编写的
代码更少。
113第8章 Scrapy
8.2.中5断 与恢复爬虫
在抓取网站时，暂停爬虫并于稍后恢复而不是重新开始，有时会很有用。
比如，软件更新后重启计算机，或是要爬取的网站出现错误需要稍后继续爬
取时，都可能会中断爬虫。非常方便的是，Srcpay内置了对暂停与恢复爬取
的支持，这样我们就不需要再修改示例爬虫了。 要开启该功能，我们只需要
定义用于保存爬虫当前状态目录的 JODBI设R置即可。需要注意的是，多个
爬虫的状态需要保存在不同的目录当中。下面是在我们的爬虫中使用该功能
的示例。
$ scrapyc rwal coutnry- sL 。GL_EVEL=DEBU-GsJ OBIDR=crwals/countyr
[c。untr]yDEBU:G Scrapedf rm。<200
htpt://xeample.webscrapin.gc。m/vi/eAwfghnaisatn-1>
｛n’ame': [u’Afghainsatn＇］， ’oppulatin。': [u’92,121,286’］ ｝
"C[ csrapy]INFO : ReceivedS IIGNT,s huttidonwng gracefully.S endag aitn。 force
[c。untr]yINF：1。Cl。isngspiedr (hsutd1。w)n
[countr]y DEBU:G Crawled( 200<)G ET
htpt://exa皿ple.webscrapin.gcom/view/Antuia-gand-Babrud-a1>0 (erfere:r
http:/ /xeai.呼le.w＇s由crapin.gcom)/
[c。untr]yDEBU:G Scrapedf rm。 <200
htpt://example.webscrpain.gc。m/view/Antuiag-and-Babrud-a1>0
｛n’ame': [u’Antiguaa ndB arbud’a1， ’。p1pulati。’n ：［u’68,754’］ }
[c。untr]yDEBU:G Crawled( 200<)G ET
http://eamxple.webscraping.。cim/view/Anatrctiac-9>(erfeerr:
htpt://xeample.webscarping.ocm/)
[。cuntr]yDEBU:G Scrapedf rmo <200
htpt://example.webscrapin.gocm/view/Anatrctiac-9>
｛n’ame’： u［’Antarctic’a1， p’。1pulatio’n ：u［’。’］ ｝
[c。untr]yINF：℃Spiedr close(dhs utdown)
从上述执行过程可以看出，我们使用AcCtClr+C）发送终止信号，然后
爬虫又完成了几个条目的处理之后才终止。想要 Srcpay保存爬虫状态， 就必
须等待它正常结束，而不能经受不住诱惑再次按下C创＋C强行立即终止 ！ 现
在，爬虫状态保存在 crawls/conutr目y录中，之后可以运行同样的命令
恢复爬虫运行。
1238.使3用 Port编i写可a视化爬虫
$ scrpay crawlc ountr-ys L 。G_LELVE=DEBU-GsJ。， BDIR=crwalsc/。untry
[c。untr]yINFi：。Resu皿ingcrawl( 12r equesst scheduled)
[c。untr]yDEBU:G Crawled( 200<)G ET
http://example.webscrapin.gcom/view/Anlgluai-8(>er feerr:
htpt://example.webscrapin.gocm/)
[c。untr]yDEBU:G Scrapedf rm。＇<200
htpt://xeample.webscrapin.gc。，m/view/uAniglal-8>
｛n’a皿e’： ［u’nAguill’a1 ，’。ppulatin。’： u［’31,524’］ ｝
[c。untr]yDEBU:G Crawled( 200<)G ET
htpt://example.webscrapin.gocm/veiw/Ang。la7->(erfeerr:
htpt://xeample.webscrapin.g。c，m/)
[countr]y DEBU:G Scarpedf rm。<200
htpt://example.webscrapin.g。cm/veiw/Ang。la7->
｛n’ame’： ［u’Ang。l’a］， p’opulatino’： ［u’31,608,161’｝］
此时，爬虫从刚才暂停的地方恢复运行，和正常启动一样继续进行爬取。
该功能对于我们的示例网站而言用处不大， 因为要下载的页面数量非常小。
不过，对于那些需要爬取几个月的大型网站而言，能够暂停和恢复爬虫就非
常方便了。
需要注意的是，有一些边界情况在这里没有覆盖， 可能会在恢复爬取时产生
问题，比如coo过ki期等e，此类问题可以从 Scrpya的官方文档中进行详细了解，
其网址为htpt:/d/oc.csrap.yrog/ne/ltaest/tpoic/jsbos.thml。
8.3使 用 Port编i写a可视化爬虫
Potri是a一款基于 Srcpay开发的开源工具， 该工具可以通过点击要抓取的
网页部分来创建爬虫，这样就比手工创建cs选s择器的方式更加方便。
8.13 .安装
Port是i一a款非常强大的工具，为了实现其功能需要依赖很多外部库。 由
于该工具相对较新，因此下面会稍微介绍一下它的安装步骤。 如果未来该工
133第8章 Scrapy
具 的安装步骤有所简化， 可以从其最新文档中 获取安装方法，网址为
http:s//gtihub.ocm/scrpainhgub/poritar#uninng-porita。
推荐安装方式的第一步是使用virtulaenv创建一个虚拟 Py由on环境。
这里我们将该环境命名为porteixamapl，e当然你也可以将其替换成其他
任何名称。
$ pip installv irutalevn
$ virtualenvp ort二ieax缸nple --n。－siet-pacakges
$ sourcep 。rt_ieaxample/bina/ctivtae
(p。rt_ieaxampl)e$cd p。rt二ie8:xample
为什么使用 virtualenv?
假如你的项目使用早期版本的 工xml进行开发， 而新版本的
工xml引入了一些向后不兼容的变史，会影响你项目 的正常运
行。但是，其他一些项目准备依赖新版本的lxml。如果你的
£ 项 目 使用 系统中安装的lx，ml那么当 lxml更新为支持其他
项 目的新版本时 你的项目 将会运行失败
IanB ikcin的gvirtuae工nv提供了一个聪明的办法来解决这
一问题，那就是复制系统Pyth on可执行文件及其依赖到一个本
地目录，创建隔离的 町也 on环境。 这样就九许项目在本地安装
特定的同咄on库版本，独立于外部系统。详细信息可以查看其
文档，网址为http:s//vritulaevn.yppa .oi。
然后， 在virtuaelnv中安装 Porti及a其依赖。
(p。rt_ieax四ple)$git cln。ehtpts://github.coms/crpainghu/bp。rtia
(p。rt_ieaxa皿ple)$ cpd。 rtia
(p。rt二ie8:xample)$pipi nstal-lr r equirement.sxtt
(p。rt_ieaxample)$pipi nstall- e .s/lyb。t
Port目ia前处于活跃开发期，因此在你阅读本书时其接口可能已经发生变
化。如果你想使用和本书相同的版本进行开发，可以运行如下gi命t令。
1438.3使 用Port编i写a可视化爬虫
(p。rtieaxample)$g itc hecokut 8210941
如果你还没有安装 gi，t可以直接下载 Port的i最a新版，其网址为
htpts://gtihu.bcom/scrapgihnbu/portiaarc/hie/vmatse.rzpi。
安装完成后，可以进入 sly目d录运行服务器端来启动 Por。tia
(portiae xample)$c d slyd
(portia_example$) twistd -n s工yd
如 果安 装成 功 ，就 可 以 在 浏 览器 中访 问 到 Port工i具a，网 址 为
htpt://localshot:0901s/taticm/ai.nthm。l
图 8.所1示为其初始屏幕。
F唱”nisP c:I
。阳’”吗副
图 8.1
如果你在安装过程中遇到了问题，可以查看 Porti的a问题页，网址为
htpts://github.com/scranpghiub/porita/iuses，s 也许其他人已
经经历过相同的问题并且找到了解决方案。
135第8章 Scrapy
8.3标.注2
在 Port的i启a动页，有一个用于输入待抓取网站 URL的文本框，比如
htpt://exampl.ewebscarpir可.ocm。输入后，Porti会a在其主面板加载
该网页，如图8.所2示。
.. Q '
参严··“�mlp副��“咱 �‘
。
。
Examplwee bs carping
webstie
嚣嚣S
B重建 M醉品唰向忌器 h•ll"<l<"''"
""'
. 问 ［｝ """
C!阳市恼 巾嗣 .....由a
圄 叫 画自 ＂＂＇＇＂＇
E盟国
. ..明白 g .....刷刷阳.....
<P＜制也 gMI” ’
图 8.2
默认情况下，项 目名称被设为 ne_wprojt，ec而爬虫名称则被设为待爬取
域名Cexapml.ewbescpriang.）c这，o两m项都可以通过单击相应标签进行修改。
接下来，浏览器会定位到一个示例国家网页，让你标注感兴趣的数据，如图
8.3 所。示
单击 Annotatthepiasg 按e钮，然后再单击国家人口数量，就会弹出如图
8.所4示的对话框。
单击＋fiel按d钮创建一个名为popluation的新域，然后单击Don保e存。
接下来，对国家名称以及你感兴趣的其他域进行相同操作。 被标注的域会在
网页中高亮显示，并且可以在右边栏的面板中进行编辑，如图8.5 所。示
1368.3使 用Port编i写a可视化爬虫
t::1
Examplwee bs carpign
website
黝曾．田．
能atlmalR 咽r
....缸”蜀暴w萄...
，气－民�· ＂＇＂口··
t.o· M
＂＂＂＇自y .,.. ..... ,,
C警戒，，， 阳l... 副
C笛您则1t. AS＂飞＇＂
Tld.
°""""""'"'
Cu阻四NM吐 崎阳世
间－ "
P部描＂＂＂＇何阳咀 ＂＂＂$＇＇公F＂ ＂＇
·�瞄臼乡，R崎回
L，理＂＇’”z
N•结始剧m tMCH!llJJ 吨＂＇
臼建
｜茎8I.3
图 8.4
l::::ll.'
宵”驰”’ltlck.i“�
’�丁 a;;;-;-·
Examplwee bs craipng
。口
website
＝－』�� 出巳j
酌”掘 。。
阳陋、唱n叮
"'""
向你..，，，..
....
C...ilfy.
c.揭属
C惯常阳”L AS
鸡-d, ..,;
"""'""'c叙... ,.,,,
α＂＂＇忧V －巳 八、阳’‘
阿炮佛’ "
R锐！alCol’C!f'«mat 偏执，，，」，’，耐
P偶WC骸给R鸣”汇
＂＂＂＇均百 ..
＂＇事l!OUrs: 11,l�C民口同时
"''
图 8.5
137第8章 Scrapy
完成标注后，单击顶部的蓝色按钮 ConitnuBeroiwns。g
8.3.优3化 爬虫
标注完成后，Porti会a生成一个 Srcpay项 目 ，并将产生的文件保存到
daat/prjeoct目s录中。要运行爬虫，只需执行 poritarcawl命令，并
带上项目名和爬虫名即可。不过，如果爬虫使用默认设置运行的话，很快就
会遇到服务器错误。
(p。rt_ieaxa呻le$)portiraacwlp 。rtai/syld/data/pjrec。ts/newyr。ject
example.webscrapin.gocm [example.webscarpin.gocm] DEBU:G Crawle(d2 00)
<GETh tpt://ex皿ple.webscrapin.gocm/veiw/Antarctcia-9>
[example.webscraping.ocm] DEBU:G Scrpaedf rmo <200
htt:p//ex四ple.w由scrapin.g。cm/view/Anatrctiac-9>
｛＿’templaet’： 9’300dcc044d4b75151044384cc0f141efd69972’2，
’＿type’： u’defautl ’ ，
I
u’amne’： u［ An’tarcti’cla
u’p。pualti。’n： u［’。’，］
’rul’： ’thtp://example.webscraping.c。m/veiw/Antractcia-9’｝
[example.webscrapin.gocm]D EBU:G Retryin<gG ET
http://ex四ple.webscrapin.gocm/edit/Antartciac-9>(afile1d timse) :50 0
InetrnalS evrer Error
这和 “优化放置”小节中遇到的问题是一样的， 因为 Portai生成的项目使
用了默认的 Srcpay 爬取设置，导致下载速度过快。我们仍然可以在设置文件
中修改这些设置 （文件位于 datap/rjoect/snewprjoect/psiedr/s
setitng.psy）。 不过，为了演示一些新方法，这次我们改为使用命令行进
行设置。
(p。rt_ieaxa呻le)$p。rtiacrapwolritas/lydd/ata/opjrectse/wnyroject
部呻 le.w由 scapring. -sCONαm圆T _R昭JE STS」血气民阳N=l -sDC删LO皿＇. ＿D ELAY=S
com
[example.webscrapin.gocm] DEBU:G Crawled( 200<)G ET
1838.3使 用Port编i写a可视化爬虫
http://exampel.webscrpaing.com/userl/og工?n_next＝毛F2工nde毛x2Fl>
[ex缸nple .webscrapin.gcom]DEBUG:C rawled( 200<)G ET
http://example.webscrapi.ncogm/usere/grisetr?_nex＝t屯2iFndex毛2Fl>
当运行这个放慢速度 的爬虫时，就可以避免被封禁的问题了。 不过，
接下来同样也会遇到下载非必要网页 （比如登录和注册页〉 这个降低效率
的问题。默认情况下，Por生ti成a的爬虫会爬取给定域名的所有 URL。 要
想只爬取特定 URL，可以配置右边栏面板中的Crawnlgi选项卡，如图 8.6
所示。
Cor,1.fifgoulrleao nwde xclupdaette r.,.n s
回民部pecntolfwlo o
Folllnikso wth maatt hcU liPs' llrtt程ms0
由
llnd辑对
圈
Ni智商j
I 圈
N叫 lowpattern
Excllukldstnhe 'am ta tcht hipsatt erns0
I
，’1岳母r/ m
I
N刷 刷eludpea时 ｜圈
5蛋白r11llbealo·cyk时!Ink翠 移
图8.6
这里， 我们添加／川de／x和／viwe／作为爬虫跟踪模式，并且将／user/
作为排除模式，这些都和之前 Scarp项y目 中的用法相似。如果勾选了底部的
Overbllaoyc lkiend复k 选s框，Poira就t会把跟踪链接高亮为绿色，排除链接
高亮为红色，如图8.所7示。
139第8 章 Scrapy
S网Dlt•ur叼幽晴圆旬玛翩·�栩
制削喃’‘ ＠
Exapmlwee bs carpnig 臣。
webiste
睦盟盟
阳，＂＂＂＂.锢，. 。
0
p。脚，，恤h帆布‘俐馆’的......."... .
。
。
�。，，洒因
时呻帕 ，阳’…恤 ...
（囚
a
臼。恻，.， ..础 �Rallt.0
图 8.7
8.43 检.查结果
现在就可以执行Por生t成i的a爬虫了，另外和之前一样，我们使用一ouptut
选项指定输出的csv文件。
{p。rt_ieaxample)$ portaicrawlp orita/syld/datar/opjec/tnse_pwr。ject
example.webscrapin.g。cm －－。utput=cournites.csv-s CONCURRE_NRTEQUESTS_
PER DOMAIN=l -sD OWNLOADD ELAY=S
当运行如上命令时，该爬虫将会产生和手工创建的 Srcap版y本相同的
输出。
Port是i一a个非常方便的与 Scrya配p合的工具。对于简单的网站，使用
Port开i发a爬虫通常速度更快。相反，对于复杂的网站 （ 比如依赖 JavacSript
的界面〉，则可以选择使用 Pyth直o接n开发 Srcap爬y虫。
1408.使4用Sceryla实现p自动化抓取
8.4使 用 Scarpel实y现自动化抓取
为了抓取标注域， Pio使art用了Scraelp库y，这是一款独立于Porti之a外
的非常有用的开源工具，该工具可以从 htpts://gihtub.ocm/scrpay/
scarpley获取。Srcpael使y用训练数据建立从网页中抓取哪些内容的模
型，并在以后抓取相同结构的其他网页时应用该模型。下面是该工具的运
行示例。
(port_ieaxample)$p yth。n
》＞ frm。 scrpaely imp。rtScrapre
》＞ s = Scraper( )
》＞ trai_unrl＝ ’thtp://example.webscarpin.gc。，m/vi/eAwfghnaisatn-1’
》＞ s.trai(nrtai_nurl, ｛n’ame’ ：’fAghnaistan’ ，’oppulati’。n：’292,1,1826｝’｝
》＞ test_url＝ ’thtp://ex四ple.webscrpain.gc。，m/view/tUedn-iKnigdom2-39’
》＞ s.scrape(ets_turl) I
[{ u’a皿ne’： ［u’UnitedKingdo’m］ U’pouplati’。n：［u’26,438,447’］ ］｝
首先，将我们想要从Afhgainstan网页中抓取的数据传给 Srcpaeyl，本
例中是国家名称和人口数量。然后，在另一个国家页上应用该模型， 可以看
出Srcpaeyl使用该模型返回了正确的国家名称和人口数量。
这一工作流允许我们无须知晓网页结构，只把所需内容抽取出来作为训练
案例，就可以抓取网页。如果网页内容是静态的，在布局发生改变时，这种
方法就会非常有用。 例如一个新闻网站，己发表文章的文本一般不会发生变
化，但是其布局可能会更新。 这种情况下，Srcpaeyl可以使用相同的数据重新
训练，针对新的网站结构生成模型。
在测试 Srcaepyl时，此处使用的示例网页具有良好的结构，每个数据类型
的标签和属性都是独立的， 因此 Srcpaeyl可以正确地训练模型。但是，对于
更加复杂的网页，Srcpael可y能在定位内容时失败，因此在其文档中会警告你
应当 “谨慎训练”。也许今后会有更加健壮的自动化爬虫库发布，不过现在仍
需了解使用第 2 章中介绍的技术直接抓取网站的方法。
141第8章 Scrapy
8.5本章小结
本章首先介绍了网络爬虫框架 Srcpay，该框架拥有很多能够改善抓取网站
效率的高级功能。然后介绍了 Portai， 它提供了生成 Scrpay爬虫的可视化界
面。最后我们试用了 Scrpeayl,Potira正是使用该库根据给定模型自动化抓取
网页的。
下一章中，我们将应用前面学到的这些技巧来抓取现实世界中的网站。
124第 9 章
总结
截止到目前，本书介绍的爬虫技术都应用于一个定制网站，这样可以帮助
我们更加专注于学习特定技巧。而在本章中，我们将分析几个真实网站，来
看看这些技巧是如何应用的。首先我们使用Goolg演e示一个真实的搜索表单，
然后是依赖 JavaSrci的pt网站 Facebo，接o下k来是典型的在线商店Gap， 最后
是拥有地图接口的宝马官网。由于这些都是活跃的网站，因此读者在阅读本
书时这些网站存在已经发生变更的风险。不过这样也好，因为这些例子的目
的是为了向你展示如何应用前面所学的技术，而不是展示如何抓取指定网站。
当你选择运行某个示例时，首先需要检查网站结构在示例编写后是否发生过
改变，以及当前该网站的条款与条件是否禁止了爬虫。
9.1G oolg搜e索引擎
根据第 4 章中 Alex的a数据，goolgeo.m是c全世界最流行的网站之一，而
且非常方便的是，该网站结构简单，易于抓取。
图 91.所示为 Goolge搜索主页使用 Friebgu加载查看表单元素时的
界面。第 9 章 总结
Goog国l际化e版本
Goog可l能e会根据你 的地理位直跳转到 指定国家的版本。要想
无论处 于世界任何地 方，都能使用一致的 Goog搜l索e， 那么
也
可以使用 Goog的l国e际化英文版本，其网址为htt:p//www.
goolge.com口／er其。中，nc表r示没有国家跳转（on
conutrreyd i）r。ect
Google
..创始 脚画’“ .、0，
阳血，碰咱 也比例
… … 惑：U
是 .P ....榈唰 .一町毗 e一鹏一徽阳 酣锵 m 一地 � … .. 一
lidor.c. "11也盔，•tt,arlti－'””据国，...ρ”’‘民，，常有伽1 “”。” ，·t�··o.俨鹏飞”“”“，. ，.崎·‘？” ”“阳们ρ崎句网、 .....叫“•1•r-oL…雌静．”加
.喝＇＂’”•H每伊．． 份协 lHi;•、“＂ld•"lffi!;俨》
.‘＂＂“M＞•飞警f'V'O'
"4” ζ耐＇t:＂＇• ＂＇到·�＇榈创树‘沁悦，崎佑LO翅·•饲在’I�＂＇U字”路，γ，
起唱“0$“$甘正•由ι"1"t1t输惧、峙。“2“＂＇＇楠悉’
:.,4jy创＇”’也感阜rl:!l•＇＂始知、
��价“… 1，伪E l) NJlb ’相 ＜＂ ”．．
4月4 t” 吨d 他W• 帽”辈毒 U但·” ＇‘’将‘mt ＇＂，梢”l＝ ”志.四伏＆ (Islti• i＞.la梅 伊’d 叭叭酬irJ-. .哈密 .· 且’都Z 庐”。IU ．抽调 川e"" .y、 �·t气M‘' ，.，，l ，’施’‘，＇tt• di阳h>
.. ＂r"•
也，，.，，，，..,.,.,.. .....帽Uct•
.制”插d惯也d*Hlh.，＇ �“地” 细细＂）.ft'_.,.
飞：�－；二；M ,.«i;:精盼陆楠精制崛制脚情耀糊钳制静蛐峨精酬’盼悔怖阳帽蝉噩 噩
辩阙娟懒畅销镶懈掰楠精树栋佛协制耐椭精明”－ 归曾于？””啊圈”F阴晴”咽理回哥”’帽”’ －
图 9.1
可以看到，搜索查询存储在输入参数 q当中，然后表单提交到 actnio
属性设定的／esarch路径。我们可以通过将 te作s为t搜索条件提交给表单对
其进行测试， 此时会跳转到类似 http:s//www.ogogl.ceoms/erach?=q
tesotq=&tset&essm= 9&3i=eUT-F8的 URL中。确切的 URL取决于你
的浏览器和地理位置。此外，还需要注意的是，如果开启了Goog实l时e， 那
么搜索结果会使用 AJAX执行动态加载，而不再需要提交表单。虽然 URL中
包含 了 很多 参数 ，但是只有用于查询的参数 q 是必 需 的 。当 URL为
http:s//www.goog.lceom/seahr?=cqtset时－，也能产生相同的结果，
如图9.所2示。
1449.1G oog搜l索e引擎
Googlel ost 4靡商
、！.＇idt'!:温’－”
W国b N•嘀嘀 Aµ庐· 阳”‘F宫 .... S."11d、lt1ol”
At>-.l1n2日00的回。，叫出’：02•0冉回碍’ ｝
Speed•lLenebly OokTlh•e G lolγal aBdrboanSdp eeTde sl
"°""·'"""-'s阻。P且"L'•回''"""· ...飞1.l.aoo••thai国1
l!-SICIW田n IUt'lllNH!-0!18四”。\005e B!n面9 ”四”’因意 ctgo呵＂＇＇＂幅lly d"pe响。
191"191$町咽，回 阶叠W宵”“四町，盹皇 剧”明..，.
My F警e纠＂＇但 凶。倒＇＂＂＂＂＂""＇""""
CTrtcoeHaTte mes lfso Orr gaz.anl !oTnraali ning and Certificatior
hl阳＂＂叫w le•t."-"'"
p＂＂r剧’•comi>l •恼，ltl\\o'3:电掣制曲，、阳，.......销也rietnt，，回mM＂＂咱
.. ，，，酬...，呻印制ali1ilc9llttlil:a11011树啕暗暗恫 uo012«阳噜脑11"
PeraonTaels”·tv同 umaMnetrics
,w,wJarmrn’..，.四，α，m t!识萨悦呻lyprJs2 .t<叩 ·
俨制唰’嗣同JH.＼阳＇＂�＇•CJ""“对9ι6现＂＇均咽，！’阳 院领呻. ..酣制 沪剧惘局
阳nm＂凶typo 归＇＂＇＇＂田、QUF"11α＂＂＇剧
•W•
Tested
twooomdl .
···�吧。．”’υ7且15Tw巾dh在....＂，飞＇m酬咔7 00011.rid晴＂＇民削 7回坷RC
，，...刑1田阳幽 γ回8回回oCom1阳＇＂＂嗣阳句’去阴雪 ？扭扭”
TToe副口sc缸t”r唱 ’i钮’c’＂-kWei＂tki 阳pedithae, t ree encyclopedia
凹’•oki阳＇币、.orgl州＂M汀＇＂国Z<.ricJ<＂＇el.消但呜冶tf＇言＇ ’
....剑 何贸m a’”E句阳阴 创Mci;r.:1Tll函’m.il:l:ll'w幡 nmp�iyMl>o":I＇＂＇号。”
r唰V-J..ntu\vtJ!i\:;.t”川巾’To.t山，，，. 肝由制呻唰.，...，
图 9.2
搜索结果的结构可以使用 Frieb来u检g查， 如图 9.所3示。
＇＂酬a
;J;.� 国回＠
c.. �.， 乓”TMLJ吟飞品和即鹅id。•＂＜•＼千雪二.附.芝～… .
m…《葛－…＇＂ ＞
"'<di•
＂＂＂＇•＂＇＂”I•
a <dl•> d"•srro＜＇，”
� <d>V.. .,.. .... ，.，”
4‘ol>b 吨l3.S5”，il.，C＂＇’
0 <l<ll r电•.•，
3最酷辙狲赚帽”曾自 跚跚赠解理费”阴阳”照�冒”鸭””理嚣曾想冒冒栩帽理照同归回理
‘，、，’，.
"''"''' ＇＂＂＂吨’〉
‘／U>
!.<U ＂＂＇＂”旷〉
"' <ll< \m•"o"•
"'"'"'""•.
<1c立飞＂＇归”，·〉
图 9.3
从图9.中3可以看出，搜索结果是以链接的形式出现的，并且其父元素是
cals为s”主”的＜h＞3标签。想要抓取搜索结果，我们可以使用第2章中介绍的
css选择器。
》＞ importl xml.html
》＞ from dowlnoader poirmtD ownlodaer
》＞ D =D owlno ade(r)
》＞ html= D（h’ttp:s//www.goolge.com/seahr?c=qtest’）
》〉 tree= lxml.html.fromstr土口g(html)
145第9章 总结
》＞ resul=t tsr e.escsseecl（th ’3.ra ’）
》＞ results
[<Elementa atO xf73d9eaafff8>,
<Elmeenat atO xf73d9ea8f9f0>,
<Elmeenat atO xf73d9ea8fef8>,
<Elmeenat atO x7f3d9eaaaff0>,
<Elmeenta atO xf73db9la698e>,
<Elmeenat atO xf73d99bcl85a>,
<Elmeenta atO xf73db9la90e>c,
<Elmeenta atO xf73db9laf918>,
<Elmeenat atO xf73d9bfl7a09>,
<Elmeenat atO xf73db9la9f]c 8>
到 目前为止，我们已经下载得到了 Goog的l搜e索结果， 并且使用 lxrnl
抽取出其中的链接。在图9.3中，我们发现链接中的真实网站URL 之后还包
含了一串附加参数，这些参数将用于跟踪点击。 下面是第一个链接。
》＞ lin=kresul[tO.s]egt （hr’e’f）
》＞ link
’u／rl=?hqtpt://www.speteeds.tent/
&sa=U&e=inmgqVgbC&wve=dOCB&AuCs_Agc=A'
这里我们需要 的 内 容是 htpt://www.speeteds.t口et／， 可以使用
urplars模e块从查询字符串中将其解析出来。
》＞ imporutr laprse
》＞ qs= urlpsae.rurlpa(rlsniek.)uq ery
》＞ urlpearp.sasre_qsq(s)
｛q’’ ：［h’ttp:/w/ww.pseedtte.esnt’／］ ，
’ie’：［n’mgVbqgC’w］ ，
’as': ［U’’］，
’sug’ ：’［CAAc A',]
冒evd’：［ ’CBO’］ ｝
》＞ urlrpsa.eaprseq s(sq). egt（q’’， ［）］
［h’ttp:/w/ww.pseetdes.tent’／］
该查询字符串解析方法可以用于抽取所有链接。
》＞ link=s l[
》＞ forr esuilntr esul: ts
16491. Goo搜g索l引e擎
=
linkr esu.gl et(t' rhe’f）
=
qs urplars.eurplasre(ilnk.)uq ery
lin.kesxte(unrdlpsae.raprseq s(sq). egt（q’’ ，［）］）
》＞ links
［h’ttp:/w/ww.speesdtt.eent／’，
’thtp:s//www.ets.tcom’／，
’thtp:/w/ww.test.ceodm’／，
’thtp:/w/ww.pseakyea.nsets/peteeds’t／，
’thtp://www.humaentmri.ccoms/cgwii /njtypes2.sap’，
’htt:/p/en.iwkiped.oirag/kwii/T_ecrsitcekt’ ，
’thtp:s//htlm5test.com’／，
’thtp:/w/ww.1p6ernsal。iite.scom/fre-epresnoalitys-t’t，e
’thtp:s//www.ogog.lceome/bwamste/rtsool/smboilfer-inedyl／’ ，
’thtp://pseeedst.tcocmas.tent’／］
成功了 ！从 Goolge搜索中得到的链接已经被成功抓取出来了。该示例的
完 整 源 码 可 以 从 htpts://bibtuck.erotg/wps/cwoed/scr/itp/
chpatre09/googl.eyp获取。
抓取Goolg搜e索结果时会碰到的一个难点是，如果你的IP出现可疑行为，
比如下载速度过快，则会出现验证码图像，如图9.所4示。
Toc oinntupele萝tyapest ehceah arctbeerwls:o
M伊拉
I 些些到
Abou伽t幅如醉
sysl随ns havde倒四恒d unusutra胃ical青田n归『UαllTlpU饱『
αIr
TI苦恼page d晤E恼t oseIfeI tre'asl yolyu s ending
network. ti回
阻qu眉tsanndo tr蚀。t WhVd itdh AiBsDOQ O?
a
图 9.4
174第 9章 总结
我们可以使用第7 章中介绍的技术来解决验证码图像这一问题， 不过更好
的方法是降低下载速度，或者在必须高速下载时使用代理，以避免被 Google
怀疑。
9.2F acbeook
目前，从月活用户数维度来看，Facebo是o世k界上最大的社交网络之一，
因此其用户数据非常有价值。
9.12 .网站
图 9.所5示为 Pac出k版t社的Fabcoeo页k面，其网址为 http:s//www.
facebko.coom/PatcPukb。
PEOPLE Ir吨�l.Pfack宫PubHshing
Sni:;
4,763i lk出
LearPnl aF.yr mae worfko frr eteo,d aγ1
ABOUT 〉 ,,_.. ...,.. ...， 叩 冈山－＇＼<Jll••,:111叩，..,. ,..,,,., ..，. .�M •a• U-11'
PacPkutb lisprho！v吨ibodoeksseBo.a ksv,i deo LearnPilnagFy r!a mew2o rk
tutoria•lnsda,• l lcfolreIT s d evelopers,
adm,,s,tlrotorasn,d u 白白 τheP layFr amew田k m•kos;eta<νM bu•ld w•b
•pplicatlw。intshJ ava>c a&la a,n dt h昭
htlp•//www.PackctaPmub/ um-frietnudtlomyra ik时al， ts;mpslbelrl
噩噩E噩噩噩噩盟军�
POSTST 。PAGE
飞！• ’V时la叭1dlqmu’r CShtrrlnsktle•lnj ［���］� 注目�cl�v凯；��A�
an"m ” an -
H• thSee<nyetol u m ai‘＇l＇ith my O;sue FREE LEARNING HELYPO URSELFI P ACKBTo oks
sa阳rdl町bougUhntity S四”。re Pael<PuIb l剧，plmnvgl1de四由阳leogByaobkso t帖an叽ddeeta< h创πp
，.口＜PUB c。但
Uke Comment Sharo
lJk• Commen1 S旧，但 ｛＇；.
E翻 …
γ。3a叫自2驴 、Jo、、拘n
I.P..阳A< .l P Ja Hc ＜lrt 忌P uhl四h1ng咄盯时 注ffnk
HII bgohutS oOwaDcee velopbmoeonakt« ，
y。utr>hrouA•gmha z 。n.c。”、sεgMo<e
LlkOC ommonSharet 01
图 9.5
当你查看该页的源代码时’， 可找以到最开始的几篇日志，但是后面的日志
只有在浏览器滚动时才会通过 AJAX加载。另外，Faceobo还k提供了一个移
1489.2F acebook
动端界面，正如第 l章所述，这种形式的界面通常更容易抓取。 该页面在移
动端的网址为 http:s//m.faceobo.kcom/PatcPukb，如图9.所6示。
L翩 白
品 － 国
·－‘’
J# 4回国响＂＂＂＂＇
AboA
＇同M梅，s＂制内＇＇＂＂草帽衍’咱阴阳翼，�l.�必诙防 部町陆，， .草1，侃”’阳臼白帽回.eo 5ea日也阳湖'1.antfu据阿
噎贯Z白雪苦而＇哩辛苦糟糟俨泪咱吨叮唁电汽－阳市τ－
国！吼：：.
圈圈
,
.•,
’＇•睬，，。俨...
岳阳’四 。如W由
P>oklP•bli•hl吨
S阳
t叫巧 I
＇＇＂＂＇＇＂＇＂肝�＂＂·�·...抱由驯
图 9.6
当我们与移动端网站进行交互，并使用 Frieb查u看g时，会发现该界面使
用了和之前相似的结构用于处理AJAX事件，因此该方法实际上无法简化抓
取。虽然这些 AJAX事件可以被逆向工程，但是不同类型的Faceb页o面o使k
用了不同的AJAX调用，而且依据我的过往经验，Faceb经o常o会k变更这些
调用的结构， 所以抓取这些页面需要持续维护。因此，如第 5 章所述，除非
性能十分重要，否则最好使用浏览器渲染引擎执行 JavaS事c件r，i然p后t访问
生成的HTML页面。
下面的代码片段使用 Sleenmi自u动化登录 Faebcoko，并跳转到给定页面
的 URL。
from selne工mu 工mportwebdirver
deff aceobok(usernmae, passwordu,r l) :
drive=r webdirver.Firfeox()
drievr.get(h'ttp:s//www.afceboo.kcom’）
drievr.find_elemetn_byi d（『ernai工’ ）.sendk eys(usernarn)e
drievr.finde lmeentb y id（p’ass’）e n.dsk• ey s(password)
drievr.finde lement by id（l’oginf or’m ）s ubrn工t（）
drievr.impliictlyw ait(30)
149第9章 总结
# waitu ntilt hes earhc boxi sa valiable,
# which meansh aves ucscseuflllyog geidn
=
searchd riv.eifrn_delernen_bty_id（ ’’q）
# nowl oggedi ns oc ang ot ot hep agoef i ntesrte
driv.eegrt(rul)
# adcdo dteo s crapdea tao fi ntreeshte re
然后，可以调用该函数加载你感兴趣的 Facebo页o面k，并抓取生成的
HTML页面。
9.2.A2PI
如第 1章所述，抓取网站是在其数据没有给出结构化格式时的最末之选。
而 Faceb提o供o了k一些数据的AP，I 因此我们需要在抓取之前首先检查一下
Facebo提o供k的这些访问是否己经满足需求。下面是使用 Facebo的o图k形
AP从IPack出t版社页面中抽取 数据的代码示例。
》＞ imporjt osn, pprint
=
》＞ hmtl D（ht’tp://grpah.afcebko.coomP/ackutb’P）
》＞ppirn.tpprin(tjons.olad(sthrnl))
{ua’bou’t：u ’PackPtub lsihinpgr oveisdb 。o,kesBoo,k vsideo
tutioarls,an da rticlfe。srI Td evle。per,sadrninsitr。art,sand
usesr.’ ，
uc’ateg’o：ru’yProudc/tsevric’e，
u’foundde': u’2040’ ，
u’di’ ：u’02460312’94，5 8
u’lieks’ ：4817,
u’link’ ：uh’ttp:/sw/ww.facoeob.kcom/Pacukb’tP，
u’imssoin’ ：u’eW heltph ew orlpdu ts oftwartoew orikn n eww ay,s
throutghhed eliver。yf effecitvel eanrinagn di nfomration
sevricse toI Tp roefsisona.l’s，
un'arne’：u’PackPtub lsihi’ng，
ut’aklin_gabot_uocun’t： 55,
uu『se口raern’：u’PakctP ub’，
uw’ebsiet’：u’thtp:/w/ww.aPcktPbu.omc’｝
该 AP调I用以JSNO格式返回数据，我们可以使用 json模块将其解析为
Pytho的ndiet类型。然后，我们可以从中抽取一些有用的特征，比如公司
名、详细信息以及网站等。
1059.G3a p
图形AP还I提供了很多访问用户数据的其他调用，其文档可以从Facbeook
的开发者页面中获取，网址为 httsp://developers.afcebook.com/
docs/garp-hap。i不过，这些 AP调I用多数是设计给与己授权的Facebook
用户交互的Facbeoo应k用的，因此在抽取他人数据时没有太大用途。要想得
到更加详细的信息，比如用户日志，仍然需要爬虫。
9.3G ap
Gap拥有一个结构化良好的网站， 通过 Sietmap可以帮助网络爬虫定位
其最新的内容。如果我们使用第 1章中学到的技术调研该网站，则会发现在
htpt:/w/ww.agp.ocm/robtos.txt这一网址下的robtos.xtt文件中
包含了网站地图的链接。
Sietma:p htpt:/w/ww.agp.ocm/prodsu/scittema_pinedx.xml
下面是链接的 Sitemap文件中的内容。
<?mxlv ersio＝口”.1”。enc。di”nUTgF-＝8”〉？
<stiemaipndexxml ns”＝htt:p//www.istempas.org/hseacms/seimpta/.0”9〉
<stiemap>
<lco>hpt:t//www.agp.com/purcot/dsstiemap._mxll/<loc>
<lamsotd>0215-0<3/-al0sm3tod>
</simtaep>
<stiemap>
<lco>hpt:t//www.agp.c。m/purctosd/tsemiap一.2mxl/<loc>
<lams。td>0215-0033-/<lamsotd>
</stiemap>
</stiemaipndex>
如上所示，Sietmap链接中的 内容仅仅是索引 ，其中又包含了其他
Sietmap文件的链接。其他的这些 Sitemap文件中则包含了数千种产品类
目 的链接，比如htpt://www.agp .ocm/pruocdt/sbleu-lnogs-leeve­
shitrsf-o-rmen. jp，s 如图9.所7示。
115第 9章 总结
阳由自时ING
··－面口I ©1 "" ""'"o•ov••• •S>o ..·．’ .．” ．‘一 .…， 咿喃胃＝w .－四 。‘－－·一 －ll
回 ......
SM1 '5怜-t-<CSl°;桐， ，伽阿•＜哈密相m缸巾 ，．，
E画画画画诅画副画画画画画…………·品画－凰缸且m.::::.I
23饵.，，，，
．
·也
�一 M•
．．崎 屿，.，阳!1.1..1....t
Worn阴晴 'ff阳
＇＂由
Gap Fil
Maternit..y.. ， ” ·w
j
Meo
BoG y巾 ·－－由…｜ d,..s.n .... ”. ’”…hf"'5 ｝，－ …叫'15 阳”m _,．、 .., ． .... ,、
s 卢 M
”’鸭 ，...”
Toddler
图 9.7
这里有大量要爬取的内容，因此我们将使用第4 章中开发的多线程爬虫。
你可能还记得该爬虫支持一个可选的回调参数，用于定义如何解析下载到的
网页。下面是爬取 Gap网站中Sitemap链接的回调函数。
from lxml importe tree
frmo thraede_dcrawleri mportt hraeded_rcawler
def scrap_ceallbac(kur,l html):
ifu rl.endswhit（.’mxl’：）
# Par =s et hes itemapX ML file
tree etre.efromstirng(html)
links= [e[O.]et xtf ore i口tree]
retu口rlinks
els:e
# Add scrapincgo de here
pass
该回调函数首先检查下载到的 URL 的扩展名。如果扩展名为.mxl， 则认为
下载到的URL 是 Sietma文p件， 然后使用 lxml的etre模e块解析 B任 文件
并从中抽取链接。否则，认为这是一个类目 URL ，不过本例中还没有实现抓取类
目的功能。现在，我们可以在多线程爬虫中使用该回调函数来爬取 gap.ocm了。
》＞ from thredaedc rawler importt hredaedc rawler
》＞ sitemap ＝ ’http://www.gap.com/pruocdt/sstiemap_ienxd.mxl’
》＞ threadedcrawler(stiemap, scrape callbackc=rsapec allback)
Downlaodin:g htt:p//www.gap.com/prodtus/csietmapl.mxl
_
1529.4
宝马
Dowlnoadin:g htpt://www.agp.com/purcot/dsstiemap2 x.ml
Dowlnoadnig: htpt://www.agp.com/purctosd/
cablen-itk-beanPi9e8 7.5j3p7s
Donwloadnig: htpt://www.agp.com/dpurctos/
2-in-1-rsitep-te9e8-P75.4jp4s
Dowlnoadin:g htpt://www.agp.com/purcot/dsboyefnrdij-eans-2.sjp
和预期一样，首先下载的是Sitemap文件，然后是服装类目 。
9.4
宝 马
宝 马 官方 网站 中 有一 个 查 询 本 地 经销 商的 搜 索 工 具， 其网 址为
htpts://www.mbw.de/de/hom.ethm?lentryTpye=odl,界 面如图 98.
所示。
’””阴胃’””MW I,_t•i’.. 因
BMWP artneirnl herrN ahe.
－－曲K圈M圈M＿�'皿 ＿
－” “”d..,_llenS lleh －”曲rw曲•nBMW h略....
,_.... . .... .... ..
� 由 国 ·－－同酬阳p 酬 怕回 国舶 Z咱呵
’酣． ．．” ’·帽， 叫·帽 a”．”
E植..........
..刷帽. ”·简而“’
一
5
．－ 命· ”
‘
’‘ lit伽H 、，
．”’” ＆组融k h．“国《，萨、蛐
-$？哪
帽同阳” 嗣M眩目 1
2损 也踹 :ic阳 •｝ De.也 曲－ ft、 栅？” 也“m嗣 吨 牛
、嚣鹏 呵f飞d』 地臼＂＂＂町 ’辄止 叫啕F中
…．‘ 害’ raE ne e’ 可；f�．边 .; ；；.＂;i ＂.＇！．． 可ii,I ia 幽由－ .if．． ＿- 喃� ,;自.. ;:．t回. 俨曲 :’ ·” - ’． . ＝且也 川蝠’” t嚣 』』＿－陆 「 ～ ＿， R一 ← o11→
11
tw 圃’自 嘟… ”’h”··”
图 9.8
该工具将地理位置作为输入参数，然后在地图上显示附近的经销商地点，
比如在图9.中9以Berli作n为搜索参数。
135第 9 章 总结
因
BMW D臼阳r >BMWif in阳drtners
BMW partneri ny oura re.a
Finad ndm anagey ourp e陌onaBlMW pa此neι In a
Youc 阳蜡arBchMW dealal一e回srt muepl ot hrBoMeW pa民 ne.-foundY ""M'yB MWa c<»-SunSl esys阳 画re
盼91.ruo皿rcdr
a MyWi陪hU引
L Sew四 」」S制
图 9.9
使用 Friebgu，我们会发现搜索触发了如下AJAX请求。
http:s//c2b-sev工rces.bmw.ocm/c2lboclasearhc/sevrice/sapiv/3/
clinets/BMWDIGIATL DOL/DE/
po工sc?ountr=yDE&categroy=BM&maexsRults9=&9al口guage=e口＆
la=t52.507537760858&681口0g=l3.425629 6305175 11
这里，maxeRsul参t数s被设为 99。 不过，我们可以使用第 1 章中介绍
的技术增大该参数的值，以便在一次请求中下载所有经销商的地点。下面是
将 maxRseult的s值增加到 100时0的输出结果。
》＞ url＝ ’http:s//c2b-ersv工ecs.mbw.com/
c2b-locaslearch/sevrice/sap／工v3/clnites/BMWIDGITALDLO/DE/
poisc?ounrty=D&Ecategoyr=BM&maxeRsul＝t毛sdl&anguage=en&
lat5=2.5075378786080&5l6ng=l3.425629637501151'
》＞ jsonp= D(url宅 l00)0
》＞ jsonp
’aclblack（｛s”tatu"s:{
｝）『
才549.4
宝马
AJA请X求提供了JSON格P式的数据，其中JSNOP是指填充模式的JSON
(J SOwNi tpha dd）i。n这g里的填充通常是指要调用的函数，而函数的参数则
为纯 JSNO数据，在本例中调用的是 callbac函k数。要想使用 Pyth的on
josn模块解析该数据，首先需要将填充部分截取掉。
》＞ imporjt osn
=
》＞ pur_ejson josnp[sjonp.inde（x（’ ’ ）1 :jos n.pridnex（’’）） ］
+
》＞ delaer=sjosn.lodas(purjeos n)
》＞ delaer.seky(s)
[u’statu’s，u ’coun’t，u ’trnasltaino’ ，dua’t’a， u’emtadat’a］
》＞ delaer［sc’ oun’t］
731
现在，我们已经将德国所有的宝马经销商加载到JSNO对象中，可以看出
目前总共有 731个经销商。下面是第一个经销商的数据。
》＞ delaer［sd’a ta ］’’［opis’］[ JO
{u’attbruitse’ ：｛u’businesTsypeCeosd’ ：［u’ON’， u『RP’］ ，
ud'istbruitoinBranc’he：［su’T，’u’F，u’’G］，’
ud’istrbiuitonCod’e：'uLN ’，
ud’istbruiti。nnPerairdt’：u’000’8，1
u’axf’：u’4＋9( 302)0 909-1210 ’ ，
uh’。empaeg’：u’thtp:/b/mwp-artrn.embw.ed/
nieedrlsaunsg-rblein-wseseins’ee，
u’ami’l ：u’ln.ebrl@ibnmw.de’ ，
uo’utleItd’ ：u’3’，
uo『uteltTypes’：［u’FU’］ ，
up’h。n’e：u’4＋9(302)0 0909’ ，
u’reuqestSveircse’ ：［u’FRO’ ，u’IRD’ ，u’OTA’］ ，
u’sevric’es：［ ｝］，
u’cateygo’：ru’MBW’ ，
u『cit’y：uB’erl’i，n
u’counyt’：ru’eGrmnay’ ，
u’conutrCyoed’：u’ED’，
u’ids’t： .656291033246061,
u『ke’y：u’000831’，
u’la’t ：52.56258636841,5
u’nlg’： 314.6358964670,7
un’aem’：uB’MWA GN ieedrlansgsB uerlFiinl iaWleie\ xfdens’e，e
up’ostoadleC’：u’130’8，8
u’strete’：uG’ehrintgr.s 20’ ｝
155第9章 总结
现在可以保存我们感兴趣的数据了。下面的代码片段将经销商的名称和经
纬度写入一个电子表格当中。
witohp e(n'= mbw .c sv’， ’w）’ asf p:
writerc s.vwrietr(pf)
writ.werrirt。e(w［Na’me’ ，’Lattiud’e， ’Lontguid’e］ ）
ford eal=eir n d eale［rds’a t’a ［］p’oi’s：］
name de=al e［rn’a me’.Jne coed ’（tuf-’8）
la,t lng deale［r’a lt’ ］d，ea le［r’n lg’ ］
wrietr.wrirtoe(w[ anm,e la,t ln]g)
运行该示例后，得到的bmw.scv表格中的内容类似如下所示。
Nam,eL attiud,Le ontguide
BMWA GN ieedrlsausnBge rlFiinl iale
Wei.Benes,5e25.628586364151,3. 643589646707
AutohauGsr abuamu GmbH,52.4528295,135.21625
AutohaRuesi erG mbH& Co. KG,52.56437,13.23521
从宝马官网抓取数据的完整源代码可以从http:s//bitb ucket.org/
wspw/ocde/scr/tpi/chpater09/bmw.py 获取 。
翻译外文内容
你可能已经注意到宝马的第一个截图 （ 见图9.）8是德文的，
而第二个截图 （ 见图9.）9是英文的。这是因为第二个截图中
的文本使用了 Goog翻l译e的浏览器扩展进行了翻译。当尝试
了解如何在外文网站中定位时，这是一个非常有用的技术．宝
马官网在经过翻译后，仍然可以正常运行。不过还是要当心
电二 Goog翻l译e可能会破坏一些网站的正常运行， 比如依赖原始值
的表单，其中的下拉菜单内容被翻译时就会出现问题。
在Chrom中e，Goog翻l译e可以通过安装GooglTernaslate
扩展获得；在 Fire中fox，可以安装 GoogelTranlsator
插件；而在IE中 ，则可以安装 GoogelTooblar此.外，
还可以使用 htpt://translat.eogogl.eocm进行
翻译，不过这样通常会打断原有功能，因为要从 Goog的l网e
站中获取相关内容。
1659.5
本章小结
9.5本 章小结
本章分析了几个著名网站，并演示了如何在其中应用本书中介绍过的技
术。我们在抓取 Goolge结果页时使用了css选择器，在抓取 Faebcoo页k面
时测试了浏览器渲染引擎和 AP，I在爬取 Gap 时使用了 Sitema，p 在从地图
中抓取所有宝马经销商时利用了 AJAX调用。
现在，你可以运用本书中介绍的技术来抓取包含有你感兴趣数据的网站
了 。希望你能够和我一样享受这其中的力量！
175构建辑程爬虫来并行爬取页面：
�n邮＝社电鳞
出 版
.A步虹医
ww.ew川I.co.nme
面�
•
�
ISBN 978-7-51-143719－口
注册奋礼，提交勘误送手只分
新书抢鲜，电子书罔步发售
投稿！＆馈邮箱 cont@aecptubit.com.cn
新浪微博 ＠人邮异步社区
cR川币『·工45ω7nnu
分类建议：计算机／程序设计／即tohn u一一U一 定价·41－ ∞一一 元f－u－
一U －
人民邮电出社版网址：www.pt.cporme.csns
R