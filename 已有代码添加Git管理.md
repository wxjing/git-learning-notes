# 一、 基本的本地准备
1. 初始化本地仓库
`git init`

2. 将代码添加仓库
`git add .`

3. 将代码提交到本地仓库
`git commit -m "Initial commit"`

# 二、远程仓库连接
1. 添加远程仓库
`git remote add origin http://your_remote_git_server/sample.git`

2. 同步远端仓库到本地
`git pull --rebase origin master`

> --rebase 非常重要，否则pull失败

3. 推送代码到远端仓库
`git push origin master`
