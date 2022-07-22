#### 1.Linux目录结构和作用

 ![计算机生成了可选文字: bin boot Cd「0m dev etc home lib 1tb32 Lib64 Iibx32 lost+found medta mnt opt 「00t sbin Snap swapftle](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png)

Bin：全称binary，含义是二进制。该目录中存储的都是一些二进制文件，文件都是可以被运行的。

Dev：该目录中主要存放的是外接设备，例如盘、其他的光盘等。在其中的外接设备是不能直接被使用的，需要**挂载（类似****windows****下的分配盘符）**。

Etc：该目录主要存储一些配置文件。

Home：表示“家”，表示**除了****root****用户以外其他用户的家目录**，类似于windows下的User/用户目录。

Proc：process，表示进程，该目录中存储的是Linux运行时候的进程。

Root：该目录是root用户自己的家目录。

Sbin：全称super binary，该目录也是存储一些可以被执行的二进制文件，但是必须得有super权限的用户才能执行。

Tmp：表示“临时”的，当系统运行时候产生的临时文件会在这个目录存着。

Usr：存放的是用户自己安装的软件。类似于windows下的program files。

Var：存放的程序/系统的日志文件的目录。

Mnt：当外接设备需要挂载的时候，就需要挂载到mnt目录下。

1. 命令ls

含义：ls （list）

 

**(1)****用法****1****：****#ls**

含义：列出当前工作目录下的所有文件/文件夹的名称

![计算机生成了可选文字: hekun@ubuntu bin dev bootetc Cd「0mhome 、/DesktopSIs/ lib Iibx32 1tb32lost+found 1tb64media mnt opt 「00t sbin Snap swapftle](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)

 

**(2)****用法****2****：****#ls** **路径**

含义：列出指定路径下的所有文件/文件夹的名称

**关于路径（重要）：**

**路径可以分为两种：相对路径、绝对路径。**

**相对路径：相对首先得有一个参照物（一般就是当前的工作路径）；**

**相对路径的写法：在相对路径中通常会用到****2****个符号“****./****”【表示当前目录下】、“****../****”【上一级目录下】。**

**绝对路径：绝对路径不需要参照物，直接****从根“****/****”开始寻找对应路径****；**

 

**(3)ls** **选项 路径**

含义：在列出指定路径下的文件/文件夹的名称，并以指定的格式进行显示。

常见的语法：

\#ls -l 路径

\#ls -la 路径

选项解释：

**-l****：表示****list****，表示以详细列表的形式进行展示**

**-a****：表示显示所有的文件****/****文件夹（包含了隐藏文件****/****文件夹）**

![计算机生成了可选文字: 22：34 d「WX「 00：47 d「WX「 00：47 d「WX「 23：10 16：10 20：31 d「WX「 19：56 22：34 00：54 00：47 -x -x d「WX「一X「一X 2 3 2 2 335 4 31 1 9 2 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 16384 4396 4e96 4e96 O 4e96 84e 8 4e96 4e96 968113383 Jul Feb Feb Jul Jul Jul Jul Jul Feb Feb Jul 11 23 23 11 15 15 15 11 23 23 11 tost+found 22 ：34 medta mnt opt 「00t sbin Snap swapftle usr/sbin](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)

**上述列表中的第一列字符表示文档的类型，****其中“****-****”表示改行对应的文档类型为文件，“****d****”表示文档类型为文件夹****。**

