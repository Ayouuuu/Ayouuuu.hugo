---
title: "记一次Linux Git Push 缺少公钥权限的问题"
date: 2023-03-27T14:50:43Z
keywords: ["Git","Linux"]

tags:
- Linux
- Git
categories:
- 其他
---

## 问题
已配置 `Github` 公钥，但是依然无法拉取私人项目或更新子项目，使用 `ssh -T git@github.com` 命令返回正常。

## 来源
这种情况一般是文件夹所有权的问题，当你使用`sudo git clone` 命令克隆项目，使用的是 `root` 账户，所以创建的文件夹所有者也是管理员账户,所以我们直接操作是没有任何权限的。  
同时在拥有私人子模块（submodules）时，使用`sudo git submodule update`克隆子项目，会出现缺少公钥权限,这种情况是由于`/root/.ssh/`文件夹当中缺少私钥。

## 解决办法
其一就是把当前用户的`~/.ssh/`文件夹复制粘贴到`/root/.ssh/`当中即可解决问题。  
其二使用`sudo chown <用户>:<用户> -R 文件夹` 修改文件夹所有人。  
其三则是尽量不要使用`sudo`执行`git`命令。 参考 [是否应将 sudo 命令或提升的权限与 Git 一起使用？](https://docs.github.com/zh/authentication/troubleshooting-ssh/error-permission-denied-publickey#should-the-sudo-command-or-elevated-privileges-be-used-with-git)
