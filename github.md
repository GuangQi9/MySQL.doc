
## Github的使用
### github的简介
* GitHub是一个通过Git进行版本控制的软件源代码托管服务，由GitHub公司（曾称Logical Awesome）的开发者Chris Wanstrath、PJ Hyett和Tom Preston-Werner使用Ruby on Rails编写而成。
### 创建github仓库
 
* Repository name: 要创建git仓库的名子
* Description: 这个仓库的简单描述, 让别人很快的了解这个库是做什么用的.
* Public: 表示这个仓库是公开的, 任何人都可看到, 可以随意下载, 这就是传说中的开源.
* Private: 私有库, 只能指定相关的人员才能看到并能下载. 这一般是公司或组织使用的私有项目, 这需要每个月向github交$7.
* Initialze this Repository with a README: 初始生成README文件, .gitignore和license文件.
### github的简单使用
创建github仓库后, 我有3种方法可以下载使用它.
1. 如果我们本地没有git仓库, 可以先在本地创建一个git仓库, 并做一个提交. 然后再互github远程仓库进行关联.
* echo "# abc" >> README.md
* git init
* git add README.md
* git commit -m "first commit"
* git remote add origin https://github.com/wangleihd/freeBook-H5.git
2. 我们本地已经有git仓库了, 那我们现在就直接与github仓库进行关联就可以了
* git remote add origin https://github.com/wangleihd/freeBook-H5.git
* git push -u origin master
3. 我们还可以用clone直接去下载这个项目, 这也是最常用下载或拉取github仓库的方法
* git clone https://github.com/wangleihd/freeBook-H5.git
 
### Github的简单开发使用
Github的流程。也就是：
* 开发者各自fork项目的repo到自己Github账户下
* 每次开发同步到项目的repo然后再进行开发
* push自己的开发分支到自己Github账户下面的fork的项目repo
* 发送pull request给项目管理员
* 等待review或者merge

1. 分支规划
采用git remote add命令给自己本地的开发repo添加分支，我们用一下约定来处理分支的名字
* origin - 指向自己fork出来的repo例如我的叫GuangQi9
* dev_name - 直接指向项目的repo

2. 本地开发配置

* 从wenda的项目repo clone最新的代码
* git clone --recursive https://github.com/GuangQi9/wenda.git

* 添加自己fork的repo用来发布代码和发送pull request
* cd wenda
* git remote add youname https://github.com/youname/wenda.git
* git fetch youname
* git fetch origin
* git checkout -b develop origin/develop (create a new branch for development)
* git reset --hard origin/develop (reset the local branch to latest origin development branch)
4. 开发流程
   
* git fetch origin
* git rebase origin/develop (rebase local change onto origin development branch)
* do some work ...
* git commit changes
* git push --force youname develop
