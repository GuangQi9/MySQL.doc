# MySQL 关系型数据库
### MySQL特点   
   
   * MySQL是开源的，所以你不需要支付额外的费用。
   * MySQL支持大型的数据库。可以处理拥有上千万条记录的大型数据库。
   * MySQL使用标准的SQL数据语言形式。
   * MySQL可以允许于多个系统上，并且支持多种语言。这些编程语言包括C、C++、Python、Java、Perl、PHP、Eiffel、Ruby和Tcl等。
   * MySQL支持大型数据库，支持5000万条记录的数据仓库，32位系统表文件最大可支持4GB，64位系统支持最大的表文件为8TB。
   * MySQL是可以定制的，采用了GPL协议，你可以修改源码来开发自己的MySQL系统。
   


### MySQL安装

  1. 更新源
   * sudo vim /etc/apt/sources.list

       2.  将下面的源粘贴到源列表
  
  * deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
* deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
* deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
* deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
#### 测试版源
* deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
#### 源码
* deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
* deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
* deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
* deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
* deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
##### Canonical 合作伙伴和附加
* deb http://archive.canonical.com/ubuntu/ xenial partner
* deb http://extras.ubuntu.com/ubuntu/ xenial main

3. 进行更新
* sudo apt-get update 
4. 安装Apache以及MySQL
* sudo apt-get install tasksel
* sudo tasksel
5.安装workbench
* sudo apt-get install mysql-workbench

### MySQL命令
#### 连接Mysql 格式： mysql -h 主机地址 -u用户名 －p用户密码
#### 连接到本机上的MYSQL
* 如：mysql -u root -p 回车后提示你输密码.注意用户名前可以有空格也可以没有空格，
但是密码前必须没有空格，否则让你重新输入密码。如果刚安装好MYSQL，超级用户root是没有密码的，
故直接回车即可进入到MYSQL中了，MYSQL的提示符是： mysql>
#### 连接到远程主机上的MYSQL
* 假设远程主机的IP为：110.110.110.110，用户名为root,密码为abcd123。则键入以下命令： mysql -h110.110.110.110 -u root -p 123;（注:u与root之间可以不用加空格，其它也一样）
#### 退出MYSQL命令
* quit
* exit
#### 修改密码
格式：mysqladmin -u用户名 -p旧密码 password 新密码

1、给root加个密码ab12。 首先在DOS下进入目录mysql\bin，然后键入以下命令 mysqladmin -u root -password ab12 注：因为开始时root没有密码，所以-p旧密码一项就可以省略了。

2、再将root的密码改为djg345。 mysqladmin -u root -p ab12 password djg345 3、增加新用户

注意：和上面不同，下面的因为是MYSQL环境中的命令，所以后面都带一个分号作为命令结束符

格式：grant select on 数据库.* to 用户名@登录主机 identified by "密码"

1、增加一个用户test1密码为abc，让他可以在任何主机上登录，并对所有数据库有查询、插入、修改、删除的权限。首先用root用户连入MYSQL，然后键入以下命令： grant select,insert,update,delete on _._ to [email=test1@"%]test1@"%[/email]" Identified by "abc";

但增加的用户是十分危险的，你想如某个人知道test1的密码，那么他就可以在internet上的任何一台电脑上登录你的mysql数据库并对你的数据可以为所欲为了，解决办法见2。

2、增加一个用户test2密码为abc,让他只可以在localhost上登录，并可以对数据库mydb进行查询、插入、修改、删除的操作（localhost指本地主机，即MYSQL数据库所在的那台主机），这样用户即使用知道test2的密码，他也无法从internet上直接访问数据库，只能通过MYSQL主机上的web页来访问了。 grant select,insert,update,delete on mydb.* to [email=test2@localhost]test2@localhost[/email] identified by "abc";

如果你不想test2有密码，可以再打一个命令将密码消掉。 grant select,insert,update,delete on mydb.* to [email=test2@localhost]


