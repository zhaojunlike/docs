---
title: 账户管理
---

### 什么是账户?

有权访问Rancher的每个用户都有Rancher帐号。对于本地身份认证设置，你可以为用户创建帐户，对于其他身份认证方式，当用户登录到Rancher时，会为该用户自动创建一个帐户。

#### AD域/GitHub/OpenLDAP验证

当[AD域](/docs/rancher/v1.x/cn/configuration/access-control/#活动目录)，[Azure AD](/docs/rancher/v1.x/cn/configuration/access-control/#azure-ad)，[GitHub](/docs/rancher/v1.x/cn/configuration/access-control/#github)，或者[OpenLDAP](/docs/rancher/v1.x/cn/configuration/access-control/#openldap)验证开启的时候，**帐户**选项卡显示已登录并针对Rancher进行身份认证的用户列表。为了登录，它们必须被赋予[访问站点](/docs/rancher/v1.x/cn/configuration/access-control/#站点访问)的权限或被添加到[环境](/docs/rancher/v1.x/cn/infrastructure/environments/)中。

#### 本地验证

[启用本地身份认证](/docs/rancher/v1.x/cn/configuration/access-control/#本地身份认证)后，你可以在**账号设置**中添加用户。点击**添加帐号**按钮将帐号添加到Rancher数据库。创建帐号时，帐号类型可以指定为管理员或用户。

### 账户类型

Rancher通过帐户类型确定用户是否可以访问系统管理页面。对于Rancher中的每个环境，都可以通过设置账号的[成员角色](/docs/rancher/v1.x/cn/infrastructure/environments/#成员角色)来为环境实现不同级别的访问控制。

#### 管理员

认证Rancher的第一个用户成为Rancher的管理员。 只有管理员才有权限查看**系统管理**页面

在管理环境时，管理员可以查看Rancher中的所有[环境](/docs/rancher/v1.x/cn/infrastructure/environments/)， 即使管理员没有被加入到该环境的成员中。 在非管理员的环境下拉菜单中，用户只能看到他们所在的环境。

管理员可以将其他用户添加为Rancher管理员。 在用户登录Rancher后，他们可以在 **系统管理** > **账号设置**页面上更改用户角色。 在**系统管理**> **账号设置帐户**标签中，点击帐户名称旁边的**编辑**，并将帐户类型更改为管理员。 点击**保存**。

#### 用户

除了用来启用Rancher认证的用户外，任何其他用户都将自动拥有用户权限。 他们将无法看到**系统管理**页面

他们只能看到他们所在的环境。
