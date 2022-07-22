- 1. df指令

- 作用：查看磁盘的空间

- **语法：****#df -h**   

- **-h****表示以可读性较高的形式展示大小**

- ![计算机生成了可选文字: hekun@ubuntu Filesystem tmpfs /dev/sda5 tmpfs tmpfs tmpfs /dev/loope /dev/loop2 /dev/loop3 /dev/loopl /dev/loop4 /dev/loop6 /dev/loop5 /dev/sdal tmpfs $df —/test 1K-bIocks 963364 198768 19992176 993836 5123 993836 128 63488 254848 63488 66816 44672 55552 523248 198764 Used O 1496 8168216 O 4 O 128 63488 254848 63488 66816 44672 55552 4 20 Available 963364 197272 1e785368 993836 5116 993836 O O O O O O O 523244 198744 Mounted0n Use% 0%/dev 1％ 44％/ 0%/dev/shm 1％/「un/lock /sys/fs/cg「oup 0% /snap/ba「e/5 133％ /snap/CO「e23/1518 133％ /snap/gnome-3-38-2004/99 133％ /snap/CO「e23/1328 133％ /snap/gtk-common-themes/1519 133％ /snap/snapd/14978 133％ /snap/snap-store/558 1e3％ 1％/boot/eft /「un/use「11000 1％](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png)

-  

- ![计算机生成了可选文字: hekun@ubuntu Filesystem tmpfs /dev/sda5 tmpfs tmpfs tmpfs /dev/loope /dev/loop2 /dev/loop3 /dev/loopl /dev/loop4 /dev/loop6 /dev/loop5 /dev/sdal tmpfs —/test Size 938凹 195凹 23G 971凹 971凹 128K 62 249凹 62凹 66凹 44凹 55凹 511凹 195凹 Used O 1．5凹 7。8G O 4。eK O 128K 62 249凹 62 66 44凹 55 4。3K 23K Avail 938 193凹 11C 971凹 971凹 O O O O O O O 511凹 195凹 Mounted0n Use% 0%/dev 1％ 44％ 0%/dev/shm 1％/「un/lock /sys/fs/cg「oup 0% /snap/ba「e/5 133％ /snap/CO「e23/1518 133％ /snap/gnome-3-38-2004/99 133％ /snap/co「e2e/1328 133％ /snap/gtk-common-themes/1519 133％ /snap/snapd/14978 133％ /snap/snap-sto「e/558 1e3％ 1％/boot/eft /「un/use「/IOOO 1％](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)

-  

- 1. free

- 作用：查看内存使用情况

- **语法：****#free -m  -m****表示以****mb****为单位查看** **-g****表示以****gb****为单位查看**

- ![计算机生成了可选文字: hekun@ubuntu.—/test 88478e sha「ed 1812 buff/cache 635343 available 951388 Mem： Swap： total 1987672 945416 467552 945416](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)

-  

