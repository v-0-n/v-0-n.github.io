# Linux笔记


## 基础

### **获取帮助方式**

> 1. 命令 --help
> 2. 系统去红帽官网
> 3. 软件去软件官网
> 4. 百度&谷歌

### **Linux目录结构**

| 常用目录         | 意义或作用                                                   |
| ---------------- | ------------------------------------------------------------ |
| `etc/passwd`     | 用户信息配置文件                                             |
| `usr/bin/passwd` | 修改用户口令的命令                                           |
| `/root`          | 超级用户的家目录                                             |
| `/home`          | 普通用户家base目录                                           |
| `/dev/zero`      | 零设备                                                       |
| `/dev/null`      | 空设备，类似回收站                                           |
| `/dev/random`    | 产生随机数                                                   |
| `/boot`          | 存放和系统启动相关的文件                                     |
| `/proc`          | **虚拟文件系统**。反映出来的是内核、进程信息和实时信心（车的仪表盘） |
| `/usr`           | 存放系统文件，相当于`C:\window`                              |
| `/bin`           | 普通用户命令、应用程序存放目录                               |
| `/sbin`          | 管理员命令、应用程序存放目录                                 |
| `/etc`           | 系统相关配置文件、应用相关配置文件                           |
| `/tmp`           | 临时文件。进程产生的临时文件，全局可写入                     |
| `/var`           | 存放变化的文件。如日志、邮件、数据库                         |
| `/mnt`           | 设备挂载点                                                   |

| `usr`下的子目录 | 意义或作用                    |
| --------------- | ----------------------------- |
| `/local`        | 软件安装目录，相当于C:Program |
| `/bin`          | 普通用户使用的应用程序、命令  |
| `/sbin`         | 管理员使用的应用程序、命令    |
| `/lib`          | 库文件Glibc                   |
| `/lib64`        | 库文件Glibc-64位              |

> **绝对路径和相对路径**
>
> 例：如果当前目录是`/root`，`/a/1.txt`和`a/1.txt`，前者的目录是`/a/1.txt`，后者的目录是`/root/a/1.txt`。在路径中，`~`代表家目录。

### **常用指令**

| 常用指令      | 含义                                             |
| ------------- | ------------------------------------------------ |
| `rm`          | 通配符`*`无法删除隐藏文件                        |
| `man`         | manual：针对命令、配置文件帮助。`-f`：查章节     |
| `tree`        | 查看指定文件夹内文件（夹）结构                   |
| `mkdir`       | 创建文件夹                                       |
| `cp`          | 复制文件（夹）                                   |
| `ls`          |                                                  |
| `unzip`       | 解压                                             |
| `tar`         | 解压缩                                           |
| `top`         | 查看系统实时运行状态                             |
| `screen`      |                                                  |
| `yum`         |                                                  |
| `wget`        | 下载                                             |
| `curl`        | 下载                                             |
| `cat`         | `-n`：显示行号 -A：包括显示控制字符。            |
| `touch`       | 创建文件                                         |
| `pwd`         |                                                  |
| `mv`          | 移动文件（夹）。利用`mv`改名                     |
| `less`        | 查看大文件                                       |
| `geit`        | 需要图形化支持，如无必要不要使用。               |
| `dos2unix`    | 转换在windows修改过的文件                        |
| `head`        | 查看文件一部分（前面部分）                       |
| `tail`        | 查看文件一部分（后面部分）。**常用`tail -f`**    |
| `grep`        | 搜索                                             |
| `less`        | 查看大文件                                       |
| `vimdiff`     | 比较两个文件的不同                               |
| `file`        | 看文件类型                                       |
| `stat`        |                                                  |
| `su username` | 切换用户                                         |
| `id username` | 查看username用户信息:uid、gid（主）、gid（所有） |
| `wc`          | 统计文件行、单词数、字符数                       |
| `tty`         | 显示当前终端数                                   |
| `EOF`         | 重定向                                           |
| `ll`          | 常用来查看文件权限（旧的ugo权限）                |
| lsattr        | 列出文件属性                                     |
| chattr        | 改变文件属性                                     |
| umask         | 进程掩码：减权限                                 |

### Vim常用快捷键

