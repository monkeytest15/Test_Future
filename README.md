# 移动测试的未来：去测试化

备选题目： 移动测试的未来：测试开发化

标签（空格分隔）： 移动 移动测试

作者：陈晔

---

首先说明，测试包括很多领域，这次谈测试的未来，我只谈移动互联网测试的未来。这些年我和很多公司的同学都做过交流，经过了长时间的交流，基本上对现状有一个清楚的了解，这里就大胆的对未来进行一个预测。 

另外我还想说，测试行业还是一个不成熟的行业，学术界和工业界都存在着大量看不清客观事实的人，同样的也存在大量的扯淡的人，本篇文章希望大家都能够认清楚现在的局势，以便更好的认清方向去学习，从而将行业整体推向一个正确的道路上。

## 移动测试的过去：从极易到极难

要预测未来，我们首先必须对过去和现状有一个清晰的了解，所以，下面首先介绍一下移动测试过去是什么样的。

我自己是从09年底开始接触Android无线应用的功能测试，那么就从那个时间开始说起吧。

09年到11年底应该是属于移动互联网测试在中国的第一个阶段，那个阶段几乎网络上除了Android、iOS的官方文档，不存在其它任何相关的测试技术博客或者文档，这对当初接触这个行业的我们是一个非常大的挑战。

对于一个未知的领域，为了保证产品质量，测试必然是从功能方面切入进行测试。不过好在那个时期的App大多都是纯Native的逻辑，并不像现在那么的复杂。但由于开发整体技术的不成熟以及硬件上不充分的支持，我们最常见的其实就是OOM（Out Of Memory），那个时期真的算是习以为常了。

09年到11年的时候，整个行业的大部分互联网公司都感觉到了移动互联网的到来，这个时候，很多大企业也觉得应该去储备移动团队和技术基础了，所以开始大范围招人。

初创企业招入的测试肯定是One Man One Team，一个人就相当于一个团队，而大公司的话，会将自己公司内以往做服务端测试，或者Web测试经验丰富的人，拉过来做移动测试团队的leader，然后开始招兵买马。

但无论是哪一类公司，测试工作肯定集中在功能测试用例的设计，执行测试用例上，而且非常的累。所以当时如果你会或者说掌握Android Monkey测试以及iOS的Monkey测试的话，那么已经是神一样的技能了，很多公司会争先恐后的抢着要的。（这里我不得不提一句，我面试了那么多的人，大部分人就是知道基础的命令，也不知道Monkey执行的策略包括实现，这些人就不要说掌握或者熟练了。）

在移动互联网早期，功能测试就被放在了一个很低的位置，直到现在依然没有什么一个很好的改观。

其实各个公司在做了快2年左右的时间之后，就发现移动互联网不如自己设想中的赚钱，反而烧钱很快。11年下半年部分公司就开始裁员了，而首当其冲的就是测试工程师。在这个第一阶段中，几乎所有公司都不知道自己要招什么样的人，JD（岗位描述）都会很模糊，会写上要移动互联网测试经验，但不知道具体要什么经验。整整2年就处于这样的一个阶段，我称之为这是移动测试第一阶段。

接着12年开始到13年底基本上又是两年，进入了第二阶段。

这个阶段，移动互联网的项目迭代周期也基本定型了，1～2月内一次大迭代，小版本可能每天都有。此时的公司对移动测试的要求也开始具体化——当然，中国是一个跟风严重的国家，比如当初BAT或者各个大公司写出来具体的测试JD，行业的其它公司纷纷开始抄袭，所以这阶段的移动测试的要求基本是从BAT出来的。

12年开始，对测试人员的招聘要求来了一个180度的转变，Robotium，Monkey，Monkeyrunner，Instrumentation，Object-C，Java，Python等各种详细的要求接踵而来，整个12年的面试会给测试人员一个感觉———面试测试岗位比面试一个CTO岗位都要累。记得某些公司在面试测试人员之前，首先先要笔试，做各种卷子，包括软件工程，测试，算法，代码，智力题等，从我看来简直变态的可以。

另一方面，移动互联网的产品本身从Native开始慢慢的转变成部分Native，部分WebView。Native主要用来实现一些类似于设置、本地界面框架的功能，而WebView更多的会做一些活动界面，广告投放的功能。之后Hybrid混合式应用就变成了移动互联网应用的主流实现方式。测试工作也从以往的纯功能性测试增加到现在的自动化测试、持续集成、碎片化测试等等。移动测试的技术在这段时间也得到了非常大的进步和提升。

