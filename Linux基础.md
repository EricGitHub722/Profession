# Linux基础

#### Linux概论

Client——Server交互

由后端到前端

后端绝大部分服务器都是Linux服务器

Linux服务器有Ubuntu和CentOS

Based on employment

网页都是在基于同一个服务器交互，其内容也是同步的

可以只通过一个终端去操作后端服务器，可以不用安装Linux服务器

根目录：/

在根目录种常见的文件夹：

1. bin各种可执行文件
2. etc各种配置
3. var里面会有log等其它文件，其中log是日志文件
4. lib安装包or静态链接库文件
5. home所有用户的家目录
6. proc存放各种进程相关的信息
7. root是根用户的目录

#### Linux中如何去描述一个路径

1. 绝对路径
2. 相对路径

绝对路径：/home/acs/main.cpp（pwd可以输出一个当前的绝对路径）

相对路径：是从当前目录开始描述的路径

.是当前目录；..是上机目录；~/表示家目录

#### 常用命令介绍

(1) ctrl c: 取消命令，并且换行
(2) ctrl u: 清空本行命令
(3) tab键：可以补全命令和文件名，如果补全不了快速按两下tab键，可以显示备选选项
(4) ls: 列出当前目录下所有文件，蓝色的是文件夹，白色的是普通文件，绿色的是可执行文件
(5) pwd: 显示当前路径
(6) cd XXX: 进入XXX目录下, cd .. 返回上层目录
(7) cp XXX YYY: 将XXX文件复制成YYY，XXX和YYY可以是一个路径，比如../dir_c/a.txt，表示上层目录下的dir_c文件夹下的文件a.txt
(8) mkdir XXX: 创建目录XXX
(9) rm XXX: 删除普通文件;  rm XXX -r: 删除文件夹
(10) mv XXX YYY: 将XXX文件移动到YYY，和cp命令一样，XXX和YYY可以是一个路径；重命名也是用这个命令
(11) touch XXX: 创建一个文件
(12) cat XXX: 展示文件XXX中的内容
(13) 复制文本
    windows/Linux下：Ctrl + insert，Mac下：command + c
(14) 粘贴文本
    windows/Linux下：Shift + insert，Mac下：command + v

### tmux & vim

非常重要，最好能练成条件反射

tmux主要作用：分屏；云端执行