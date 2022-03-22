---
date: 2019-04-09T10:58:08-04:00
description: "Git 是一款流行的版本管理工具，熟练使用 Git 命令是用好 Git 的基础。本参考表提供了常用 Git 命令的速查功能，是技术开发人员必备的参考资料。"
featured_image: "images/notebook.jpg"
images: ["images/notebook.jpg"]
tags: ["git"]
categories: "Code"
title: "Git命令速查表"
---



创建命令
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git clone &lt;url&gt;</code></td><td>克隆远程仓库</td></tr><tr><td><code>git init</code></td><td>初始化本地 git 仓库（即创建新的本地仓库）</td></tr></tbody></table>

本地更改
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git status</code></td><td>查看当前分支状态</td></tr><tr><td><code>git diff</code></td><td>查看已跟踪文件的变更</td></tr><tr><td><code>git add &lt;file&gt;</code></td><td>将指定的文件添加到暂存区</td></tr><tr><td><code>git add .</code></td><td>将所有有变更的文件添加到暂存区</td></tr><tr><td><code>git commit -a</code></td><td>提交所有本地修改</td></tr><tr><td><code>git commit -m "xxx"</code></td><td>把已添加至暂存区的文件执行提交，并以 xxx 作为本次提交的描述</td></tr><tr><td><code>git commit --amend -m "xxx"</code></td><td>修改上一次提交（请勿用该命令修改已发布的提交）</td></tr><tr><td><code>git commit -am "xxx"</code></td><td>该命令是 <code>git add .</code> 和 <code>git commit -m "xxx"</code> 的快捷方式</td></tr><tr><td><code>git stash</code></td><td>暂存当前修改，将所有置为 HEAD 状态</td></tr><tr><td><code>git stash list</code></td><td>查看所有暂存列表</td></tr><tr><td><code>git stash push</code></td><td>把当前工作区的文件暂存到临时空间</td></tr><tr><td><code>git stash pop</code></td><td>把文件从临时空间中恢复到当前工作区</td></tr></tbody></table>

提交历史
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git log</code></td><td>查看提交日志</td></tr><tr><td><code>git log -n</code></td><td>显示 n 行日志，n 为整数</td></tr><tr><td><code>git log --stat</code></td><td>查看本地提交日志</td></tr><tr><td><code>git show &lt;commit&gt;</code></td><td>查看提交日志及相关变动文件</td></tr><tr><td><code>git show HEAD</code></td><td>查看 HEAD 提交日志</td></tr><tr><td><code>git show HEAD^</code></td><td>查看 HEAD 的上一个版本提交日志。另外，<code>git show HEAD^^</code> 是查看上 2 个版本的提交日志；<code>git show HEAD^5</code> 是查看上 5 个版本的提交日志</td></tr><tr><td><code>git blame &lt;file&gt;</code></td><td>对于指定文件，逐行显示提交的哈希 ID、提交者、提交日期以及修改的内容</td></tr><tr><td><code>git whatchanged</code></td><td>显示提交历史，以及每次提交变更的文件</td></tr></tbody></table>

分支和标签
-----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git branch</code></td><td>查看本地分支</td></tr><tr><td><code>git branch -r</code></td><td>查看远程分支</td></tr><tr><td><code>git branch -a</code></td><td>查看所有分支（本地和远程）</td></tr><tr><td><code>git branch --merged</code></td><td>查看所有分支已合并到当前分支的分支</td></tr><tr><td><code>git branch --no-merged</code></td><td>查看所有分支未合并到当前分支的分支</td></tr><tr><td><code>git branch -m &lt;new-branch&gt;</code></td><td>把当前分支的名称改成 <code>new-branch</code>；如果 <code>new-branch</code> 已存在，将不会执行改名</td></tr><tr><td><code>git branch -M &lt;new-branch&gt;</code></td><td>强制把当前分支的名称改成 <code>new-branch</code>（即使 <code>new-branch</code> 已存在）</td></tr><tr><td><code>git branch -m &lt;old-branch&gt; &lt;new-branch&gt;</code></td><td>把分支 <code>old-branch</code> 的名称改成 <code>new-branch</code>，如果 <code>new-branch</code> 已存在，将不会执行改名</td></tr><tr><td><code>git branch -M &lt;old-branch&gt; &lt;new-branch&gt;</code></td><td>强制把分支 <code>old-branch</code> 的名称改成 <code>new-branch</code>（即使 <code>new-branch</code> 已存在）</td></tr><tr><td><code>git checkout &lt;branch-name&gt;</code></td><td>切换到 <code>branch-name</code> 分支</td></tr><tr><td><code>git branch &lt;new-branch&gt;</code></td><td>新建分支（也可以用 <code>git checkout -b &lt;new-branch&gt;</code>）</td></tr><tr><td><code>git branch --track &lt;new&gt; &lt;remote&gt;</code></td><td>基于远程分支创建一个新分支，同 <code>git checkout --track &lt;remote/branch&gt;</code></td></tr><tr><td><code>git branch -d &lt;branch-name&gt;</code></td><td>删除本地分支</td></tr><tr><td><code>git tag</code></td><td>列出所有本地标签</td></tr><tr><td><code>git tag &lt;tag-name&gt;</code></td><td>基于最新的提交创建标签</td></tr><tr><td><code>git tag -d &lt;tag-name&gt;</code></td><td>删除标签</td></tr></tbody></table>

