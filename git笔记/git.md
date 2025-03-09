# 一、Git常用命令

| 命令                                                         | 作用                                                         |
| :----------------------------------------------------------- | ------------------------------------------------------------ |
| git config --global user.name 用户名                         | 设置用户签名                                                 |
| git cinfig --global user.email 邮箱                          | 设置用户签名                                                 |
| git init                                                     | 初始化本地库                                                 |
| git status                                                   | 查看本地库状态                                               |
| git add .（若写文件名，则表示只添加该文件）                  | 添加到暂存区                                                 |
| git commit -m "日志信息" 文件名（若不写文件名，则表示添加所有） | 提交到本地库                                                 |
| git reflog或者git log(详细信息)                              | 查看历史记录                                                 |
| git reset --hard 版本号                                      | 版本穿梭                                                     |
| git branch 分支名                                            | 创建分支                                                     |
| git branch 或 git branch -v                                  | 查看分支                                                     |
| git checkout 分支名/git checkout -b 分支名                   | 切换分支/创建并切换分支                                      |
| git merge 分支名                                             | 把指定分支合并到当前分支上                                   |
| **（重要）git remote add 别名 【远程仓库https地址】**        | **给远程仓库起别名**                                         |
| **（重要）git push 【远程仓库名】【分支名】，若没有给远程仓库起别名，这里直接用远程仓库https地址也是可以的** | **将本地分支推送到远程仓库中**                               |
| **（重要）git push -u 【远程仓库名】【分支名】，若没有给远程仓库起别名，这里直接用远程仓库https地址也是可以的。（命令中的-u也可以写成--set-upstream）** | **将本地分支和远程分支关联起来，之后可以直接git push推送或git pull拉取** |
| git pull 【远程仓库名】【分支名】                            | 拉取代码                                                     |
| git clone 远程地址                                           | 克隆远程仓库                                                 |
| git remote 或 git remote -v                                  | 查看别名列表                                                 |

# 二、使用Git常见问题

## 1、解决拉下来的项目在本地只有主分支master

以dev分支为例，运行命令 git checkout -b dev origin/dev，即可拉下并切换至dev分支

## 2、新建分支，并推送远程

1、新建分支 git checkout -b new_branch

2、推送远程 git push origin new_branch

3、开发完成后 git push 时报错，未与远程分支相关联，运行  git push --set-upstream origin feature/file关联即可

## 3、从暂存区中删除某个文件

![image-20250225134105448](C:\Users\21928\AppData\Roaming\Typora\typora-user-images\image-20250225134105448.png)