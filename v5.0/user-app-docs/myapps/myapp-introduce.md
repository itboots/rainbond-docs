---
title: 应用管理界面
summary: 应用组为用户自定义组，组中包含用户创建的各类应用。如用户自定义应用组名为商城应用，该组包含web应用于MySQL 服务。应用组与未分组界面存在差别：应用组界面包括拓扑图以及列表视图，默认以拓扑图展示，可切换至列表视图；未分组只含有列表视图。
toc: false
---



<div id="toc"></div>

##管理单元简介

- 在 **我的应用** 管理界面中，您能以 **应用组** 为单位分组管理您的应用。在创建应用的时候，您可以选择将应用创建到哪个应用组中。如果您没有选择应用组，则应用会创建到 **未分组** 中。云帮为所有的应用组设计了 **拓扑** 与 **列表** 两种视图模式，而 **未分组** 只有列表视图模式。
- 在 **应用组** 的内部，您可以部署多个 **应用** 。应用是为您提供服务功能的主体。应用之间也可以相互关联、提供依赖，通过这些搭配，可以为您提供更多更丰富的应用内容。应用是您可以管理的最小单元，在后文中的 **控制台选项** 中，每一种管理手段所针对的对象，都是当前的应用。
- 每一个 **应用** 都由一个或者更多的 **实例** 组成。这种集群化的部署方式，保证了应用的高可用性。

<center><img src="https://static.goodrain.com/images/acp/docs/user-docs/myapps/V3.5/myapp-managelogic.png"style="border:1px solid #eee;max-width:100%" /></center>

##应用索引

- **进入应用管理界面**  点击导航区中  **我的应用** 即可进入应用管理界面

<center><img src="https://static.goodrain.com/images/acp/docs/user-docs/myapps/V3.5/myapp-sidebar.png" style="border:1px solid #eee;max-width:100%" /></center>

- 在导航中，您可以选择您的 **应用组** 与其中的 **应用**

## 应用组界面

- 双击应用组，您就可以进入该应用组的界面。在您自建的用户组界面下，默认提供的是拓扑图视图

<img src="https://static.goodrain.com/images/acp/docs/user-docs/myapps/V3.5/myapp-group-interface.png" style="border:1px solid #eee;max-width:100%" />

- 图中元素的意义
  - **应用组名** 即当前应用组的名称，由您在创建时自定义。
  - **拓扑图** 当前应用组中的逻辑拓扑关系，在图中，您可以清晰的看到部署了哪些应用，应用中的实例的功能、运行状态，以及实例之间的网络连接关系、依赖关系。
  - **缩放** 动态缩放拓扑图
  - **分享** 将您自行构建的应用分享到云市[点击这里查看如何分享](http://www.kancloud.cn/good-rain/share2market/198574)
  - **更多** 提供更改组名、删除应用组、新建组的功能
  - **拓扑图/列表** 用于切换拓扑图视图与列表视图

<!--根据图中序号查看对应解释：

| 功能 | 序号 |          说明                                    |
| :---| :---| :------------------------------------ |
| 组名|      1   | 该组组名，在新增应用时新建或将应用添至已知组                |
|  拓扑图|    2  | 当前分组内的拓扑图，通过它可以直观的了解应用的逻辑关系，网络连接      |
|分享|      3    | 可以把当前的应用分享到云市，并且在**应用市场——分享的应用**中可以看到 |
| 更多 |    4   | 包括修改组名、删除当前组、新增组。删除当前组后组内应用转至未分组中     |
| 切换视图 |   5   | 在此处切换视图模式，有分组的情况下默认拓扑图模式，未分组只有列表模式   |
| 自定义拓扑图大小 |  6 | 通过滑动原点或点击"➕"、"➖"符号实现对拓扑图的放大与缩小        |-->

### 拓扑图视图

- 当您点击某个实例之后，由这个实例所参与构建的整个应用的拓扑就会放大显示，并调出您点击实例的状态。这种视图方式便于让您了解应用或者实例之间的逻辑关系、网络拓扑。如果您更关心这些，请使用拓扑图视图

<img src="https://static.goodrain.com/images/acp/docs/user-docs/myapps/V3.5/myapp-toplgic.png" style="border:1px solid #eee;max-width:100%" />

- 在图中，您可以清晰地看到当前 **WordPress** 实例的运行情况，除了运行状态之外，您也应该关注其它部分：
  - **服务** 该栏提供了一个URL和一个端口，通过它们，您就可以在浏览器里直接访问您的应用。如图中，访问80.gr05d803.demo.ali-hz.goodrain.net 这个链接，即可登陆 WordPress 
  - **依赖服务** 该栏说明了当前实例所提供的服务，还需要哪些其他服务的支持才能生效，这就是依赖服务。如图中， WordPress 需要 MySQL 所提供的数据库服务支持才可以正常运行。**特别提醒，当您想关闭您的应用的时候，请先将依赖服务全部关闭**
  - **实例** 该栏显示了当前实例的ID与内存消耗情况。

### 列表视图

- 当您切换到列表视图下的时候，将会把该应用组下的所有实例以列表的形式列示出来。在这里，您可以通过多选的操作实现批量重启、关闭、启动。如果您想要对应用组内的多个应用进行批量操作，请使用列表视图。 **特别提示**，未分组的应用，会统一在 **未分组**  的应用组中以列表视图显示

<img src="https://static.goodrain.com/images/acp/docs/user-docs/myapps/V3.5/myapp-listmode.png" style="border:1px solid #eee;max-width:100%" />

- 图中元素的意义
  - **批量操作** 通过多选之后，在这里进行批量重启、关闭、启动的操作
  - **信息列表** 列示了单个应用当前的信息，包括应用类型、内存、状态、更新时间
  - **操作** 对单个应用进行重启或关闭的操作