| 光标定位 |                                                       |
| -------- | ----------------------------------------------------- |
| k        | 上                                                    |
| j        | 下                                                    |
| h        | 左                                                    |
| l        | 右                                                    |
| 0        | 光标移至本行行首                                      |
| $        | 光标移至本行行尾                                      |
| gg       | 光标移至第一行行首                                    |
| G        | 光标移至最后一行行首                                  |
| NG       | 光标移至第N行行首。                                   |
| /string  | `/`代表搜索模式，搜索`string`。其中string可以使用正则 |

| 文本编辑          |                                                  |
| ----------------- | ------------------------------------------------ |
| `yy`              | 复制本行，可视（块、行），只需单按`y`键          |
| `Nyy`             | 从光标所在行开始（包括所在行），复制N行。        |
| `ygg`             | 从第一行复制到光标所在行（包括所在行）           |
| `yG`              | 从光标所在行开始（包括所在行），复制到最后一行。 |
| `dd`              | 删除（严格说是剪切）                             |
| `Ndd`             | 类似于上面的`Ngg`                                |
| `dgg`             | 类似于上面的`ygg`                                |
| `dG`              | 类似于上面的`yG`                                 |
| `D`               | 从光标所在处开始删至本行行尾                     |
| `x`               | 删除本行                                         |
| `u`               | 撤销上一步操作                                   |
| `Ctrl`+`r`        | 恢复上一步操作                                   |
| `p`               | 粘贴                                             |
| `R`               | 批量替换          `r`：单字符替换                |
| `ctrl+p`&`ctrl+n` | 进行编辑时可自动补全                             |

> 命令模式只能替换

| 可视模式   |                                       |
| ---------- | ------------------------------------- |
| `v`        | 进入可视模式                          |
| `Ctrl`+`v` | 进入可视块模式                        |
| `V`        | 进入可视行模式                        |
| `I`        | ^v进入可视块，按大写`I`进入进入块插入 |

|     命令扩展模式      |                                                              |
| :-------------------: | ------------------------------------------------------------ |
|          `:`          | 进入扩展命令模式                                             |
|         `:N`          | 进入第N行行首                                                |
|         `:w`          | 保存                                                         |
|         `:q`          | 退出                                                         |
|         `:wq`         | 保存并退出                                                   |
|         `:q!`         | 不保存并退出                                                 |
|         `:w!`         | 强制保存                                                     |
|        `:wq!`         | 强制保存并退出                                               |
| `:m,n s/old/new/选项` | n不写或者m不写，代表从当前行开始或者到当前行结束。类似于sed，可用正则匹配 |
|  `:m,n w /path/file`  | 将m到n行保存到path目录下的file文件中（file文件是新建的，m、n可省略） |
|   `:n r /path/file`   | 将path目录下file文件的内容读入当前文件第n行后                |

| 临时设置环境 |              |
| ------------ | ------------ |
| `:set nu`    | 显示行号     |
| `:set ic`    | 不区分大小写 |
| `:set ai`    | 自动缩进     |
| `:set list`  | 显示控制字符 |

| 永久设置配置路径 |                       |
| ---------------- | --------------------- |
| `/etc/vimrc`     | 修改所有用户vim配置   |
| `~/.vimrc`       | 影响当前用户的vim配置 |

### 文件相关

#### Linux文件时间

> 1. access time：访问时间
> 2. modify time：修改时间
> 3. change time：改变时间
> 4. delete time：删除时间

#### Linux文件类型

`ls - l 文件名`判断：

1. 以`-`开头：普通文件
2. 以`d`开头：目录文件（蓝色）
3. 以`b`开头：设备文件（存储设备硬盘）
4. 以`c`开头：设备文件（打印机、终端等）
5. 以`s`开头：套接字文件
6. 以`p`开头：管道文件
7. 以`l`开头：链接文件（淡蓝色）

> `type`:查看命令类型或属性
>
> `stat`:查看问文件属性（名称、大小、时间、权限）
>
> `file`:查看文件类型

### 用户&组

#### 用户&组的相关配置文件

`/etc/passwd`：用户信息文件

`/etc/shadow`：密码信息文件

`/etc/group`：组信息文件

> 1. /etc/passwd文件内容格式：
>
> ​          `用户名:x:uid:gid:描述:用户所在家的目录:shell目录 `。其中，`gid`指的是主用户组
>
> 2. /etc/shadow文件内容格式：
>
>    `用户名:$加密算法id$salt(随机数):密码（加密后的）:最后一次修改密码的时间:多长时间内不能改密码：多长时间后必须更改密码`      倒数第二的内容：多长时间后密码失效不可用

