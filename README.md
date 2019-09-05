[toc]


# 设置个人信息
- git config --global user.name wxjing #你是谁
- git config --global user.email youremail #怎么联系你

# 基础命令
git init 初始化git目录
git status 查看状态
git rm 删除
git add 添加
git commit -m '注释' 提交到版本库
git pull 远程仓库拉取到本地
git push 代码提交到远程仓库

git checkout -- 恢复修改的文件
git reset HEAD  恢复删除的文件
流式协议，没有消息边界。<br/><span style="color:red;">客户端向服务器</span>发送1次数据，可能会被服务器分成多次收到。<br>客户端向服务器发送
git branch 查看分支
git branch branch-name 创建分支
git checkout branch-name 切换分支
git checkout -b branch-name 创建新分支并切换分支
git branch -d branch-name 删除分支

git merge branch-name 合并分支

# 查看日志
- git log 查看项目的日志
- git log filename 查看某文件的日志
- git log . 查看本目录的日志
- git log --pretty=oneline 让日志单行显示

# 查看操作记录
- git reflog

# 版本切换
- git reset --hard HEAD^^^ 向前切3个版本
- git reset --hard 版本号

# remote
- git remote 列出已经存在的远程分支
- git remote -v 列出详细信息，在每一个名字后面列出其远程url
- git remote add origin url 添加一个远程仓库
- git remote remove remotename 删除添加的远程仓库
- git remote rename <旧名字> <新名字>