- ![计算机生成了可选文字: shared 1 Mem： Swap： 、[test total 1941 923 84e buff/cache 622 available 952 478 923](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

-  

- ![计算机生成了可选文字: hekun@ubuntu Swap： 、[test total 1 shared buff/cache available](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)

- Swap：用于临时内存，当系统真实内存不够用的时候可以临时使用磁盘空间来充当内存。

-  

- 1. head

- 作用：查看一个文件的前n行，如果不指定n，则默认显示前10行。

- **语法：****#head -n** **文件路径**  **【****n****表示数字】**

- ![计算机生成了可选文字: hekun@ubuntu total76 d「闪×「一x「一x15 06：12 d「闪×「一X「一X3 22：49 22：49 —/testShead -n8 4396 4396 637 22e 3771 4396 4396 Itnuxall.txt 1 1 1 10 13 hekun 「00t hekun hekun hekun hekun hekun hekun 「00t hekun hekun hekun hekun hekun Jul Jul Jul Jul Jul Jul Jul 16 11 16 11 11 11 16 35 22 23 36 ：49 ：49 ：17 ：39 .bashhisto「y .bashlogOUt .bash「c ．config](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

-  

- 1. tail

- 作用1：查看一个文件的未n行，如果n不指定默认显示后10行

- **语法：****#tail -n** **文件的路径**   **n****同样表示数字**

- ![计算机生成了可选文字: d「WX「WX「 d「WX「一X「 hekun@ubuntu 23：15 23：15 23：15 06：13 23：15 —/testStail -n10Itnuxall.txt -x -x -x -x -x -x -x 3 3 2 2 1 2 1 2 3 2 hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun hekun 4e96 4396 4e96 4e96 837 4e96 O 4e96 4e96 4396 Jul Jul Jul Jul Jul Jul Jul Jul Jul Jul 11 11 11 11 11 11 15 11 16 11 23 23 22 19 23 ：15 ：15 ：49 ：46 ：15 •gnupg ．local Pictu「es .p「oftle Public ．sudOaS Templates test Videos](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)

-  

- 作用2：可以通过tail指令来查看一个文件的动态变化内容【**变化的内容不能是用户手动增加的**】

- **语法：****#tail -f** **文件路径**

- **利用输出重定向功能，将内容写入指定文件**

- **该命令一般用于查看系统的日志比较多。**

-  

- 1. less指令

- 作用：查看文件，以较少的内容进行输出，按下辅助功能键（数字+回车、**空格键**+上下方向键）查看更多

- **语法：****#less** **需要查看的文件路径**

- ![img](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

- 在退出的只需要按下q键即可。

-  

- 1. wc指令

- 作用：统计文件内容信息（包含行数、单词数、字节数）

- 语法：**#wc -lwc** **需要统计的文件路径**

- **-l****：表示****lines****，行数**

- -w：表示words，单词数  依照空格来判断单词数量

- -c：表示bytes，字节数

- ![计算机生成了可选文字: hekun@ubuntu:、/testSWC Itnuxall.txt 635463195Itnuxall.txt hekun@ubuntu:、/testSwc Itnuxall.txt 63Itnuxall.txt hekun@ubuntu:、[test $WC Itnuxall.txt 546Itnuxall.txt hekun@ubuntu:、[test $WC Itnuxall.txt 3195Itnuxall.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

-  

- 1. date指令（重点）

- 作用：表示操作时间日期（**读取**、设置）

- 语法1：#date   

- ![计算机生成了可选文字: hekun@ubuntu:、/DesktopSdate on18Jul2e2212：26：40AMPDT](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

-  

- 语法2：**#date +%F**  **（等价于** **#date “+%Y-%m-%d”** **）** 

- ![计算机生成了可选文字: hekun@ubuntu 2e22一07一18 hekun@ubuntu 2322一37一18 —/DesktopSdate十％F —/DesktopSdate十％Y一一％d](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

-  

- 语法3：#date  “+%F %T”  **引号表示让“年月日与时分秒”成为一个不可分割的整体**

- **等价操作****#date “+%Y-%m-%d %H:%M:%S”**

- ![计算机生成了可选文字: hekun@ubuntu 、/DesktopSdate 2e22一07一1800：37：24 hekun@ubuntu 、/DesktopSdate 2322一37一1800：37：26 "十％F%T"](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

-  

- 语法4：获取之前或者之后的某个时间（备份）

- \#date -d “**-**1 **day**” “+%Y-%m-%d %H:%M:%S”

- ![计算机生成了可选文字: hekun@ubuntu —/DesktopS 2e22一07一17 hekun@ubuntu —/DesktopS 2e22一07一1700：44：29 hekun@ubuntu —/DesktopS 2e22一07一17 hekun@ubuntu —/DesktopS 2e22一07一1700：45：24 date date date date -d1day' -d1day' -d1day' -d1day' "十％F%T" 十％F](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

- 符号的可选值：+（之后） 或者 - （之前）

- ![计算机生成了可选文字: hekun@ubuntu 、/DesktopS 2e22一07一1700：45：24 hekun@ubuntu 、/DesktopS 2322一37一1900：45：59 date date -d》一1day' -d "十1day'](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

- 单位的可选值：day（天）、month（月份）、year（年）

- ![计算机生成了可选文字: hekun@ubuntu 、/DesktopS 2e22一08一1800：46：38 hekun@ubuntu 、/DesktopS 2323一37一1800：46：48 date date -d -d "十1 "十1 month'](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image015.png)

- **%F****：表示完整的年月日**

- **%T****：表示完整的时分秒**

- **%Y****：表示四位年份**

- **%m****：表示两位月份（带前导****0****）**

- **%d****：表示日期（带前导****0****）**

- **%H****：表示小时（带前导****0****）**

- **%M****：表示分钟（带前导****0****）**

- **%S****：表示秒数（带前导****0****）**

- 1. cal

- **作用：用来操作日历的**

- **语法****1****：****#cal**   **等价于** **#cal -1**     直接输出当前月份的日历

- ![计算机生成了可选文字: hekun@ubuntu：、/DesktopScal July2322 Su 10 24 11 25 Tu 12 19 26 We 13 20 27 Th 14 21 28 Fr 15 22 29 Sa 16 23 30](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

- **语法****2****：****#cal -3**      表示输出上一个月+本月+下个月的日历

- ![计算机生成了可选文字: hekun@ubuntu：、/DesktopScal 一1 July2e22 Su 10 24 11 25 Tu 12 19 26 13 20 27 Th 14 21 28 Fr 15 22 29 Sa 16 23 30](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png)

- **语法****3****：****#cal -y** **年份**      表示输出某一个年份的日历

- ![计算机生成了可选文字: hekun@ubuntu.—/DesktopScal January -y2e22 2e22 Feb「uary March Su 9 16 23 Su 10 17 24 10 17 24 11 18 25 Tu 11 18 25 We 12 19 26 AP「 Tu 12 19 26 We 13 20 27 Th 13 20 27 Th 14 21 28 Fr 14 21 28 Fr 15 22 29 Sa 1 15 22 29 Sa 16 23 30 Su 6 13 20 27 Su 8 15 22 29 7 14 21 28 9 16 23 30 Tu 8 15 22 Tu 10 17 24 31 We 9 16 23 May We 11 18 25 Th 10 17 24 Th 12 19 26 Fr 11 18 25 Fr 13 20 27 Sa 12 19 26 Sa 14 21 28 Su 6 13 20 27 Su 5 12 19 26 7 14 21 28 6 13 20 27 Tu 8 15 22 29 Tu 7 14 21 28 9 16 23 30 We 8 15 22 29 Th 10 17 24 31 Th 9 16 23 30 Fr 11 18 25 Fr 10 17 24 Sa 12 19 26 Sa 11 18 25](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png)

- 1. clear / ctrl+L指令

- 作用：清除终端中已经存在的命令和结果（信息）。

- **语法：****clear**    **或者快捷键：****ctrl + L**

- 1. 管道（重要）

- **管道符：****|**

- 作用：管道一般可以用于“**过滤**”，“特殊”，“扩展处理”。

- 语法：管道不能单独使用，必须需要配合前面所讲的一些指令来一起使用，其作用**主要是辅助作用**。

-  

- (1)过滤：需要通过管道查询出根目录下包含“y”字母的文档名称。

- ![计算机生成了可选文字: hekun@ubuntu:/SIs bin dev home lib bootetc cd「omhekunzutntu 1tb32 hekun@ubuntu:/SIs/]g「eP hekun@ubuntu:/SIs/]g「eP •tc hkunzutntu ho mdia swapftl 1tb64 Iibx32 lost+found Y media mnt opt 「00t sbin Snap swapftle SS](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png)

- **针对上面这个命令说明：**

- **①以管道作为分界线，****前面的命令有个输出，后面需要先输入，然后再过滤，最后再输出，通俗的讲就是管道前面的输出就是后面指令的输入****；**

- **②****grep****指令：****主要用于过滤**

-  

- (2)特殊：通过管道的操作方法来实现less的等价效果（了解）

- 之前通过less查看一个文件，可以#less 路径

- 现在通过管道还可以这么：#cat 路径|less

-  

-  

- ③扩展处理：请使用学过的命令，来统计某个目录下的文档的总个数？

- **答：****#ls / | wc -l**

- ![计算机生成了可选文字: hekun@ubuntu Itnuxl。txt 1 hekun@ubuntu 6 、[test Itnux2.txtItnuxall.txt —/test Linux。txt test.txt](file:///C:/Users/He%20Kun/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

-  