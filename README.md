# ics-homework
## 第一次作业
### 作业要求
1. 中国地图、世界地图
⾃⼰设定喜欢的故事背景，或者是⾃⼰专业相关的统计数据，⾄少画出中国地图和世界地图，有兴趣
还可以扩展到其他国家或者中国的省市县区地区。
2. 组合图表
⾃⼰设定喜欢的故事背景，或者是⾃⼰专业相关的统计数据，⾄少画出⼀种组合图表
3. 词频统计图
选择⾃⼰熟悉领域的某⼀⻓篇⽂本进⾏某⼀类词的词频分析（也可选科研著作）
将结果可视化，可使⽤柱状图或词云，也可⽤课上未讲到的其他图表形式
4. ⽤GitHub发布个⼈⽹站
⽹站⾸⻚包含个⼈学号信息，以及上述三个作业的介绍说明⽂字和链接
每个作业包含⼀个或多个链接
注：也可以⽤其他公开的个⼈主⻚空间，只要能通过⽹址直接访问即可

### 中国地图、世界地图
[中国2022各省分GDP](https://github.com/xjudyc/xjudyc.github.io/blob/main/1%E4%BD%9C%E4%B8%9A1%20%E5%9C%B0%E5%9B%BE/%E4%B8%AD%E5%9B%BD2022%E5%90%84%E7%9C%81%E4%BB%BDGDP.html)
[世界GDP地图](https://github.com/xjudyc/xjudyc.github.io/blob/main/1%E4%BD%9C%E4%B8%9A1%20%E5%9C%B0%E5%9B%BE/%E4%B8%AD%E5%9B%BD2022%E5%90%84%E7%9C%81%E4%BB%BDGDP.html)
1. 中国地图的数据是2022年各省分的GDP总数，数据来源是[国家统计局](https://data.stats.gov.cn/easyquery.htm?cn=E0103)
学习了读取csv文件制作成列表
2. 世界地图的数据是近年的世界人均GDP，数据来源是[世界各国人均GDP排名_全球各国人均GDP历年数据_聚汇数据](https://gdp.gotohui.com/word/2)
本来想做总GDP统计，但是没有好用的现成数据
但是由于一些尚不明晰的原因，貌似没有颜色
**已解决**：由于pyecharts的工具无法识别出csv文件里的“国家地区”的中文名，只能转换成特定英文才能输入（由于工作量浩大，于是只做了人均GDP大于10000美元的大部分国家及地区）

### 组合图表
[北京天气](https://github.com/xjudyc/xjudyc.github.io/blob/main/1%E4%BD%9C%E4%B8%9A2%20%E5%9B%BE%E8%A1%A8/%E5%8C%97%E4%BA%AC%E5%A4%A9%E6%B0%94.html)
用北京2024-2及一些其他的天气数据制作而成，主要数据来源是[【北京气温】北京市全年各月气温走势统计查询 - 北京历史天气](https://www.tianqi24.com/beijing/history.html?eqid=ee1efa760002855c000000026470ceb2)
感觉2月份天气好多变，今年甚至下了雪，往年也是，感觉忽高忽低，然后一下就热起来
做这个主要是因为数据获取方便而且格式很好，比较符合组合图表的适用范围
虽然只是整理数据和调整的工作，还是好累心，经常不知道为什么就出来一个空白页啥也没有……
顺带调整了主题，好看

### 词频统计图
[人名统计](https://github.com/xjudyc/xjudyc.github.io/blob/main/1%E4%BD%9C%E4%B8%9A3%20%E8%AF%8D%E4%BA%91/%E3%80%8A%E6%82%B2%E6%83%A8%E4%B8%96%E7%95%8C%E3%80%8B%E4%BA%BA%E5%90%8D%E7%BB%9F%E8%AE%A1.html)
[人名词云](https://github.com/xjudyc/xjudyc.github.io/blob/main/1%E4%BD%9C%E4%B8%9A3%20%E8%AF%8D%E4%BA%91/%E3%80%8A%E6%82%B2%E6%83%A8%E4%B8%96%E7%95%8C%E3%80%8B%E4%BA%BA%E5%90%8D%E8%AF%8D%E4%BA%91.html)
用悲惨世界的文本做了人名的统计，非常喜欢的一本书，做这个主要是想看看雨果写这本书究竟是在干什么（雾）
做这种小说的词频统计真的心累，不仅是因为人物多次出现的时候可能用其他称呼指代
>如“主教”一词，在书中大多时候指称“卞福汝主教”，但也有少部分时候会指其他人

而且因为jieba分词的词性判断真的很令人恼火
>“阳光”“崇高”“滑铁卢”这些最开始都算做人名了（叹气）
>还有那种人家明明叫“格朗泰尔”，结果给人家分成“格朗”和“泰尔”，而且这两个词的出现次数还不一样
>更离谱的事“让·勃鲁维尔”和“勃拉什维尔”都只剩下了“维尔”

再者还有雨果写书到底有多少部分是主线这件事让人很难绷
>像“路易十六”出现次数比某些ABC中的某些人还要多
>而且雨果写的时候，要是写到了这种针对史实的议论，就会疯狂写这个人的名字，反而是故事里的主角的名字不会这么频繁地出现

除此之外还有很多问题：
1. 像如上述原因所导致的，很多人的统计并不符合事实，很多地方的其他称呼可能完全没有统计到
2. 尝试用象形柱状图做了一个，但是柱子之间好像分不开

## 第二次作业
感觉这次不难(
难得部分也是上次没解决的问题（
### 作业要求
作业——⽹⻚设计基础
选⼀部著作，可以是之前分析词频的作品，分析⼈物（或其他关键词）“共现”，⽣成关系图
⽤本次课学到的⽹⻚设计技术，设计⼀个简单的⽹⻚，放置关系图和相关说明
要求：
将课堂练习和课后作业要求完成的共两个⽹⻚放到github个⼈主⻚空间，并在⾸⻚加链接和
说明
提交⽅式：将⾃⼰的姓名、学号和作业⽹址上传⾄教学⽹本课程作业
截⽌时间：4⽉14⽇23:59

### 悲惨世界共现+关系图
[这里是链接](https://github.com/xjudyc/ics-homework/blob/main/2%E6%82%B2%E6%83%A8%E4%B8%96%E7%95%8C%E5%85%B1%E7%8E%B0%2B%E5%85%B3%E7%B3%BB%E5%9B%BE/%E5%85%B3%E7%B3%BB%E5%9B%BE.html)
**学会了jieba的自定义词典！**
本来珂赛特和芳汀在jieba分词后都出不来，现在好多了，还可以把伽弗洛什，格朗泰尔好好的分词了！
>但是雨果真的好能扯，所以把一些历史人物留下了，但是像“滑铁卢”“阳光”这种还是算了

然后是分类，本来没准备分类的，因为悲惨世界没有像三国演义那样明确的分类，但是为了突出**ABC的戏份不多**与**历史人物出现得很多**，于是做了这个分类

### 悲惨世界网页
[这里是链接](https://github.com/xjudyc/ics-homework/blob/main/2%E6%82%B2%E6%83%A8%E4%B8%96%E7%95%8C%E7%BD%91%E9%A1%B5/%E5%85%B3%E7%B3%BB%E5%9B%BE.html)
是之前做的汇总，也没整出什么新东西
但是学会了**框架**，把三个图放在了同一html里了！！

### 课堂练习
[这里是链接](https://github.com/xjudyc/ics-homework/blob/main/2%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A0/%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A0.html)
呃呃呃，插入图片没学会其他，只会用url，所以得把图片先发到一个网站上，但貌似发在github上不太行
然后是文字部分，因为看到了很好看的字体和样式，又没办法在html实现，于是都放在了图片里，但是图片被压缩的好严重（头痛）

## 第三次作业
