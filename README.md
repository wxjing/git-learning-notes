[toc]
# 设置个人信息
> git config --global user.name yourname #你是谁
> git config --global user.email youremail #怎么联系你

# 基础命令
> git init #初始化git目录
> git status #查看仓库状态

# 添加文件|修改文件
> git add index.php #把index.php提交到暂存区
> git add . #把当前目录所有文件提交到暂存区

# 移动|修改
> git mv 源文件 新文件
移动:git mv config.php ./inc/config.php
改名:git mv config.php config.inc.php
# 删除文件
> git rm index.php #把index.php删除

# 提交文件至版本库
> git commit -m "注释内容"

# 添加一个远程仓库
> git remote add origin https://git.oschina.net/lianshou/test.git
[意思是:添加1个远程库,代号是origin,地址是https://......test.git]

# 把代码提交到远程仓库
> git push origin master

# 把远程仓库代码拉取到本地
> git pull origin master

# 查看日志
> git log 查看项目的日志
git log filename 查看某文件的日志
git log . 查看本目录的日志
git log --pretty=oneline 让日志单行显示

# 查看操作记录
> git reflog

# 版本切换
> git reset --hard HEAD^^^ 向前切3个版本
> git reset --hard 版本号

# 查看分支
> git branch

# 创建分支
> git branch branchname

# 切换分支
> git checkout branchname

# 快速创建和切换分支
> git checkout -b branchname

# 分支合并
> git merge branchname

# 删除分支
> git branch -d branchname



# remote
> git remote add origin url #添加一个远程仓库
> git remote #列出已经存在的远程分支
> git remote -v #列出详细信息，在每一个名字后面列出其远程url
> git remote remove remotename #删除添加的远程仓库
> git remote rename <旧名字> <新名字>


# 公钥登录
1. 配置ssh格式的远程仓库地址
git remote add 远程仓库名 远程仓库地址
例:
git remote add gitaddr git@git.oschina.net:lianshou/test.git
2. 创建ssh key
ssh-keygen -t rsa -C "youremail@example.com",把邮件地址换成你自己的邮件地址,一直回车,不用输入密码.完成后,可以在用户主目录里找 到.ssh目录,内有id_rsa和id_rsa.pub两个文件. id_rsa是私钥,id_rsa.pub是公钥. 这两把钥匙是成对的,可以让分别持有私钥和公钥的双方相互认识.
3. 把公钥放在服务器 用记事本打开id_rsa.pub,复制公钥内容. 登陆git.oschina.net,如下图,填入公钥并保存.

# git服务器搭建
[菜鸟教程](http://www.runoob.com/git/git-server.html)