删除命令
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git rm &lt;file&gt;</code></td><td>删除文件（将从磁盘中删除文件）</td></tr><tr><td><code>git rm -r &lt;directory&gt;</code></td><td>递归删除指定目录下的文件</td></tr><tr><td><code>git rm --cached &lt;file&gt;</code></td><td>停止跟踪文件，不会从磁盘中删除</td></tr></tbody></table>

合并和衍合
-----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git merge &lt;branch&gt;</code></td><td>合并指定分支到当前分支，保留两个</td></tr><tr><td><code>git rebase &lt;branch&gt;</code></td><td>合并指定分支到当前分支，只保留一个</td></tr><tr><td><code>git rebase --abort</code></td><td>终止 rebase 操作，即回到执行 rebase 之前的状态</td></tr><tr><td><code>git rebase --continue</code></td><td>解决冲突后继续执行 rebase</td></tr><tr><td><code>git mergetool</code></td><td>使用配置文件指定的 mergetool 解决冲突</td></tr><tr><td><code>git add &lt;resolved-file&gt;</code><br><code>git rm &lt;resolved-file&gt;</code><br></td><td>使用编辑器手动解决文件冲突，并在冲突解决后，把文件标记为 resolved</td></tr></tbody></table>

撤销命令
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git reset --hard HEAD</code></td><td>将当前版本重置为 HEAD（用于 merge 失败的时候）</td></tr><tr><td><code>git reset &lt;commit&gt;</code></td><td>将当前版本重置为某一个提交状态，代码不变</td></tr><tr><td><code>git reset --hard &lt;commit&gt;</code></td><td>强制将当前版本重置为某一个提交状态，并丢弃那个状态之后的所有修改（请谨慎使用该命令）</td></tr><tr><td><code>git reset --merge &lt;commit&gt;</code></td><td>将当前版本重置为某一个提交状态，并保留版本库中不同的文件</td></tr><tr><td><code>git reset --keep &lt;commit&gt;</code></td><td>将当前版本重置为某一个提交状态，并保留未提交的本地修改</td></tr><tr><td><code>git revert &lt;commit&gt;</code></td><td>撤销提交</td></tr><tr><td><code>git restore &lt;file&gt;</code></td><td>丢弃指定文件的修改信息，即恢复到文件修改前的状态</td></tr><tr><td><code>git checkout -- &lt;file&gt;</code></td><td>同 <code>git restore &lt;file&gt;</code> 命令</td></tr><tr><td><code>git checkout HEAD &lt;file&gt;</code></td><td>对于指定文件，丢弃该文件的本地修改信息</td></tr><tr><td><code>git clean</code></td><td>清除工作目录中未跟踪的文件</td></tr><tr><td><code>git clean -n</code></td><td>列出哪些文件将从工作目录中删除</td></tr></tbody></table>

配置命令
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git config --list</code></td><td>列出当前 Git 配置</td></tr><tr><td><code>git config --global user.name &lt;name&gt;</code></td><td>把参数 <code>name</code> 设置为当前用户使用的提交者的姓名；如果未指定 <code>name</code> 参数，则显示当前用户使用的提交者姓名</td></tr><tr><td><code>git config --global user.email &lt;email&gt;</code></td><td>把参数 <code>email</code> 设置为当前用户使用的提交者的邮箱；如果未指定 <code>email</code> 参数，则显示当前用户使用的提交者邮箱</td></tr><tr><td><code>git config --global alias.&lt;alias&gt; &lt;command&gt;</code></td><td>为 Git 命令创建全局的别名。比如，执行 <code>alias.glog log --graph --oneline --decorate</code> 命令后，<code>git glog</code> 就相当于 <code>git log --graph --oneline --decorate</code>。</td></tr><tr><td><code>git config --system core.editor &lt;editor&gt;</code></td><td>对于本机的所有用户，设置命令使用的编辑器（比如 <code>vim</code>）</td></tr><tr><td><code>git config --global --edit</code></td><td>在编辑器中打开全局配置文件（用于手动修改）</td></tr><tr><td><code>git config --global color.ui auto</code></td><td>使用不同的颜色渲染 Git 命令的输出结果</td></tr></tbody></table>

其他命令
----

<table><thead><tr><th width="35%">Git 命令</th><th>说明</th></tr></thead><tbody><tr><td><code>git var -l</code></td><td>列出 Git 环境变量</td></tr><tr><td><code>git help &lt;command&gt;</code></td><td>显示指定命令的帮助（将呼出该命令的 man 文件）</td></tr></tbody></table>