#### 用户&组管理

| 指令              |                                                              |
| ----------------- | ------------------------------------------------------------ |
| `groupadd`        | 添加组                                                       |
| `groupdel`        | 删除组                                                       |
| `useradd`         | 添加用户。 `-g`：指定主组    `-G`：指定附加组                |
| `userdel`         | 删除用户,无法删除用户家目录和邮箱，`-r`参数可解              |
| `usermod`         | 改变用户                                                     |
| `passwd username` | root可以更改所有用户密码。普通用户只能修改自己的密码         |
| `change`          | 修改密码  参数查看--help  `-d 0`参数常用于修改初始密码       |
| `gpasswd`         | `-a`：添加用户到组   `-d`：从组中删除用户   `-M`：批量添加用户到组 |

> 1. `useradd`使用`-g`、`-G`时，指定的组必需事先存在。
> 2. `uaseradd`使用`-s /sbin/nologin`设置用户nologin时，应用场景有用户可以访问邮件、ftp、运行进程等，但无法管理系统。
> 3. 原则：主组自动创建，附加组手动指定。
> 4. `usermod`、`gpasswd`将已存在的用户加到组中。usermod的-G参数覆盖原有的附加组。-aG参数则是新增附加组。其`-s /sbin/nologin`参数和useradd用法相同。
> 5. `/etc/login.defs`、 `/etc/default/useradd`影响创建用户时的相关内容
> 6. `useradd`创建用户时从`/etc/skel`复制一套bash环境文件到用户的家目录。

### 文件权限

#### 基本权限设置`r`、`w`、`x`

| 命令      |                                                              |
| --------- | ------------------------------------------------------------ |
| `chown`   | 改变文件属主（所有者）和属组   `-r`参数递归                  |
| `chgrp`   | 改变用户属组（group）                                        |
| `chmod`   | 改变文件权限                                                 |
| `getfacl` | 查看文件（夹）acl权限                                        |
| `setfacl` | 设置文件（夹）acl权限（直接是新增，不会覆盖原ugo权限）。只能是已存在的u、g |

##### 基本权限设置之ugo

u：user      g：group     o：other

>​                 u                +               r(4)
>
>chmod     g                —             w(2)           file
>
>​                 o                =               x(1)
>
>​                 a                                                                                                `a`指`ugo`



##### 基本权限之ACL（FACL）

1. `mask`决定自定义用户和所有组的最高权限（掐头去尾）。应用场景：**临时**修改用户和组的权限。
2. **继承(default)权限**,需要在设置时明确指定。并且继承权限发生在后续动作。

#### 高级权限suid、guid、sticky

1. s：例如passwd程序拥有s权限。那么所有（用户）便可以以root的身份暂时运行passwd程序。
2. g：在新建的文件夹上加上sgid，那么在该文件夹内新创建的文件属组会得到继承（**只继承属组**）。
3. t：目录添加t权限（粘滞位），文件和该目录的所有者能删除，其他人无法删除（此处不包括root）
4. 小写`s`、`t`权限比大写`S`、`T`完全

|        |       文件       |          目录          |
| :----: | :--------------: | :--------------------: |
|  suid  | 以所有者身份执行 |           ——           |
|  sgid  | 以所有组身份执行 |      能够继承属组      |
| sticky |        ——        | 用户只能删除自己的文件 |

> 1. **文件属性：**属性凌驾于权限上
>
> 2. umask:影响新建文件、目录的默认初始权限。不同的进程可以设置自己的umask
>
>    ![1](http://pic.vong.one/Captures/1.png)

### 进程管理

|        |                                                              |
| ------ | ------------------------------------------------------------ |
| pstree | 查看进程树                                                   |
| ps     | 静态查看进程.`--sort`用来（正向）排序，若想反向排序在列名称前加`-`。-f参数可查看树结构 |
| top    | 动态查看进程                                                 |
|        |                                                              |
|        |                                                              |
|        |                                                              |
|        |                                                              |

#### 进程状态解释

![3](http://pic.vong.one/Captures/3.png)

#### top命令

| 参数 | 作用                       |
| ---- | -------------------------- |
| -d   | 后续加秒表明几秒刷新一次   |
| 1    | 刷新界面按1显示所有cpu负载 |

![](http://pic.vong.one/Captures/2-1.png)

#### 使用信号控制进程

1. `kill -l`查看所有控制信号

2. 常用信号

   1) sighup：重新加载配置，pid不变

   2) sigint：相当于`ctrl`+`c`

   3) sigquit：键盘退出

   9) sigkill：强制终止(**轻易不要用**)

   15) sigterm：正常终止，缺省信号

   18) sigcont：继续

   19) sigstop：停止

   20) sigtstp：暂停相当于`ctrl`+`z`

