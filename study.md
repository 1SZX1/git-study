## 基本
+ 当列表过长时，第一行会变成:,输入q可以退出。
## 常用本地操作
+ git init : 初始化
+ git add &lt;文件名&gt; : 添加指定文件到暂存区
    - git add . : 添加所有文件到暂存区
+ git commit -m &lt;message&gt; : 添加到本地仓库
+ git diff : 查看修改内容
+ git log : 查看详细提交历史
    - git log --pretty=oneline 查看简化提交历史
+ git reflog : 查看命令历史
+ git stash : 把当前工作现场“储藏”起来，等以后恢复现场后继续工作
    - git stash list : 查看储藏(以下操作可以在后面添加指定储藏头)
    - git stash pop : 恢复并删除储藏
    - git stash apply : 恢复储藏，但是恢复后，stash内容并不删除
    - git stash drop : 删除储藏
+ git cherry-pick commit_id : 复制一个特定的提交到当前分支
## 撤销操作
+ git reset : 回退版本
    - git reset --hard HEAD^ : 回退到上一个版本
    - git reset --hard commit_id : 回退到指定commit_id版本
+ git checkout -- 文件名 / git restore &lt;文件名&gt; : 丢弃文件工作区的改动，回到最近一次git commit或git add时的状态。
+ git reset HEAD &lt;文件名&gt; : 把暂存区的修改撤销掉，重新放回工作区
## 分支操作
+ git checkout -b dev / git switch -c dev: 创建并切换到dev分支
    - git branch dev : 创建dev分支
    - git checkout dev / git switch dev: 切换到dev分支
+ git merge dev: 合并dev分支到当前分支(fast forward合并)
+ git merge --no-ff -m "提交信息" dev : 合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并。
+ git branch -d dev : 删除dev分支
+ git log --graph : 查看分支合并图
+ git branch -D &lt;分支名&gt; : 强行删除没有被合并的分支
## 常用远程操作
+ ssh-keygen -t rsa -C "我的邮箱地址" : 创建SSH Key
+ git remote add origin 远程仓库地址 : 关联远程仓库
+ git clone : 从远程仓库克隆
工作现场sdfd