其实在这两年里，还有一个事情让所有人都感觉到非常大的变化，那就是开源的测试技术越来越多。现在很多刚进入移动互联网的测试人会发现单是UI自动化测试就会有十几二十几个框架，根本就不知道选什么。

## 移动测试的现状：关注性能、平台化

最近的一年又有了什么变化呢？

从我了解的情况看，各个公司的关注点慢慢从功能测试转到专项测试，又从以往单纯去做UI自动化框架的开发发展到了测试平台化，发展到了线上监控。

行业大部分公司前几年都在做什么呢？招聘业务测试人员，大批量的招聘所谓的自动化测试工程师。整个团队分成两部分—————测试团队和工具团队（这里不得不吐槽，其实实际情况是工具组的大部分所谓的测试开发工程师其实就是开发，并没有太多测试的sense）。从2011年百度等公司就开始陆续这样去分团队工作，几年下来的确有着不错的积累，比如各个公司属于自己的框架和平台都搭建起来了，但各个公司在大会上面给大家看到的着实是幸福的一面。这样的分工就如双刃剑，让我来和大家说下另外一面吧。

第一点相信很多人心里也都知道，也就是两个组总是不能非常融洽的合作，总有互相的抱怨。所谓一个巴掌拍不响，双方都存在问题。
* 业务方的同学抱怨工具组做的工具不落地，不能触及到业务功能测试的痛点
* 工具方的同学不停的输出工具，更多的从架构层代码层去改进工具，却忽略了业务的实际真正的用途
* 业务方和工具方的同学互相不服对方，这点很实际。业务同学大多拼体力拼业务，工具方大多拼技术拼实现，但两者薪资会有一定的差别，公司的重视程度也会有一定的差异，这其中不见得一定哪方好哪方不好，得看公司。

工具组的同学唯一难过的一点就是他们大多并没有自己实际的KPI，更多的是看多少能在业务方落地，也就是说KPI其实是依附于业务方的同学，那么合作就变的尤其重要，但从上面的现状我们看得出来这并非易事。

第二点可能很多人就未必知道了。在移动互联网，工具组的同学无非做两样东西————二次开发自动化测试框架和测试平台（兼容性，自动化，监控等）。先说框架这个东西，如果仅仅是API层面的框架，那么的确能够长期有效的使用下去。但移动互联网中工具组大多做的是什么类型的框架呢？你猜对了，正是UIAutomation Framework，过程很黄很暴力，我就不多说了，我们来说结果吧。结果大多就是业务方用着也不是很爽，所以不停的给工具组提需求，工具组大多数服务的不止一个业务方，为了KPI只能不停的去接需求，最终导致还没有满足业务方的情况下，工具组团队先跪了，原因是需求根本来不及满足，Bug也根本就修不完，不停的恶性循环。


行业里的公司慢慢的发现，自己在功能测试上基本都有了一定的积累，开始关注应用的性能，因为性能直接关系到用户体验。同时，行业也意识到功能测试和自动化应该是测试人员的基本能力，而不是一个加分项。

