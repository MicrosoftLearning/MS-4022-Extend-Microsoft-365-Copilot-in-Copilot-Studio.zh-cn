---
title: 练习说明
permalink: index.html
layout: home
---

# 练习

此页面列出了与 Microsoft 技能课程 **MS-4022：在 Copilot Studio 中扩展 Microsoft 365 Copilot** 相关的练习。

相关学习路径：[在 Copilot Studio 中扩展 Microsoft 365 Copilot](https://learn.microsoft.com/training/paths/extend-microsoft-365-copilot-studio/)。

**备注**：要完成这些练习，你将需要：

- 具有 [Copilot Studio 访问权限](https://learn.microsoft.com/microsoft-copilot-studio/requirements-licensing-subscriptions)的工作或学校帐户。 如果还没有访问 Copilot Studio 的权限，则根据 Microsoft 365 组织的配置，可以[创建试用帐户](https://learn.microsoft.com/microsoft-copilot-studio/sign-up-individual)。
- Microsoft 365 Copilot 许可证
- 用于连接到所需内容源的凭据（连接器、API 等）

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %} {% assign labs = labs | sort: "lab.title" %} {% for activity in labs  %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}

