---
title: "作业管理列表"
linkTitle: "作业管理"
description: hpc的作业管理
keyword: 云计算, 青云, QingCloud, HPC，作业管理
draft: false
weight: 10
---

作业是用户在 HPC 或 EHPC 集群中提交的一个计算任务，作业在相应的集群队列中运行并输出结果。集群会对其中的作业进行统一的调度管理。

登录高性能计算 的**作业管理**页面，可显示当前集群的所有作业，系统提供两种提交作业的方式**界面提交**或**CLI提交**。


## 查看作业列表

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **计算** > **高性能计算 HPC**，默认进入**高性能计算 HPC** 的**集群管理**页面。
   ![cluster_manage](../../../_images/cluster_manage.png)

3. 点击左侧导航栏中的**作业管理**，进入作业管理页面，默认显示当前 HPC 和 EHPC集群中所有作业列表。

   ![joblist_1](../../../_images/joblist_1.png)

  作业列表的参数说明，如下所示
  | 参数     | 参数说明                 |
  | ----------------| ------------------------------------------|
  | 作业名称/ ID | 作业的名称和ID。             |
  | 状态     | 作业当前状态，包括正在运行、排队中、运行结束、失败、暂停以及未知。   |
  | 所属队列 | 作业所属的队列。         |
  | 核心数   | 运行作业的核心数。       |
  | 运行时长 | 作业运行的时长。             |
  | 总计耗时 | 总计耗时。               |
  | 用户名   | 提交该作业的用户的名称。 |
  | 创建时间 | 创建作业的时间。         |
  | 更新时间 | 作业状态更新的时间。         |
  |操作    |支持针对当前作业可进行的操作：查看详情、重新提交作业和删除|

4. 点击**所属集群**右侧的下拉框，可通过当前平台内以创建的集群类型对作业列表进行筛选。

   ![joblist_2](../../../_images/joblist_2.png)


## 查看作业详情

1. 在**作业管理**页面，勾选待查看详情的作业，点击**操作** > **查看详情**。
   ![joblist_3](../../../_images/joblist_3.png)

2. 弹出的**作业详情**页面，主要包含以下内容。
  <table>
  <tr>
    <th style="width:20%">信息类型</th> 
    <th style="width:30%">参数</th>
    <th style="width:50%">说明</th>
  </tr>
  <tr>
    <td rowspan="6">集群信息</td>
    <td>所属集群</td>
    <td>该作业所属集群的名称</td>
  </tr>
  <tr>
    <td>集群 ID</td>
    <td>该作业所属集群的 ID</td>
   </tr>
   <tr>
     <td> 集群状态</td>
     <td> 当前集群的状态，活跃为唯一正常状态。</td>
   </tr>
   <tr>
     <td> 调度器</td>
     <td> 目前采用默认调度器</td>
   </tr>
   <tr>
     <td> 共享目录</td>
     <td> 用户创建的共享目录的名称</td>
   </tr>
   <tr>
     <td> 申请/创建时间</td>
     <td> HPC / EHPC 集群创建时间</td>
   </tr>
    <tr>
    <td rowspan="4">队列信息</td>
    <td>队列名称</td>
    <td>该作业所属队列。HPC 集群中包括共享队列和专属队列， EHPC 集群只支持默认队列</td>
  </tr>
  <tr>
    <td>队列规格</td>
    <td>当前作业所属队列的规格</td>
   </tr>
   <tr>
     <td> 计费模式</td>
     <td> 包年包月或按需计费</td>
   </tr>
   <tr>
     <td> 申请时间</td>
     <td> 当前作业所属队列的申请时间</td>
   </tr>
    <tr>
    <td rowspan="6">基本信息</td>
    <td>作业名称</td>
    <td>当前作业的名称，可自定义需根据实际情况而定</td>
  </tr>
  <tr>
    <td>作业 ID</td>
    <td>当前作业的 ID，提交作业时自动生成</td>
   </tr>
   <tr>
     <td> 作业状态</td>
     <td> 当前作业的执行状态</td>
   </tr>
   <tr>
     <td> 调度器作业 ID</td>
     <td> 调度器作业 ID，系统自动生成</td>
   </tr>
   <tr>
     <td> 开始时间</td>
     <td> 该作业开始执行的时间</td>
   </tr>
   <tr>
     <td> 更新时间</td>
     <td> 该作业状态更新的时间</td>
   </tr>
      <tr>
    <td rowspan="8">运行信息</td>
    <td>作业运行时长</td>
    <td>当前作业从开始执行到运行结束所用时长</td>
  </tr>
  <tr>
    <td>平均 CPU 使用率</td>
    <td>该作业运行所消耗的集群内所有计算节点的平均 CPU 使用率</td>
   </tr>
   <tr>
     <td> 内存用量</td>
     <td> 该作业运行所消耗集群内计算节点的内存</td>
   </tr>
   <tr>
     <td> 作业是否闲置</td>
     <td> true 或 false</td>
   </tr>
   <tr>
     <td> SWAP 用量</td>
     <td> 该作业运行过程中的 SWAP 使用量</td>
   </tr>
   <tr>
     <td> 作业核心数</td>
     <td> 提交作业时已设定的该作业所需 CPU 核心数</td>
   </tr>
    <tr>
     <td> 标准输出路径</td>
     <td> 该作业运行结果所保存的路径</td>
   </tr>
    <tr>
     <td> 错误输出路径</td>
     <td> 该作业运行失败后，错误日志所保存的路径</td>
   </tr>
  <tr>
    <td rowspan="4">结果文件</td>
    <td>名称</td>
    <td>该作业运行结束后的结果文件，其中 .out 后缀文件为输出结果，.err 后缀文件为错误日志</td>
  </tr>
  <tr>
    <td>更新时间</td>
    <td>该作业结果文件的更新时间</td>
   </tr>
   <tr>
     <td> 大小</td>
     <td> 结果文件所占内存的大小</td>
   </tr>
   <tr>
     <td> 操作</td>
     <td> 用户可下载或查看任一结果文件</td>
   </tr>
  <table>

## 删除/重新提交作业

用户可以对作业进行暂停或者删除操作，如作业运行失败，也可以进行命令文件更新，重新设置一些参数，然后重新提交此作业。

### 删除作业

1. 在**作业管理**页面，勾选待删除作业，点击**操作** > **删除**。

   ![joblist_4](../../../_images/joblist_4.png)

2. 在弹出的删除相应作业的提示窗口中，点击**确定**即可。

   ![joblist_5](../../../_images/joblist_5.png)

### 重新提交作业

1. 在**作业管理**页面，勾选待重新提交的作业，点击**操作** > **重新提交作业**。

   ![joblist_6](../../../_images/joblist_6.png)

2. 弹出**提交作业**页面，根据需要相应资源、软件进行选择，并对作业执行命令进行进一步的配置修改，点击**提交作业**即可。

   ![joblist_7](../../../_images/joblist_7.png)