所以到了14年，其实很少看到再有公司要招单纯的自动化测试工程师了，就算有，招入进去的也会承担更多的职责。虽然我很难确认这到底是不是一个进步，但是国内测试行业之前一直很混乱，伸手党横行，大多数人属于自己根本不能自理的状态，所以从这个角度来看，整个行业的技术能力要求提升，算是一个非常不错的趋势了。关于测试行业到底有哪一些捣乱的人，可以移步[测试行业感谢有你](https://testerhome.com/topics/2660)。

不过近期我走访的各个公司中的部分也已经走过了这混乱的过程，改变了自己的策略。现在的工具组，平台组不再去不停的满足各个业务线团队的需求了，而是搭建公共平台的前端的展示，后台数据库的存储以及给业务线的公共SDK。各个业务线根据自己的需求基于SDK来做封装从而达到自己的需求。这样平台组的压力也小，更好的关注平台本身的建设和SDK的封装，各个业务线也让真正熟悉业务的同学去做真正能在业务线落地的工具、框架等。

## 移动测试未来：找出问题还不够，要定位问题

了解了移动测试的过去和现状，现状可以大胆的预测未来了，不过，这里也仅仅是未来三年内的情况。

首先，测试人员肯定是朝着全栈的方向去发展了，这点毫无疑问。而功能（业务）测试，专项测试，自动化测试等都会变成一个测试人员的基本的能力，而非加分项。

**这里希望扩充一点，之前谈的去测试化，观察到的BAT测试人员的现状等**

而随着网商的发展，各类互联网＋金融的崛起，移动安全的测试将会变成专项测试之后的一个新的关注点。

测试人员自我能力的提升，也不再是单纯的某一方面技术，而是这些技术如何真正的落地，以及怎么结合自己的业务，以及产品的实现框架去排查和定位问题，最终解决问题或者优化产品性能。

将来不会再有单纯的业务测试，也不会再有单纯的自动化测试，以后测试将全部是测试开发工程师，这些人可以快速的去适应各种需求，并且能够通过业务和技术的双向分析从而定位真正所在的问题。

举个例子，随着React Native和Html5的发展，很多公司为了满足应用的需求，会开发私有的RCT和WebView容器。同时，很多业务复杂的公司的客户端，背后对接的不仅仅是一个服务，更多的是服务群。那么这个时候问题就出现了：

我们发现了一个客户端很卡，或者有某些安全的风险，那么，我们首先需要去从业务角度分析，可能是哪些业务链路上出现问题，接着我们需要去将被测产品拆开，一个一个排查和定位问题。比如

* Native Activity View启动消耗
* RCT转换到Natvie控件的消耗
* WebView自定义容器的消耗
* Html中的CSS，JS，PNG等流量和时间的消耗
* Native业务代码调用RPC，http请求的方法的消耗
* 本地请求到得到返回的时间消耗
* 数据交互的Json结构是否复杂，json解析的消耗
* 本地业务逻辑是否编写恰当
* 客户端在智能机上的界面绘制的消耗
* 整个架构View是否存在重复绘制
* 服务群中互相交互以及透传的逻辑是否恰当
* 服务群中的系统超时机制是否恰当
* 服务群中每个系统的消耗

我们会发现，其实我们并不能一下子就能够找到问题在什么地方，而是需要对业务和被测应用技术了解的情况下，去慢慢排除哪些地方没有问题，从而最终定位问题所在。此时的你光有技术，或者你光懂业务，都无法去完成这样一个工作。测试人员很大的一部分价值会体现在这个地方。

也许看到这里，很多测试同学就要跳起来了，觉得要求怎么那么高，感觉就在扯淡，肯定不是这样。我想说的是：

第一，目前测试圈很多人以为自己的圈子就是这个行业的全部，但其实测试的内涵比他们想象的要大的多。

第二，很多人被培训忽悠（什么自称xxx培训第一），觉得单纯的学习技术就可以提升价值，你们自己想想看，测试真的只是一个纯技术岗位吗？

第三，国内测试原本长时间存活在低要求环境中，导致很多人已经不知道正常的要求是什么了，当行业开始以正确的标准来要求的时候，就感觉无法接受。

大家只要抛弃成见，自然知道谁对谁错，也会知道应该怎么去面对未来，只要勇于承认，并且快速学习，未来的测试仍然有你的一席之地。

说到这里，很多测试管理者可能会问，管理者的出路在何方。

其实对于管理者而言，现在应该已经有所感受了，就是纯管理角色在移动互联网很难存活下去。原因有两个，其一，测试本身的技术定位要求，以及技术的更新速度会倒逼着管理者需要有一定的技术基础，包括对一些新技术有一定的了解，否则如何将合适的人安排在合适的位置上呢？又如何去服众呢？其二，未来的转变不仅仅是测试技术和业务的融合，更多的是就业人员从85后转变成了90后以及95后。以往很多管理者觉得给员工一些钱，一些股票，这些员工就会默默无闻的为公司卖命，为项目去加班。但是随着时代的发展，现在很多的年轻人看重事情变成：工作是否开心以及是否对自己有提升。他们不是不在乎钱，但他们会变的更有自己的想法和追求。面临这样一群人，管理者本身的管理方式也需要有一定的改变，同时需要从公司的流程，业务发展，个人规划，技术发展等各个角度去给出一些引导。

差不多以上就是我想表达的观点了，也许很多人已经看到了变化，也许很多人没有，但是无论如何，变化总在快速的，不以任何人的意志而转移的进行下去。最后，如何想了解更多移动测试发展的话，可以关注我写的书《大话移动App测试2.0——技术篇》，会在明年上半年出版，这会是全新的一本书。粗略的目录可见： [大话移动App测试2.0目录](https://testerhome.com/topics/2095)。其中我也会将这次我全程参与钱包9.0研发过程中的一些经历和技术写在里面。