3. **`kill`和`killall`区别**：`kill`只能杀pid和jobid。`killall`跟进程名字。

4. `pkill`: 

   > `pkill -t 终端`：终止终端上的所有进程
   >
   > `pkill -9 -t 终端`：结束终端上所有进程并结束该终端

5. `pgrep`：查看进程id

#### 优先级

cfq调度程序

> 1. nice:相对优先级（屌丝）
> 2. RT、fifo：高富帅

### Linux中的特殊字符

| \|             | 管道符                                                       |
| -------------- | ------------------------------------------------------------ |
| \|\|           | 逻辑关系中表示或                                             |
| !              | 逻辑关系中表示非，                                           |
| #              | 命令行前的#代表root用户，命令行后的#代表注释                 |
| $              | 在linux文件中代表换行符，正则中代表结尾，命令行前代表普通用户 |
| ^              |                                                              |
| >              |                                                              |
| ~              | 目录中代表当前用户的家目录，                                 |
| &              | vim中代表反向引用                                            |
| \              |                                                              |
| ''             |                                                              |
| ""             |                                                              |
| ()             |                                                              |
| []             | 条件测试                                                     |
| {}             | 表示集合                                                     |
| /              |                                                              |
| *              |                                                              |
| ``             |                                                              |
| ..             | 切换目录中代表返回上一层目录                                 |
| .              |                                                              |
| -              | 切换目录中代表退回上一次的目录                               |
| %              | 在vim中表示全文；                                            |
| <<             | 重定向，前面加-代表内容支持table缩进                         |
| (())           | 数值比较和运算                                               |
| `$()`、``      | 命令替换                                                     |
| ${}            | 变量的引用和替换                                             |
| [[]]           | 支持正则的条件测试                                           |
| `$(())`、`$[]` | 整数运算                                                     |
| :              | 可以代表命令ture                                             |
|                |                                                              |

ftp配置文件详解

>

### 变量

变量中包含空格需要用双引号或者单引号引起来，单引号是强引用，双引号是弱引用。

### Tips或注意：

1. 手动删除用相对路径删，脚本删除用绝对路径删
2. 在linux中文件末尾都会默认加上换行符。linux中换行符用`$`表示，windows中用^M表示。所以有的文本，比如脚本如果在windows的**记事本**中修改过将无法在服务器中使用。需要安装dos2unix软件（`yum -y install dos2unix`）。
3. `\etc\bashrc`:bash的配置文件（用来永久修改别名等问题）。
4. Linux有两种时间：linux软件时间、bios硬件时间
5. 在sed和vim中都可以使用分隔符(`!`、`@`、`#`)代替转义符号`\`。
6. vim可同时打开两个文件，使用快捷键`ctrl`+`w`+`w`进行两文件间的切换。退出时`:q`只能退出一个。`qall`能够全部退出
7. uid为0是特权用户
8. 大多数设备只能由root控制
9. 普通用户提权：1.将用户加入wheel组；2.然后在命令前添加sudo。
10. 重启和重新加载：重启是停止+启动；重新加载是reload或者reconfigure。
11. **命令和文件自动补齐：安装**`yum -y install bash-completion`
12. `rpm -qc 程序`：查看程序的配置文件
13. ctrl+z暂停当前前台任务，fg返回暂停任务（用于临时进行任务切换）
14. 命令替换：反引号或者`$()`
15. 查看进程打开了什么文件，使用指令`ls /proc/$pid/fd`(fd:文件描述符)
16. ftp共享目录：`/var/ftp`  配置目录：`/etc/vsftpd/vsftpd.conf`
17. selinux配置目录：`/ect/selinux/config`

18. dns配置文件：`/etc/resolv.conf`