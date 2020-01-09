## 基本
+ 当列表过长时，第一行会变成:,输入q可以退出。
## 基本
+ git init : 初始化
+ git add &lt;file&gt; : 添加指定文件到暂存区
    - git add . : 添加所有文件到暂存区
+ git commit -m &lt;message&gt; : 添加到本地仓库
+ git diff : 查看修改内容
+ git log : 查看详细提交历史
    - git log --pretty=oneline 查看简化提交历史
+ git reflog : 查看命令历史
+ git reset : 回退版本
    - git reset --hard HEAD^ : 回退到上一个版本
    - git reset --hard commit_id : 回退到指定commit_id版本
+ git restore -- file : 丢弃文件工作区的改动，回到最近一次git commit或git add时的状态。
+ git reset HEAD &lt;file&gt; : 把暂存区的修改撤销掉，重新放回工作区