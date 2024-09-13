# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 11112ssm影院在线售票系统

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Kp48e9EtU?p=13)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

电影院售票网站工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。电影院售票网站的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、用户管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3用户管理实体图

2、即将上映管理实体图如图4-4所示：

![](/md/blog.015.png)

图4-4即将上映管理实体图

3、订单管理实体图如图4-5所示：

![](/md/blog.016.png)

图4-5订单管理实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1：allusers表

|列名|数据类型|长度|约束|
| - | :-: | :-: | :-: |
|id|int|11|PRIMARY KEY|
|username|varchar|50|DEFAULT NULL|
|pwd|varchar|50|DEFAULT NULL|
|cx|varchar|50|DEFAULT NULL|
表4-2：yonghu表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|PRIMARY KEY|
|addtime|varchar|50|DEFAULT NULL|
|yonghuming|varchar|50|DEFAULT NULL|
|mima|varchar|50|DEFAULT NULL|
|xingming|varchar|50|DEFAULT NULL|
|xingbie|varchar|50|DEFAULT NULL|
|touxiang|varchar|50|DEFAULT NULL|
|shouji|varchar|50|DEFAULT NULL|
表4-3：zhengzaishangying表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|ID|int|11|PRIMARY KEY|
|addtime|varchar|50|DEFAULT NULL|
|dianyingmingcheng|varchar|50|DEFAULT NULL|
|leixing|varchar|50|DEFAULT NULL|
|haibao|varchar|50|DEFAULT NULL|
|daoyan|varchar|50|DEFAULT NULL|
|zhuyan|varchar|50|DEFAULT NULL|
|shangyingriqi|varchar|255|DEFAULT NULL|
|pianzhang|varchar|255|DEFAULT NULL|
|dianyingyugao|varchar|255|DEFAULT NULL|
|dianyingjianjie|varchar|255|DEFAULT NULL|
|fangyingting|varchar|255|DEFAULT NULL|
表4-4；jijiangshangying表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|PRIMARY KEY|
|addtime|varchar|50|DEFAULT NULL|
|dianyingmingcheng|varchar|50|DEFAULT NULL|
|leixing|varchar|50|DEFAULT NULL|
|haibao|varchar|50|DEFAULT NULL|
|daoyan|varchar|50|DEFAULT NULL|
|zhuyan|varchar|255|DEFAULT NULL|
|dianyingyugao|varchar|255|DEFAULT NULL|
|shangyingriqi|varchar|255|DEFAULT NULL|
|pianzhang|varchar|255|DEFAULT NULL|
|dianyingjianjie|varchar|255|DEFAULT NULL|

#########
# 5统详细设计
## 5.1用户前台功能模块
电影院售票网站，在系统首页可以查看首页、正在上映、即将上映、电影资讯、个人中心、后台管理、客服等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1用户前台功能界面图



用户登录、用户注册，在注册页面可以填写用户名、密码、姓名、手机等信息进行注册，如图5-2所示。

![](/md/blog.018.png)

![](/md/blog.019.png)

图5-2用户注册、用户登录界面图
#########
个人中心，在个人中心页面通过填写用户名、密码、姓名、性别、头像、手机等信息进行更新信息、退出登录，如图5-3所示。在正在上映页面通过填写电影名称、类型、海报、导演、主演、上映日期、片长、电影预告、放映厅、场次、价格、座位总数等信息进行立即预定操作，如图5-4所示。

![](/md/blog.020.png)

图5-3个人中心界面图

![](/md/blog.021.png)

图5-4正在上映界面图

确认下单，在确认下单页面通过填写购买商品、价格、座位、总价等信息进行支付，如图5-5所示。在即将上映页面通过填写电影名称、类型、海报、导演、主演、电影预告、上映日期、片长、电影简介等信息进行点我收藏操作，如图5-6所示。

![](/md/blog.022.png)

图5-5确认下单界面图

![](/md/blog.023.png)

图5-6即将上映界面图


## 5.2管理员功能模块
管理员登录，通过填写用户名、密码、角色进行登录，如图5-7所示。

![](/md/blog.024.png)

图5-7管理员登录界面图
#########
管理员登录进入电影院售票网站可以查看首页、个人中心、用户管理、电影类型管理、放映厅管理、正在上映管理、即将上映管理、系统管理、订单管理等信息。

用户管理，在用户管理页面中可以通过填写用户名、密码、姓名、性别、头像、手机等内容进行修改，如图5-8所示。还可以根据需要对电影类型管理进行详情，修改等详细操作，如图5-9所示。

![](/md/blog.025.png)

图5-8用户管理界面图

![](/md/blog.026.png)

图5-9电影类型管理界面图
#########
放映厅管理，在放映厅管理页面中可以查看放映厅等信息，并可根据需要对已有放映厅管理进行修改或删除等操作，如图5-10所示。

![](/md/blog.027.png)

图5-10放映厅管理界面图
#########
正在上映管理，在正在上映管理页面中可以查看电影名称、类型、海报、导演、主演、上映日期、片长、电影预告、放映厅、场次、价格、座位总数、已选座位{用号隔开}等信息，并可根据需要对已有正在上映管理进行修改或删除等详细操作，如图5-11所示。

![](/md/blog.028.png)

图5-11正在上映管理界面图
#########
即将上映管理，在即将上映管理页面中可以查看电影名称、类型、海报、导演、主演、电影预告、上映日期、片长、电影简介等内容，并且根据需要对已有即将上映管理进行详情，修改或删除等详细操作，如图5-12所示。

![](/md/blog.029.png)

图5-12即将上映管理界面图
#########
轮播图；该页面为轮播图管理界面。管理员可以在此页面进行首页轮播图的管理，通过新建操作可在轮播图中加入新的图片，还可以对以上传的图片进行修改操作，以及图片的删除操作，如图5-13所示。

![](/md/blog.030.png)

图5-13轮播图管理界面图
#########
订单管理，在订单管理页面中可以查看订单编号、商品名称、商品图片、购买数量、价格/积分、折扣价格、总价格/总积分、折扣总价格、支付类型、状态、地址等内容，并且根据需要对已有订单管理进行详情，修改或删除等详细操作，如图5-14所示。

![](/md/blog.031.png)

图5-14订单管理界面图













