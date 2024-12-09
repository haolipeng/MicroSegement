先梳理出来一份neuvector dp的功能都有哪些。

将waf类，dlp类的功能代码都删除掉。

想清楚到底要实现什么功能？



设定目标后，将大任务拆解为小任务，然后具体的内容分配到每一天的工作中。

反思几个事，我真的看透这些开源程序了吗？对里面的原理也看懂了吗？我感觉并没有



# 一、功能需求

先弄一个demo出来。包括最精简的功能：

## 1、1 作用到主机环境

能够针对ip、port、五元组进行隔离。



## 1、2 黑/白名单功能





## 1、3 网络流量行为的拓扑梳理

梳理清楚用户的网络流量拓扑，才更方便方便用户指定精准的网络策略。

这块需要使用到图数据库，或者Neuvector自研的db数据库源代码。



## 1、4 零信任架构功能

在零信任架构中，策略决策点（PDP）和策略执行点（PEP）是达成“零信任”访问的最核心组件。

PDP策略决策点作为策略管理和动态访问控制引擎，负责策略设定和授权决策，而PEP则是具体的策略执行者，为了确保零信任体系和访问控制策略的完整性，PDP与PEP应当在互相受信的情况下开展协同。



## 1、5 支持对哪些应用层协议进行流量阻断

目前先做ipv4，tcp，udp三种，后续考虑增加更多的应用层协议。



1、6 自动打



# 二、微隔离技术架构

微隔离的架构主要分为三大组件，Agent、Server、Web

## 2、1 Agent

认证流程：

Egress捕获出站流量

Egress根据策略添加认证头

Ingress捕获入站流量

Ingress根据策略校验认证头

认证失败返回阻断数据包

认证成功建立快速流表



## 2、2 Server

把代码敲起来。每天读代码或者写代码，都算是一种进步。



2、3 前端展示



每天要抽出一定时间来加强对代码的熟悉度，不能忘本。

 Micro-isolation system based on iptables, tc and ebpf technology



# 三、技术研究

## 3、1 ebpf基础库技术选型

参考链接

https://developer.aliyun.com/article/934966



## 3、2 tc和ebpf tc的区别是什么？



## 3、3 确定eBPF map 类型和结构



## 3、4 socket filter

socket filter主要用在什么领域？有什么好处？



# 四、可参考的开源架构

## 4、1 Neuvector

主要是参考其中的dp组件和agent组件，



## 4、2 基于ebpf的零信任防火墙zfw

https://github.com/netfoundry/zfw.git