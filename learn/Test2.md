# 第二阶段

## 一、Git基本操作

版本控制系统：控制一份文件不同版本的系统

集中式版本控制系统：版本库是集中存放在中央服务器的，而干活的时候，用的都是自己的电脑，所以要先从中央服务器取得最新的版本，然后开始干活，干完活了，再把自己的活推送给中央服务器。（缺点：必须要联网才能工作）

分布式版本控制系统：每个人的电脑上都一份版本库，个人各个修改只需要互相推送修改来完善文件

我的Git版本库

![image-20201029163823494](C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201029163823494.png)

版本控制系统是无法跟踪word文件的改动的！！（因为word是二进制的储存方式，版本控制系统只能知道他改变了01，无法知道内容改变了什么），所以我们就要以纯文本方式编写文件

此外我们不使用win自带的记事本（编码会出错），我们使用Notepad++软件来编写一个txt文件

### Git命令：

* git init：初始化本地仓库

* git add：添加一个文件到缓存区（物理）（打怪前的备份）

* git commit -m "本次文件修改说明" ：添加文件到仓库（一次可以提交多份文件）（备份时的装备状态说明）

* git status 反馈工作区的当前状态:（可以看到有没有未提交的文件）（查看这个存档的装备）

* git diff :（diff means differences）查看修改的不同之处 （查看装备状态的改变）

* git log : 查看历代的版本修改（--pretty=oneline：添加后简化版本说明，前面的数字为版本号）

* git reset : 版本回退，第一个版本为HEAD^，第二个为HEAD^^或者HEAD~2，或者直接写版本号commit_id（通常添加参数--hard）

* git reflog：关机后的后悔药，记录了每一次命令

* git checkout -- <file>：可以撤销工作区的修改，让该文件回到最近一次commit或add的状态

* git reset HEAD <file>：可以撤销暂存区的修改，重新放回工作区

* git rm：从版本库中删除文件（记得commit一下）

* cd .. ：退回上一个文件夹

  ***

* git push origin master：将本地master分支的最新修改推送到Github

* git remote add origin git@server-name:path/repo-name.git：关联本地与github的账号的仓库

* git clone git@github.com:13007491638/<file>.git：把Github远程库中的库同步clone到本地来


### Git基本概念：

<img src="C:\Users\29297\AppData\Roaming\Typora\typora-user-images\image-20201029193650076.png" alt="image-20201029193650076" style="zoom: 67%;" />

版本库是工作区中的一个隐藏区域（.git），但不算工作区

Git跟踪的其实是修改（修改的这个动作），而非文件本身（动作结果）

所以在git中的每一次提交都被穿成了一条时间线（所有的修改都在这条线上面），而我们的master（仓库）都只是指向那个最新的提交（应证了上面的GIt跟踪的其实是修改记录而不是文件本身）；除此以外HEAD指向master，master再指向提交，所以HEAD指向的就是当前时间线的末端（当前分支）



## 二、Git远程仓库

### 惊！GitHub就是那种24/7的远程仓库！

User里面的.ssh文件夹就是用来存储SSH加密的通讯所使用的密匙（Git和Github之间的通讯通过ssh加密）

### 分支管理

相当于一个远程库上只有自己能看到的小空间，所有撸到一半又没法用又怕进度丢失的代码就放这里面，别人又看不到，等到代码完善后再合并到原分支上去。