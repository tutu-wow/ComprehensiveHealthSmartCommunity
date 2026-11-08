# ComprehensiveHealthSmartCommunity
智慧社区健康管理系统 
亮点：AI智能健康问答、WebSocket在线咨询、ECharts数据可视化、健康指标监测、居民健康档案、健康评估报告、健康知识与社区活动； 
角色：居民、社区医生、管理员；

所有源码均本人开发，项目是前后端分离的，所有的项目都具备了完整的业务逻辑，不仅仅局限于基础的增删改查（CRUD）操作，系统亮点众多。

本文注重于计算机毕业设计选题指导，列出题目均有源码， 大家可以去【公众号】(毕业终点站)获取或者加我【qq】(2112698948)提意见(别忘记Star哟)。备注：git

声明：仅用于学习使用，请勿用于任何商业行为！

1.系统非商用，非开源，非无偿。

2.由本人开发，如需源码，请联系以下方式，qq:2112698948。

3.项目有很多，并未全部上传，如果未找到想要的，可直接咨询。


# 面向智慧社区的综合健康管理系统

> 居民 + 社区医生 + 管理员三角色协同的社区健康服务平台。居民查看健康档案、监测指标、问 AI、在线问诊与挂号；社区医生标注居民、出评估报告、排班接诊；管理员统筹排班、知识、活动与公告，把健康服务做到社区里。

## 一、系统亮点

- **AI 智能健康问答**：基于 LangChain4j + DeepSeek，用自然语言对话解答日常健康管理问题，SSE 流式输出，逐字显示更自然。
- **WebSocket 在线咨询**：结合医生排班提供预约挂号与在线交流，支持咨询评价，居民就近获得社区医疗服务。
- **ECharts 数据可视化**：健康、预约与社区服务概况看板，配合趋势分析与分类统计，辅助社区健康管理与服务决策。
- **健康指标监测**：记录血压、血糖、心率、体重及运动数据，用趋势图与异常标记帮居民和医生掌握健康变化。
- **居民健康档案**：统一管理基本信息、既往病史、过敏记录与用药情况，为随访与健康服务提供完整信息底表。
- **健康评估报告**：社区医生发布综合评估与健康建议，支持历史报告查看与对比，辅助持续随访。
- **健康知识与社区活动**：整合分类知识文章、个性化推荐与活动报名，让健康科普与社区服务更便捷。
- **多角色协同管理**：围绕管理员、社区医生、居民设置功能权限，配合消息通知，支持社区健康服务协同开展。

## 二、技术选型

| 层面 | 技术栈 |
| --- | --- |
| 前端 | Vue 3 + Vite + Element Plus + Vue Router + Pinia + Axios + ECharts + AIEditor + SSE 流式输出 |
| 后端 | Java + Spring Boot 3.3.1 + Spring MVC + MyBatis-Plus + MySQL + JWT |
| 实时 / 智能 | WebSocket + LangChain4j + DeepSeek + SSE 流式输出 |
| 文档 / 任务 | Apache POI（健康报告导出）+ Spring 定时任务 |
| 环境 / 工具 | JDK 17、Maven、Node.js、IDEA、Windows |

## 三、角色与功能

| 角色 | 核心职责 |
| --- | --- |
| 居民 | 健康档案、健康指标监测、AI 智能问答、在线咨询与预约挂号、健康知识与活动、消息通知 |
| 社区医生 | 居民标签标注、查看居民健康数据、发布健康评估、在线咨询、排班与预约管理、文章管理 |
| 管理员 | 医生排班、知识文章、社区活动、公告管理，统筹多角色协同 |

## 四、核心截图

### 系统总览

<p align="center"><img width="100%" src="images/overview.png"></p>

### 居民端

<table>
  <tr>
    <td width="50%"><img width="100%" src="images/res-01-home.png"></td>
    <td width="50%"><img width="100%" src="images/res-02-record.png"></td>
  </tr>
  <tr>
    <td align="center"><b>① 首页</b></td>
    <td align="center"><b>② 健康档案</b></td>
  </tr>
  <tr>
    <td width="50%"><img width="100%" src="images/res-03-data.png"></td>
    <td width="50%"><img width="100%" src="images/res-04-doctors.png"></td>
  </tr>
  <tr>
    <td align="center"><b>③ 健康数据 · 指标监测 / 趋势图</b></td>
    <td align="center"><b>④ 医生列表</b></td>
  </tr>
  <tr>
    <td width="50%"><img width="100%" src="images/res-05-chat.png"></td>
    <td width="50%"><img width="100%" src="images/res-06-appointment.png"></td>
  </tr>
  <tr>
    <td align="center"><b>⑤ 在线咨询 · WebSocket</b></td>
    <td align="center"><b>⑥ 预约挂号</b></td>
  </tr>
  <tr>
    <td width="50%"><img width="100%" src="images/res-07-knowledge.png"></td>
    <td width="50%"><img width="100%" src="images/res-08-activity.png"></td>
  </tr>
  <tr>
    <td align="center"><b>⑦ 健康知识 · 个性化推荐</b></td>
    <td align="center"><b>⑧ 健康活动 · 报名</b></td>
  </tr>
  <tr>
    <td width="50%"><img width="100%" src="images/res-09-ai.png"></td>
    <td width="50%"><img width="100%" src="images/res-10-notice.png"></td>
  </tr>
  <tr>
    <td align="center"><b>⑨ AI 智能健康问答 · 流式输出</b></td>
    <td align="center"><b>⑩ 消息通知</b></td>
  </tr>
</table>

> **健康档案 / 健康数据**对应「居民健康档案」「健康指标监测」「ECharts 数据可视化」——档案统一管信息，数据页用趋势图与异常标记看变化；**在线咨询 / 预约挂号**对应「WebSocket 在线咨询」；**AI 智能问答**对应「AI 智能健康问答」；**健康知识 / 健康活动**对应「健康知识与社区活动」；**消息通知**对应「多角色协同管理」。

### 社区医生端

**① 居民标签标注**
<img width="100%" src="images/doc-01-tags.png">

**② 健康数据 · 医生视角看板**
<img width="100%" src="images/doc-02-data.png">

> 医生侧的居民健康数据看板，对应「健康指标监测」「ECharts 数据可视化」。

**③ 健康评估 · 报告发布与对比**
<img width="100%" src="images/doc-03-assess.png">

> 发布综合评估与健康建议，支持历史报告对比，对应「健康评估报告」。

**④ 在线咨询**
<img width="100%" src="images/doc-04-chat.png">

**⑤ 预约列表**
<img width="100%" src="images/doc-05-appointments.png">

**⑥ 排班管理**
<img width="100%" src="images/doc-06-schedule.png">

> 在线咨询、预约与排班联动，对应「WebSocket 在线咨询」「多角色协同管理」。

**⑦ 文章管理**
<img width="100%" src="images/doc-07-articles.png">

> 医生维护健康知识文章，对应「健康知识与社区活动」。

### 管理员端

**① 医生排班**
<img width="100%" src="images/adm-01-schedule.png">

**② 知识文章**
<img width="100%" src="images/adm-02-articles.png">

**③ 活动列表**
<img width="100%" src="images/adm-03-activities.png">

**④ 公告管理**
<img width="100%" src="images/adm-04-notices.png">

> 管理员统筹医生排班、知识文章、社区活动与公告，把住「多角色协同管理」的全局入口。

---

> 文档展示 22 张截图，需要了解更多，请联系我。
