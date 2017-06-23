# Linux
## Linux安装
 首先找到VMware Workstation，进行安装Linux系统，在file下进行安装Linux
 
 ![](https://nts.newbieol.com/static/k6/mySQL/class-001/img/Ubuntu_17.04_English.png)

### Linux基本命令
* ls　　         显示文件或目录
* -l           列出文件详细信息l(list)
* -a          列出当前目录下所有文件及目录，包括隐藏的a(all)
* mkdir         创建目录
* -p           创建目录，若无父目录，则创建p(parent)
* cd               切换目录
* touch          创建空文件
* echo            创建带有内容的文件。
* cat              查看文件内容
* cp                拷贝
* mv               移动或重命名
* rm               删除文件 * -r            递归删除，可删除子目录及文件
* -f            强制删除
* find              在文件系统中搜索某文件
* wc                统计文本中行数、字数、字符数
* grep             在文本文件中查找某个字符串
* rmdir           删除空目录
* tree             树形结构显示目录，需要安装tree包
* pwd              显示当前目录
* ln                  创建链接文件
* more、less  分页显示文本文件内容
* head、tail    显示文件头、尾内容
* ctrl+alt+F1  命令行全屏模式
### 基本文件操作
* 文件的创建、删除、复制、重命名、移动
* touch  file 
* rm –rf file
* cp file file1
* cp file  /home/linux/file1
* mv file   file2
* mv file  /home/linux/
* 列出文件列表
* ls -al
* 查看文件内容
* Cat file 
### 基本目录操作
* 目录的创建、删除、复制、重命名、移动
* mkdir dir
* rm –rf dir
* cp dir   dir1  -a
* cp dir   /home/linux/dir2  -a
* mv dir  dir2
* mv dir  /home/linux/
* 列出目录列表
* ls -d  dir
* 目录中查找文件
* find  ./dir  -name  "filename"

### vim的基本使用
* i：在当前字符的左边插入
* I：在当前行首插入
* a：在当前字符的右边插入
* A：在当前行尾插入
* o：在当前行下面插入一个新行
* O：在当前行上面插入一个新
* h: 向前移动一个字符
* j: 向上移动一行
* k: 向下移动一行
* l: 向后移动一个字符
* yy: 复制当前一行
* dd:剪切当前一行
* p: 粘贴内容到游标之后
* P: 粘贴内容到游标之前