![计算机生成了可选文字: total d「WX「 hekun@ubuntu -la[etc 20:01 22：41 00：50 00：47 00：48 22：51 1116 -x -x -x 13e 3 1 3 2 1 1 5 3 6 4 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 12288 4396 4396 3328 4396 4396 431 433 4e96 4396 4396 4396 769 Jul Jul Feb Feb Feb Jul Jul Oct Feb Feb Jul Feb Jan 15 11 23 23 23 11 16 1 23 23 11 23 18 2e19 2e17 00:48 00：50 22：53 00：50 232e acpt adduser.conf alternatives 「Ontab apg。conf apm apparmor．d apport appstream.conf](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

**在****Linux****中隐藏文档一般都是以“****.****”开头。**

 

**(4)****用法****4****：****#ls -lh** **路径**

含义：列出指定路径下的所有文件/文件夹的名称，以列表的形式并且在显示文档大小的时候以**可读性较高的形式显示**

![计算机生成了可选文字: total d「WX「 d「WX「 hekun@ubuntu -lh/etc 00：50 3KFeb 00：47 00：48 22：51 1．1凹 -x -x -x -x -x -x -x 3 1 3 2 1 1 5 3 6 4 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 4KFeb 4KFeb Jul 4。eK 431 433 4。eK 4。eK 4。3K 4。3K 769 Jul Oct Feb Feb Jul Feb Jan 23 23 23 11 16 1 23 23 11 23 18 2319 2317 00：48 00：50 22：53 00：50 2323 acpi adduser.conf alternatives 「Ontab apg。conf apm apparmor．d apport appst「eam.conf](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)

 

**在****Linux****中有一个特殊的符号“****~****”，****表示当前用户的家目录****。**

 

1. mkdir指令

指令：mkdir  （make directory，创建目录）

 

语法1：**#mkdir** **路径 【路径，可以是文件夹名称也可以是包含名称的一个完整路径】**

![计算机生成了可选文字: 「oot@ubuntu:/#mkdtrntua 「oot@ubuntu:/#Is bin lib dev 1tb32 bootetc Cd「0mhome 1tb64 「oot@ubuntu:/#Is Iibx32 lost+found medta mnt 0「0C 「00t sbin Snap swapftle SS](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

注意：ls列出的结果颜色说明，**其中蓝色的名称表示文件夹**，黑色的表示文件，**绿色的其权限为拥有所有权限**。

 

语法2：**#mkdir -p** **路径**

含义：**当一次性创建多层不存在的目录的时候**，添加-p参数，否则会报错

![计算机生成了可选文字: 「oot@ubuntu:/#mkdt「/ntua/a/b/c mkdt「：cannotc「eatedt「ecto「y'/ntua/a/b/c' NOsuchfile0「directory 「oot@ubuntu ：/#mkdt「一P/ntua/a/b/c 「oot@ubuntu:/#Is bin dev bootetc Cd「0mhome 「oot@ubuntu b 「oot@ubuntu 「oot@ubuntu lib Iibx32 mnt 1tb32lost+foundntua 「00t sbin Snap swapftle SS 1tb64medta ：/#Is/ntua/a ：/#Is/ntua/a/b opt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)

 

语法3：**#mkdir** **路径****1** **路径****2** **路径****3 ….** 【表示一次性创建多个目录】

![计算机生成了可选文字: 「oot@ubuntu:/ntua#cd/ 「oot@ubuntu:/#mkdt「/ntua/b/ntua/c./ntua/d 「oot@ubuntu:/#Is/ntua](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

 

1. touch指令

指令：touch  

作用：创建文件

语法：**#touch** **文件路径**  【路径可以是直接的文件名也可以是路径】

 

(1)使用touch来在当前路径下创建一个文件，命名为Linux.txt

![计算机生成了可选文字: 「oot@ubuntu:/#touch 「oot@ubuntu:/#Is bin lib dev 1tb32 bootetc Cd「0mhome 1tb64 。。txt Iibx32 Linux。txt tost+found media mnt opt 「00t sbin Snap swapftle SYS](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

 

(2)使用touch来同时创建多个文件

![计算机生成了可选文字: 「oot@ubuntu:/#touchntua/a,/ltnuxl.txt./ntua/a,/ltnuxl.txt/ntua/a,/Itnux2.txt 「oot@ubuntu:/#Is/ntua/a/ b Itnuxl.txtItnux2.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

 

(3)使用touch来在“hekun”用户的家目录中创建文件，Linux.txt

![计算机生成了可选文字: 「oot@ubuntu:/#touchtxt 「oot@ubuntu:/#Ishome/hekun/ Desktop DownloadsMusic Public Linux。txt PicturesTemplates Documents test Videos](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

 

1. 指令：cp （copy，复制）

作用：复制文件/文件夹 到 指定的位置

语法：**#cp** **被复制的文档路径** **文档被复制到的路径**

 

(1)使用cp命令来复制一个文件

![计算机生成了可选文字: 「oot@ubuntu：/ntua/a# 「oot@ubuntu：/ntua/a# Itnuxl。txt 「oot@ubuntu：/ntua/a# 「oot@ubuntu：/ntua/a# cp Is cp Is Itnuxl。txt b Itnuxl。txt b 。。txt 。。txt Itnux10.txtItnuxl.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

**注意：****Linux****在复制过程中是可以重新对新位置的文件进行重命名的，但是如果不是必须的需要，则建议保持前后名称一致。**

 

(2)使用cp命令来复制一个文件夹

**注意：当使用****cp****命令进行文件夹复制操作的时候需要添加选项“****-r****”【****-r****表示递归复制】，否则目录将被忽略**

![计算机生成了可选文字: 「oot@ubuntu:/ntua/a#CP-「.[b/c 「oot@ubuntu:/ntua/a#Is Itnuxl.txtItnux2.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

 

1. 指令：mv （move，移动，剪切）

作用：移动文档到新的位置

语法：**#mv** **需要移动的文档路径 需要保存的位置路径**

 

确认：移动之后原始的文件还在不在原来的位置？原始文件是不在原始位置的

 

(1)使用mv命令移动一个文件

![计算机生成了可选文字: 「oot@ubuntu:/ntua/a#Is Itnuxl.txtItnux2.txt 「oot@ubuntu:/ntua/a#mvItnuxl.txt 「oot@ubuntu:/ntua/a#Is Itnux2．txt root@ubuntu:/ntua/a#Is Itnuxl．txt 。。txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

 

(2)使用mv命令移动一个文件夹

![计算机生成了可选文字: 「OOt@UbUntU:/nUJa/a#IS Itnux2．txt 「oot@ubuntu:/ntua/a#mvCb 「oot@ubuntu:/ntua/a#Is b Itnux2．txt 「oot@ubuntu:/ntua/a#Isb Itnux10.txtItnuxl.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image015.png)

 

**补充：在****Linux****中重命名的命令也是****mv****，语法和移动语法一样。**

![计算机生成了可选文字: 「oot@ubuntu:/#Is lib bin dev 1tb32 bootetc 1tb64 Cd「0mhome 「oot@ubuntu:/#Is bin dev boot Iibx32 mnt lost+foundntua medta 「oot@ubuntu:/#mv/ntua/hekunzutntu home lib 1tb32 1tb64 Iibx32 lost+found 「00t media mnt opt sbin Snap 「00t swapftle SS sbin Snap swapftle SS cd「omhekunzutntu](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

 

1. rm指令

指令：rm （remove，移除、删除）

作用：移除/删除文档

语法：#rm 选项 需要移除的文档路径

选项：

-f：force，强制删除，不提示是否删除

-r：表示递归

 

(1)删除一个文件

![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png)

在删除的时候如果不带选项，会提示是否删除，如果需要确认则输入“y/yes”，否则输入“n/no”按下回车。

**注意：如果在删除的时候不想频繁的确认，则可以在指令中添加选项“****-f****”，表示****force****（强制）。**

 

(2)删除一个文件夹

![计算机生成了可选文字: 「oot@ubuntu：/hekunzutntu# Is 「oot@ubuntu：/hekunzutntu# 「oot@ubuntu：/hekunzutntu# adt「ectory Is](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png)

 

(3)删除多个文档

![计算机生成了可选文字: 「oot@ubuntu:/hekunzutntu#「-「a 「oot@ubuntu:/hekunzutntu#Is 「oot@ubuntu:/hekunzutntu#「m-rfb（d 「oot@ubuntu:/hekunzutntu#Is](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png)

 

(4)删除一个目录下有公共特性的文档，例如都以Linux开头

![计算机生成了可选文字: 「oot@ubuntu:/hekunzutntu#Is Itnuxl.txtItnux2.txtLinux3.txt 「oot@ubuntu:/hekunzutntu#「一fLinux* 「oot@ubuntu:/hekunzutntu#Is](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

​    其中*******称之为通配符，意思表示任意的字符，****Linux\*****，则表示只要文件以****Linux****开头，后续字符则不管**。     

1. 输出重定向

**一般命令的输出都会显示在终端中，有些时候需要将一些命令的执行结果想要保存到文件中进行后续的分析****/****统**   **计，则这时候需要使用到的输出重定向技术。**

 

\>：覆盖输出，会覆盖掉原先的文件内容

\>>：追加输出，不会覆盖原始文件内容，会在原始内容末尾继续添加

 

**语法：****#****正常执行的指令** **> / >>** **文件的路径**

注意：文件可以不存在，不存在则新建

 

(1)使用覆盖重定向，保存ls -la 的执行结果，保存到当前目录下的ls.txt

![计算机生成了可选文字: 「oot@ubuntu:/hekunzutntu#Is total8 d「wx「-xr-x2「00t「00t4e96 04：52 d「wxr-xr-x21「00t「00t4e96 02：45 1「00t「00t O 1「00t「00t O 「oot@ubuntu：/hekunzutntu# Is 「oot@ubuntu：/hekunzutntu# Is Itnux3.txt Itnux.txtIs.txt -la Jul Jul Jul Jul -Ia 16 16 16 16 04：52Linux3.txt 04：52Itnux.txt >Is.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image021.png)

 

![计算机生成了可选文字: total 8 05：38 02：45 04：52 04：52 05：38 "Is.txt" 2 21 1 1 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 4e96 4e96 O O O Jul Jul Jul Jul Jul 16 16 16 16 16 Linux3。txt Itnux。txt Is.txt 6 lines, 251characters](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image022.png)

(2)使用追加重定向，保存ls -la的执行结果到ls.txt中

![计算机生成了可选文字: 「oot@ubuntu:/hekunzutntu#Is-la>>Is.txt 「oot@ubuntu:/hekunzutntu#VtIs.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image023.png)

 

![计算机生成了可选文字: total 05：38 02：45 04：52 04：52 05：38 total12 05：42 02：45 04：52 04：52 05：38 "'Is.txt" 2 21 1 1 1 2 21 1 1 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 4e96 4e96 O O O 4e96 4e96 O O 251 Jul Jul Jul Jul Jul Jul Jul Jul Jul Jul 16 16 16 16 16 16 16 16 16 16 Linux3。txt Linux。txt Is.txt Linux3。txt Itnux。txt Is.txt 12 lines, 5e3characters](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image024.png)

1. cat指令

 

**作用****1****：****cat****有直接打开一个文件的功能，查看内容直接输出到控制台，不用退出**

**语法****1****：****#cat** **文件的路径**

![计算机生成了可选文字: total8 total12 d「WX「—W—X hekun@ubuntu./hekunzuiniuscatIs.txt 05：38 02：45 04：52 04：52 05：38 05：42 02：45 04：52 04：52 05：38 2 21 1 1 1 2 21 1 1 1 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「00t 4e96 4396 O O O 4396 4e96 O O 251 Jul Jul Jul Jul Jul Jul Jul Jul Jul Jul 16 16 16 16 16 16 16 16 16 16 Linux3。txt Linux。txt Is.txt Linux3。txt Linux。txt Is.txt hekun@ubuntu：/hekunzLJi.ni.LJS](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image025.png)

 

**作用****2****：****cat****还可以对文件进行合并**

**语法****2****：****#cat** **待合并的文件路径****1** **待合并的文件路径****2 ….** **文件路径****n >** **合并之后的文件路径**

 

(1)合并3个文件，并存到一个文件中【配合输出重定向使用】

![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image026.png)

 

 