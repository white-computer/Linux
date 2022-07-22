- ### 1. hostname指令

- 作用：操作服务器的**主机名**（**读取**、设置）

- 语法1：#hostname      含义：表示输出完整的主机名

- ![](C:/Users/He%20Kun/Documents/GitHub/Linux/advanced-command/clip_image001.png)

- - 1. hostname指令

  - 作用：操作服务器的**主机名**（**读取**、设置）

  -  

  - 语法1：#hostname      含义：表示输出完整的主机名

  - ![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png)

  -  

  - **语法****2****：****#hostname -f**       **含义：表示输出当前主机名中的****FQDN**（全限定**域名**）

  - ![计算机生成了可选文字: hekun@ubuntu.—/testShostname一f UbUntU](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)

  - 1. id指令

  - **作用：查看一个用户的一些基本信息（包含用户****id****，用户组****id****，附加组****id…****），该指令如果不指定用户则默认当前用户。**

  -  

  - 语法1：#id    默认显示当前执行该命令的用户的基本信息

  - ![计算机生成了可选文字: hekun@ubuntu:、/testS utd=1000(hekun)gid=1000(hekun)g「oups=1000(hekun),4(adm)，24（cd「om），27（sudo）,30( dtp),46(plugdev)，120(lpadmtn)，132（×d），133(sambasha「e)](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)

  -  

  - 语法2：#id  用户名     显示指定用户的基本信息

  - ![计算机生成了可选文字: hekun@ubuntu:、/testSid「00t Utd=O(「00t）gid=O（「00t）g「oups=e(「00t） hekun@ubuntu:、/testSidhekun utd=1000(hekun)gid=1000(hekun)g「oups=1000(hekun)，4（ad），24（cd「om），27（sudo）,30( dtp),46(plugdev)，120(lpadmtn)。132（Ixd），133(sambasha「e)](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

  -  

  - 验证上述信息是否正确？

  - **验证用户信息：****cat** **/etc/passwd**

  - ![计算机生成了可选文字: hekun:x:1000::hekun, ：/home/hekun：/btn/bash systemd-co「edump:x:999:999:systemdCO「eDumpe「:/:/usr/sbtn/nologtn](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)

  - **验证用户组信息：****cat** **/etc/group**

  - ![计算机生成了可选文字: hekun@ubuntu:、/testScat/etc/g「oup adm:x:4:sysIog, hekun cd「0：x：24： sudo：x：27：hekun dtp：×：30： plugdev:x:46: Ipadmtn:x:120: Ixd：x：132： ：x：1333： lg「ephekun](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

  -  

  - 1. whoami指令

  - **作用：“我是谁？”显示当前登录的用户名，****一般用于****shell****脚本，用于获取当前操作的用户名方便记录日志****。**

  - 语法：#whoami

  - ![计算机生成了可选文字: hekun@ubuntu.—/testSwhoamt hekun](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)

  -  

  - 1. ps -ef指令（重点）

  - 指令：ps  

  - 作用：主要是查看服务器的进程信息

  - 选项含义：

  - -e：等价于“-A”，表示列出全部的进程

  - -f：显示全部的列（显示全字段）

  - ![计算机生成了可选文字: hekun@ubuntu UID 「00t 「00t 「00t 「00t 「00t 「00t 巧PS PID 1 2 3 4 6 8 -ef PPID C STIME TTY TIME CMD /sbtn/tnttautonop「ompt ：33 [kth「eadd] ：00 ：[「cugp] [「cupa「gp] [kwo「ke「/O:OH-eventshighl ：00 [kwo「ke「/u256：3一e×t4一「sv- ：31](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

  - 列的含义：

  - UID：该进程执行的用户id；

  - PID：进程id；

  - PPID：该进程的父级进程id，如果一个程序的父级进程找不到，该程序的进程称之为僵尸进程（parent process ID）；

  - C：Cpu的占用率，其形式是百分数；

  - STIME：进行的启动时间；

  - TTY：终端设备，发起该进程的设备识别符号，如果显示“?”则表示该进程并不是由终端设备发起；

  - TIME：进程的执行时间；

  - CMD：该进程的名称或者对应的路径；

  -  

  - 案例：（100%使用的命令）在ps的结果中过滤出想要查看的进程状态

  -  

  - **#ps -ef|grep “****进程名称****”**

  - ![计算机生成了可选文字: hekun@ubuntu 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「nOOPS 「nOOPS 「00t 「00t 「00t hekun 巧PS 376 377 38e 383 387 389 391 87e 2549 3e83 3298 3438 -ef lg「ep t00 00：00：00 33：33：33 33：33：33 00：33：00 00：00：00 33：33：33 00：00：00 33：33：33 33：33：33 100 PO] PI] p2] p3] p4] p5] /us「/sbtn/ke「ne /us「/sbtn/ke「ne p8] PS PS 1837 O 38 ：32 pts/e —COLO「 100 g「ep](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

  -  

  - 1. top指令（重点）

  - **作用：查看服务器的进程占的资源（****100%****使用）**

  - 语法：

  - 进入命令：#top      （动态显示）

  - 退出命令：按下q键

  -  

  - ![计算机生成了可选文字: Tasks:273total, hekun@ubuntu./Stop top-e8：42：39up36min， 1， O．7 1。2 O．7 1．7 3：35 O。7 O。2 O：00 O．3 e。5 3：33 O．3 1。6 O：33 2「unntng,271 loadave「age：e．37，e．31，O。32 Ostopped, Ozombie sleeping, %CPU(S)： 4.0us 1Be 1941 凹1BSwap： 923 PID USER hekun 1532 hekun 1712 hekun 1827 hekun 3776 「00t 1 hekun 1361 「00t 2 「00t 3 「00t 4 「00t 6 「00t 9 「00t 3。OSY。 。1total, ·3total, O。Ont, 87。9id。 5。1 687。9 2e1。3 wa，O。Ohi,O。Ost,O。Ost 5e1 721 VIRT 339e152 291916 814736 11992 168838 288636 。6 ·9 *CPU 751。6 1e87。O *MEM buff/cache avail TIME+ PR 20 20 20 20 20 20 NI O O O O O O RES 165544 23668 33852 3772 1e88e 3e856 SHR 46783 16484 21296 3008 6496 1134e O O O O O O S S S S R S S S I I I I S ：33 O：34．35 O：17．97 O：33．31 ．89 ．70 .05 。43 Mem COMMAND S十 vmtoolsd gnome一t+ top systemd XO「g kth「eadd 「Cugp 「Cpa「十 「C十 「C](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

  - 表头含义：

  - PID：进程id；

  - USER：该进程对应的用户；

  - PR：优先级；

  - VIRT：虚拟内存；

  - RES：常驻内存；

  - SHR：共享内存；

  - 计算一个进程实际使用的内存 = 常驻内存（RES）- 共享内存（SHR）

  - S：表示进程的状态status（sleeping，其中S表示睡眠，R表示运行）；

  - %CPU：表示CPU的占用百分比；

  - %MEM：表示内存的占用百分比；

  - TIME+：执行的时间；

  - COMMAND：进程的名称或者路径；

  -  

  - **在运行****top****的时候，可以按下方便的快捷键：**

  - M：表示将结果按照内存（MEM）从高到低进行降序排列；

  - P：表示将结果按照CPU使用率从高到低进行降序排列；

  - 1：当服务器拥有多个cpu的时候可以使用“1”快捷键来切换是否展示显示各个cpu的详细信息；

  -  

  - 1. du -sh指令

  - 作用：查看目录的真实大小

  - **语法：****#du -sh** **目录路径**

  - 选项含义：

  - -s：summaries，只显示汇总的大小

  - -h：表示以高可读性的形式进行显示

  - ![计算机生成了可选文字: hekun@ubuntu:/Sdu-sh/home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxall.txt 4。eK hekun@ubuntu:./Sdu-s/home/hekun/test/ltnuxall.txt 4 /home/hekun/test/ltnuxall.txt hekun@ubuntLJ:/Sdu-sh/home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxall。txt 4．OK](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

  -  

  - 1. find指令

  - 作用：用于查找文件（其参数有55个之多）

  - 语法：#**find** **路径范围 选项 选项的值**

  - 选项：

  - -name：按照文档名称进行搜索（支持模糊搜索）

  - -type：按照文档的类型进行搜索

  - **文档类型：“****-****”表示文件（在使用****find****的时候需要用****f****来替换），“****d****”表示文件夹**

  - ![计算机生成了可选文字: hekun@ubuntu:/Sfind/home/hekun/test /home/hekun/test/ltnux．txt /home/hekun/test/test.txt /home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxl．txt /home/hekun/test/ltnux2．txt hekun@ubuntu:/Sfind/home/hekun/test /home/hekun/test /home/hekun/testL1 一typef 一typed](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

  - 案例：搜索etc目录下所有的conf后缀文件

  - ![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

  -  

  - 1. service指令（重点）

  - 作用：用于控制一些软件的服务启动/停止/重启

  - **语法：****#service** **服务名** **start/stop/restart**

  -  

  - 1. kill指令（重点）

  - **作用：表示杀死进程**     （当遇到僵尸进程或者出于某些原因需要关闭进程的时候）

  - 语法：**#kill** **进程****PID**    （语法需要配合ps一起使用）

  -  

  -  

  - 与kill命令作用相似但是比kill更加好用的杀死进程的命令：killall

  - 语法：**#killall** **进程名称**

  -  

  - 1. ifconfig指令（重点）

  - **作用：用于操作网卡相关的指令。**

  - 简单语法：#ifconfig    （获取网卡信息）

  - ![计算机生成了可选文字: 「oot@ubuntu:/#tfconftg flags=4163<UP，BROADCAST,RUNNING，MULTICAST>mtu1500 ens33: tnet192。168。83。128netmask255．255．255．Ob「oadcast192。168。83。255 七℃辶5|e：：：0上3：5f2d：9c4dp「eftxlen64scopetdex20<Itnk> ethe「00：Oc：29：ff：ed：1atxqueuelen1333(Ethe「net) RXpackets3222e5bytes431238395（431．28） 10。 RXe「「0「sOd「oppedOove「「unSOf「ameO TXpackets52611bytes3436337（3．48） TXe「「0「sOd「oppedeove「「unSecar「terO flags=73<UP。LOOPBACK，RUNNING>mtu65536 iner1z／。e。e。1netmask255。O。3。O ：P》128scopetdOxlO<host> tnec looptxqueuelen133e(LocalLoopback) RXpackets953bytes96629（96．6KB） RXe「「0「sOd「oppedOove「「unSef「ameO TXpackets953bytes96629（96．6KB） TXe「「0「sOd「oppedOove「「unSeca「rterO collisionsO collisionsO](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

  - ens33表示Linux中的一个网卡，ens33是其名称。Lo（**loop****，本地回还网卡，其****ip****地址一般都是****127.0.0.1**）也是一个网卡名称。

  - **注意：****inet** **就是网卡的****ip****地址**。

  -  

  - 1. reboot指令

  - 作用：重新启动计算机    

  - **语法****1****：****#reboot**    **重启**

  - 语法2：#reboot  -w  模拟重启，但是不重启（只写关机与开机的日志信息）

  -  

  - 1. shutdown指令

  - 作用：关机      （慎用）

  - **语法****1****：****#shutdown -h now  “****关机提示****”** **或者** **#shutdown  -h 15:25 “****关机提示****”**

  - 案例：设置Linux系统关机时间在12:00

  -  

- 语法2：#hostname -f       含义：表示输出当前主机名中的FQDN（全限定域名）

- ![](C:\Users\He Kun\Documents\GitHub\Linux\advanced-command\clip_image002.png)

- 1. id指令

- **作用：查看一个用户的一些基本信息（包含用户****id****，用户组****id****，附加组****id…****），该指令如果不指定用户则默认当前用户。**

-  

- 语法1：#id    默认显示当前执行该命令的用户的基本信息

- ![计算机生成了可选文字: hekun@ubuntu:、/testS utd=1000(hekun)gid=1000(hekun)g「oups=1000(hekun),4(adm)，24（cd「om），27（sudo）,30( dtp),46(plugdev)，120(lpadmtn)，132（×d），133(sambasha「e)](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)

-  

- 语法2：#id  用户名     显示指定用户的基本信息

- ![计算机生成了可选文字: hekun@ubuntu:、/testSid「00t Utd=O(「00t）gid=O（「00t）g「oups=e(「00t） hekun@ubuntu:、/testSidhekun utd=1000(hekun)gid=1000(hekun)g「oups=1000(hekun)，4（ad），24（cd「om），27（sudo）,30( dtp),46(plugdev)，120(lpadmtn)。132（Ixd），133(sambasha「e)](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

-  

- 验证上述信息是否正确？

- **验证用户信息：****cat** **/etc/passwd**

- ![计算机生成了可选文字: hekun:x:1000::hekun, ：/home/hekun：/btn/bash systemd-co「edump:x:999:999:systemdCO「eDumpe「:/:/usr/sbtn/nologtn](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)

- **验证用户组信息：****cat** **/etc/group**

- ![计算机生成了可选文字: hekun@ubuntu:、/testScat/etc/g「oup adm:x:4:sysIog, hekun cd「0：x：24： sudo：x：27：hekun dtp：×：30： plugdev:x:46: Ipadmtn:x:120: Ixd：x：132： ：x：1333： lg「ephekun](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

-  

- 1. whoami指令

- **作用：“我是谁？”显示当前登录的用户名，****一般用于****shell****脚本，用于获取当前操作的用户名方便记录日志****。**

- 语法：#whoami

- ![计算机生成了可选文字: hekun@ubuntu.—/testSwhoamt hekun](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)

-  

- 1. ps -ef指令（重点）

- 指令：ps  

- 作用：主要是查看服务器的进程信息

- 选项含义：

- -e：等价于“-A”，表示列出全部的进程

- -f：显示全部的列（显示全字段）

- ![计算机生成了可选文字: hekun@ubuntu UID 「00t 「00t 「00t 「00t 「00t 「00t 巧PS PID 1 2 3 4 6 8 -ef PPID C STIME TTY TIME CMD /sbtn/tnttautonop「ompt ：33 [kth「eadd] ：00 ：[「cugp] [「cupa「gp] [kwo「ke「/O:OH-eventshighl ：00 [kwo「ke「/u256：3一e×t4一「sv- ：31](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

- 列的含义：

- UID：该进程执行的用户id；

- PID：进程id；

- PPID：该进程的父级进程id，如果一个程序的父级进程找不到，该程序的进程称之为僵尸进程（parent process ID）；

- C：Cpu的占用率，其形式是百分数；

- STIME：进行的启动时间；

- TTY：终端设备，发起该进程的设备识别符号，如果显示“?”则表示该进程并不是由终端设备发起；

- TIME：进程的执行时间；

- CMD：该进程的名称或者对应的路径；

-  

- 案例：（100%使用的命令）在ps的结果中过滤出想要查看的进程状态

-  

- **#ps -ef|grep “****进程名称****”**

- ![计算机生成了可选文字: hekun@ubuntu 「00t 「00t 「00t 「00t 「00t 「00t 「00t 「nOOPS 「nOOPS 「00t 「00t 「00t hekun 巧PS 376 377 38e 383 387 389 391 87e 2549 3e83 3298 3438 -ef lg「ep t00 00：00：00 33：33：33 33：33：33 00：33：00 00：00：00 33：33：33 00：00：00 33：33：33 33：33：33 100 PO] PI] p2] p3] p4] p5] /us「/sbtn/ke「ne /us「/sbtn/ke「ne p8] PS PS 1837 O 38 ：32 pts/e —COLO「 100 g「ep](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

-  

- 1. top指令（重点）

- **作用：查看服务器的进程占的资源（****100%****使用）**

- 语法：

- 进入命令：#top      （动态显示）

- 退出命令：按下q键

-  

- ![计算机生成了可选文字: Tasks:273total, hekun@ubuntu./Stop top-e8：42：39up36min， 1， O．7 1。2 O．7 1．7 3：35 O。7 O。2 O：00 O．3 e。5 3：33 O．3 1。6 O：33 2「unntng,271 loadave「age：e．37，e．31，O。32 Ostopped, Ozombie sleeping, %CPU(S)： 4.0us 1Be 1941 凹1BSwap： 923 PID USER hekun 1532 hekun 1712 hekun 1827 hekun 3776 「00t 1 hekun 1361 「00t 2 「00t 3 「00t 4 「00t 6 「00t 9 「00t 3。OSY。 。1total, ·3total, O。Ont, 87。9id。 5。1 687。9 2e1。3 wa，O。Ohi,O。Ost,O。Ost 5e1 721 VIRT 339e152 291916 814736 11992 168838 288636 。6 ·9 *CPU 751。6 1e87。O *MEM buff/cache avail TIME+ PR 20 20 20 20 20 20 NI O O O O O O RES 165544 23668 33852 3772 1e88e 3e856 SHR 46783 16484 21296 3008 6496 1134e O O O O O O S S S S R S S S I I I I S ：33 O：34．35 O：17．97 O：33．31 ．89 ．70 .05 。43 Mem COMMAND S十 vmtoolsd gnome一t+ top systemd XO「g kth「eadd 「Cugp 「Cpa「十 「C十 「C](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

- 表头含义：

- PID：进程id；

- USER：该进程对应的用户；

- PR：优先级；

- VIRT：虚拟内存；

- RES：常驻内存；

- SHR：共享内存；

- 计算一个进程实际使用的内存 = 常驻内存（RES）- 共享内存（SHR）

- S：表示进程的状态status（sleeping，其中S表示睡眠，R表示运行）；

- %CPU：表示CPU的占用百分比；

- %MEM：表示内存的占用百分比；

- TIME+：执行的时间；

- COMMAND：进程的名称或者路径；

-  

- **在运行****top****的时候，可以按下方便的快捷键：**

- M：表示将结果按照内存（MEM）从高到低进行降序排列；

- P：表示将结果按照CPU使用率从高到低进行降序排列；

- 1：当服务器拥有多个cpu的时候可以使用“1”快捷键来切换是否展示显示各个cpu的详细信息；

-  

- 1. du -sh指令

- 作用：查看目录的真实大小

- **语法：****#du -sh** **目录路径**

- 选项含义：

- -s：summaries，只显示汇总的大小

- -h：表示以高可读性的形式进行显示

- ![计算机生成了可选文字: hekun@ubuntu:/Sdu-sh/home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxall.txt 4。eK hekun@ubuntu:./Sdu-s/home/hekun/test/ltnuxall.txt 4 /home/hekun/test/ltnuxall.txt hekun@ubuntLJ:/Sdu-sh/home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxall。txt 4．OK](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

-  

- 1. find指令

- 作用：用于查找文件（其参数有55个之多）

- 语法：#**find** **路径范围 选项 选项的值**

- 选项：

- -name：按照文档名称进行搜索（支持模糊搜索）

- -type：按照文档的类型进行搜索

- **文档类型：“****-****”表示文件（在使用****find****的时候需要用****f****来替换），“****d****”表示文件夹**

- ![计算机生成了可选文字: hekun@ubuntu:/Sfind/home/hekun/test /home/hekun/test/ltnux．txt /home/hekun/test/test.txt /home/hekun/test/ltnuxall.txt /home/hekun/test/ltnuxl．txt /home/hekun/test/ltnux2．txt hekun@ubuntu:/Sfind/home/hekun/test /home/hekun/test /home/hekun/testL1 一typef 一typed](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

- 案例：搜索etc目录下所有的conf后缀文件

- ![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

-  

- 1. service指令（重点）

- 作用：用于控制一些软件的服务启动/停止/重启

- **语法：****#service** **服务名** **start/stop/restart**

-  

- 1. kill指令（重点）

- **作用：表示杀死进程**     （当遇到僵尸进程或者出于某些原因需要关闭进程的时候）

- 语法：**#kill** **进程****PID**    （语法需要配合ps一起使用）

-  

-  

- 与kill命令作用相似但是比kill更加好用的杀死进程的命令：killall

- 语法：**#killall** **进程名称**

-  

- 1. ifconfig指令（重点）

- **作用：用于操作网卡相关的指令。**

- 简单语法：#ifconfig    （获取网卡信息）

- ![计算机生成了可选文字: 「oot@ubuntu:/#tfconftg flags=4163<UP，BROADCAST,RUNNING，MULTICAST>mtu1500 ens33: tnet192。168。83。128netmask255．255．255．Ob「oadcast192。168。83。255 七℃辶5|e：：：0上3：5f2d：9c4dp「eftxlen64scopetdex20<Itnk> ethe「00：Oc：29：ff：ed：1atxqueuelen1333(Ethe「net) RXpackets3222e5bytes431238395（431．28） 10。 RXe「「0「sOd「oppedOove「「unSOf「ameO TXpackets52611bytes3436337（3．48） TXe「「0「sOd「oppedeove「「unSecar「terO flags=73<UP。LOOPBACK，RUNNING>mtu65536 iner1z／。e。e。1netmask255。O。3。O ：P》128scopetdOxlO<host> tnec looptxqueuelen133e(LocalLoopback) RXpackets953bytes96629（96．6KB） RXe「「0「sOd「oppedOove「「unSef「ameO TXpackets953bytes96629（96．6KB） TXe「「0「sOd「oppedOove「「unSeca「rterO collisionsO collisionsO](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

- ens33表示Linux中的一个网卡，ens33是其名称。Lo（**loop****，本地回还网卡，其****ip****地址一般都是****127.0.0.1**）也是一个网卡名称。

- **注意：****inet** **就是网卡的****ip****地址**。

-  

- 1. reboot指令

- 作用：重新启动计算机    

- **语法****1****：****#reboot**    **重启**

- 语法2：#reboot  -w  模拟重启，但是不重启（只写关机与开机的日志信息）

-  

- 1. shutdown指令

- 作用：关机      （慎用）

- **语法****1****：****#shutdown -h now  “****关机提示****”** **或者** **#shutdown  -h 15:25 “****关机提示****”**

- 案例：设置Linux系统关机时间在12:00

-  