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
   
       1.  将下面的源粘贴到源列表
  
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

   

