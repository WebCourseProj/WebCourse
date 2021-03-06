# Task5 Web应用架构设计

## 一、层次架构

本次web项目系统设计我们采用的层次架构为三层架构，即为了符合“高内聚，低耦合”思想，把各个功能模块划分为展示层（UI）、业务逻辑层（BLL）和数据访问层（DAL）三层架构，各层之间采用接口相互访问。

展示层位于三层构架的最上层，与用户直接接触，主要是 B/S 信息系统中的 Web浏览页面。展示层实现用户界面功能，将用户的需求传达和反馈，保证用户体验。西电在线考试系统在前端系统中实现学生考试系统以及管理员系统网站页面的展示。在本系统展示层的实现过程中，我们使用的工具包括：

1、新版Vue框架，使用了vue-cli4搭建的系统，减少大量配置文件

2、Vue UI框架element-ui 3、Vue-element-admin 深度定制版

4、echarts 图表统计

5、ueditor 深度定制版。

业务逻辑层的功能是对具体问题进行逻辑判断与执行操作，接收到表现层 UI 的用户指令后，会连接数据访问层 DAL，访问层在三层构架中位于表示层与数据层中间位置，同时也是表示层与数据层的桥梁，实现三层之间的数据连接和指令传达，可以对接收数据进行逻辑处理，实现数据的修改、获取、删除等功能，并将处理结果反馈到表示层 UI 中，实现软件功能。西电在线考试系统在业务逻辑层完成了用户模块、问题模块、教育模块、班级模块、试卷模块、消息模块以及文件存储模块。在本系统业务逻辑层的实现过程中，我们使用的工具包括：

1、spring-boot 2.1.6.RELEASE

2、spring-boot-security用于用户登录验证

3、web容器undertow

4、Redis作为通用组件的一部分，用于实现缓存功能，提升系统性能

5、数据库中间件mybatis

6、数据库连接池hikari

7、七牛云存储，也是作为通用组件的一部分用于分布式文件存储中心。

数据层是数据库的主要操控系统，实现数据的增加、删除、修改、查询等操作，并将操作结果反馈到业务逻辑层。西电在线考试系统在数据仓储中实现系统中所有信息包括考试信息、用户信息等内容的存储。在本系统数据层的实现过程中，我们使用的工具包括：

1、开源数据库PostgreSQL

2、Redis用于实现缓存功能，提升系统性能。

## 二、展示图

![img](https://camo.githubusercontent.com/6fd4871a256d0902458061e4866ee40448beda4c9ccd605f8c35bbffb7a32be4/687474703a2f2f6d2e717069632e636e2f7073633f2f5635326c67683672323948316a46335543714f6d3376334d745a327241474c542f546d455567746a39454b362e375638616a6d5172454d51786d766d6354386a774b2e6664577541564c552a494e637a387052487743674c454b43626e6c364434314541644a4e527a7169536841455a632e57764f346d4e4d4250642e7274624543565831414f5630307234212f6226626f3d396748664167414141414144467867212672663d7669657765725f34) ![img](https://camo.githubusercontent.com/92694aecee9c9b167dcd62b20d5ffcb34ee96849b15547c964d5973087fdbb87/687474703a2f2f6d2e717069632e636e2f7073633f2f5635326c67683672323948316a46335543714f6d3376334d745a327241474c542f546d455567746a39454b362e375638616a6d5172454734434e33624f3355586c7559555a49683355502a69557650595457525a76534f77306a355a5a46395a2e6658564d51674b417a75694a38377734486a7043556539596b634e44664b7a4c46533053707443546a334d212f6226626f3d397745424177414141414144463859212672663d7669657765725f34)