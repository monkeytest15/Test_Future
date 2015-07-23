  其实移动互联网认识我的人都知道，我很少去扯那些没有发生，没有实现，
  虚幻的东西，所以这次谈测试的未来，上下文我要说清楚，我只去谈移动互联网的测试的未来。
  在这些年我基本上去和各个公司的同学都做过交流，经过了长时间的交流基本上能够对现状有一个清楚的了解，从而能够大胆的对未来进行推测。
  测试行业还是一个不成熟的行业，学术界和工业界都存在着大量看不清客观事实的人，同样的也存在大量的扯淡的人，本篇文章希望大家都能够认清楚
  现在的局势以便能够更好的认清楚方向去学习从而将行业整体推向一个正确的方向。
  
前言
---
  我自己是从09年底开始接触Android无线应用的功能测试，那么我就从那个时间开始说起吧。09年到11年底应该是属于移动互联网测试在中国的第一个阶段，那个阶段几乎网络上除了Android，iOS的官方文档不存在其他任何相关的测试技术博客或者文档，这对当初接触这个行业的我们是一个非常大的挑战。对于一个未知的领域，为了保证产品质量，测试必然是从功能方面切入进行测试。不过好在那个时期的App大多都是纯Native的逻辑，并不像现在那么的复杂。但由于开发整体技术的不成熟以及硬件上不充分的支持，我们最常见的其实就是OOM（Out Of Memory），那个时期真的算是习以为常了。
  
  为什么说09年到11年底基本上属于移动互联网测试的第一阶段呢？整个行业的大部分互联网公司感觉到了移动互联网的到来，这个时候国内很多初创的企业开始立志于做移动互联网的产品，为了生存，其中一部分公司采取了在国外智能机上预装自己应用的策略，从而保持公司正常的运作。从现在回过头去看，这真的是个不错的手段，的确让国内很多初创公司度过了当初那段国内移动互联网还没有火起来的时间。我们还是言归正传来说测试吧，这个时候很多大企业也觉得应该去储备为了将来奋战移动互联网的团队和技术基础了，所以开始大范围招人。初创企业招入的测试肯定是One Man One Team，而大公司的话会将自己公司内以往做服务端或者Web的经验丰富的测试拉过来做一个移动无线的团队的leader，然后开始招兵买马。但无论是哪一类公司，测试活动肯定集中在功能测试用例的设计，执行测试用例上，而且非常的累。所以当时如果你会或者说掌握（这里我不得不提一句，我面试了那么多的人，大部分人就是知道基础的命令，也不知道Monkey执行的策略包括实现，这些人请不要和我说掌握或者熟练）Android Monkey测试以及iOS的Monkey测试的话，那么已经是神一样的技能了，很多公司会争先恐后的抢着要的。在移动互联网早期，功能测试就被放在了一个很低的位置，直到现在依然没有什么一个很好的改观。其实各个公司在做了快2年左右的时间之后，就发现移动互联网不如自己以前想的那么赚钱，反而烧钱很快。11年下半年部分开始就开始裁员了，当然首当其冲的还是测试工程师。在这个第一阶段中，几乎所有公司都不知道自己要招什么样的人，JD的描述都会很模糊，要移动互联网测试经验等。整整2年就处于这样的一个阶段，我称之为这是测试第一阶段。
