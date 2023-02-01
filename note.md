# git 学习笔记
    git init 把当前目录变成git可以管理的仓库  
    git status 查看仓库当前状态  
    git add 《file》 添加修改  
    git commit -m "write something" 提交修改并注释
    git commit --amend 修改最近一次的提交
    git diff 《file》 查看文件差异  

    git branch 查看当前分支  
    git branch -r 查看远程分支  
    git branch -a 列出所有本地分支和远程分支   
    git branch -d [branch-name] 删除本地分支  
    git branch -D [branch-name] 强行删除本地分支  
    git branch --set-upstream [本地分支名] origin/[远程分支名] 指定[本地分支]分支追踪origin/[远程分支名]。  

    git remote 所有远程主机名  
    git remote -v 所有远程主机名和网址    
    git remote show origin 查看远程 (可以看到本地和远程对应关系) <origin为远程主机名>  
    git remote prune origin 删除本地库中这些相比较远程库中已经不存在的分支 <origin为远程主机名>  
    git remote add origin [远程仓库地址] 本地与远程仓库关联(添加远程仓库)
    git remote set-url origin <URL> 更换远程仓库地址
    git remote set-url --add origin <url2> 为远程仓库添加其他地址
    

    git pull <远程主机名> <远程分支名>:<本地分支名> 取回远程主机某个分支的更新，再与本地的指定分支合并。  
    git push <远程主机名> <本地分支名>:<远程分支名> 将本地分支的更新，推送到远程主机。 !!注意两者差异!!  

    git push -u origin master 把当前master分支推送到远程master分支。-u 参数 可以使本地与远程master分支关联  
    git push origin :<远程分支名> 删除远程分支  
    git push origin --delete [branch-name] 删除远程分支  

    git reset --hard [表示版本的数字串]  版本切换  
    git reset --hard HEAD 切换到当前版本 (HEAD^ 上一个版本，HEAD^^ 上上个版本，HEAD~5 往上5个版本)  
    git reset HEAD [文件名] 撤销文件暂存区的修改，重新放回工作区。
    git checkout -- [文件名] 丢弃文件当前工作区的修改，让文件恢复到上一个git add或git commit的状态  
    git checkout -b [本地分支名] 创建并切换到本地分支  
    git checkout -b [本地分支名] origin/[远程分支名] 创建和切换到本地分支并与远程分支建立关联  

    git checkout master 切换到master分支  
    git merge dev 把dev分支合并到当前分支  
    git merge --no-ff -m "merge with no-ff" dev 把dev分支合并到当前分支并留下历史记录  

    git rm [文件名] 删除文件  

    git stash 把当前的工作状态暂存起来
    git stash save [描述] 把当前的工作状态暂存起来
    git stash list 查看暂存的工作状态  
    git stash apply 恢复暂存的内容，但是恢复后，stash内容并不删除  
    git stash drop 删除暂存  
    git stash pop 恢复的同时把stash内容也删除  
    git stash apply stash@{0} 恢复指定的暂存内容
    git stash show -p stash@{1} 是查看第二最近stash的变化

    git tag 查看所有标签  
    git tag [标签名] 为当前分支创建标签  
    git show [标签名] 显示标签具体信息  
    git tag [标签名] [commit ID] 为某一次提交创建标签  
    git tag -a [标签名] -m "描述信息" [commit ID] 为某一次提交创建有说明的标签
    git tag -d [tagName] 删除本地标签
    

    git config 用于git相关设置  
    git config --list git设置显示 --local 显示本地   
    git config --global user.name "John Doe"  
    git config --global user.email "johndoe@example.com"  
    git config --global alias.st status 为status设置别名 git st 就表示 git status  
    git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"  设置别名 git lg 就表示 git [后面那一窜]  

    git config --global core.quotepath false 设为false的话，就不会对0×80以上的字符进行quote。中文显示正常  
    git config --global gui.encoding utf-8 设置 commit log 提交时使用 utf-8 编码，可避免服务器上乱码，同时与linux上的提交保持一致！  
    类似见 [git乱码解决方案](http://www.cnblogs.com/perseus/archive/2012/11/21/2781074.html)  

    git log 查看记录
    git reflog 查看操作记录  
    git log --pretty=oneline 查看记录（每个一行显示）
    git log -- [file] 查看文件的提交记录

    git log dev ^master 查看dev中有，而master中没有的内容  
    git log master ^dev 查看master中有，而dev中没有的内容   
    git log master..dev 查看 dev 中比 master 中多提交了哪些内容
    git log dev...master 查看其中一个比另一个多提交什么  
    
    git log -- filename  查看该文件的提交记录  
    git log filename 查看该文件的提交记录  
    git log -p filename 可以显示该文件每次提交的diff  
    git show [commit-id] filename 查看某次提交中的某个文件变化  
    


## 命令行释意
  
    cd 进入目录  
    mkdir 创建目录  
    touch 创建或打开文件
    pwd 显示当前目录  
    ls -ah 查看当前目录内容  
    vim ( ":"状态下 ) 
        进入编辑状态 i 退出编辑状态 ESC
        退出 q
        保存退出 wq
        不保存退出 q!
        强制退出 !  


    /usr/libexec/java_home -V 查看jdk版本信息 （ Mac已安装 和 Mac默认使用 ） 
    npm list -g --depth 0 查看已经全局安装的npm包。  



    

