方法一 :  (个人首选方案) 

修改 .git/config 配置文件 [remote "origin"] 下 url 的值 ；
[remote "orgin"]
	url =  git@github.com:hhy5277/itying.git

方法二 ：

使用 Git 命令
直接修改本地仓库所关联的远程仓库的地址；

进入本地 Git 仓库根目录下；
键入： git remote 查看远程仓库名称：origin ； 
键入：git remote get-url origin 查看远程仓库地址；
键入：git remote set-url origin git@github.com:hhy5277/itying.git  ( 如果未设置ssh-key，此处仓库地址为 http://... 开头)


方法三 ：
使用 Git 命令
先删除本地仓库当前关联的无效远程地址，
再为本地仓库添加新的远程仓库地址
进入本地 Git 仓库根目录下；
键入： git remote 查看远程仓库名称：origin ； 
键入：git remote rm origin 删除本地仓库当前关联的远程仓库；
键入：git remote add origin git@github.com:hhy5277/itying.git  ( 如果未设置ssh-key，此处仓库地址为 http://... 开头)


git remote add origin git@github.com:hhy5277/itying.git

git push -u origin master

由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。