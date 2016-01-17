写在前面的话：
1、总是鼓吹着使用虚拟机安装Linux操作系统的同志们，请使用WinLy吧。

2、总是埋怨安装Linux和windows之间很难互相删减和引导的网友们，请使用WinLy吧。

3、总是喜欢折腾安装很多的Linux系统尝鲜的朋友们，请使用WinLy吧。


关于winly引导器：
1、WinLy：Windows base Live Linux Installer的缩写，由神雕teasiu与外国的网友noryb009共同制作。
2、这是一个安全的启动引导器，
> 启动什么：通过您本身的windows启动加载器NTLDR或BOOTMGR加载Grub2 for DOS
> 引导什么：Grub2的强大特性，引导您硬盘（任意格式NTFS/FAT/EXT）的ISO镜像/操作系统/文件等
> 为什么安全：WinLy没有改变您的windows系统的结构，仅仅作为一个软件可安装可完全卸载。
3、这是一个强大而且不断更新的GNU系列开源软件Grub2。
4、这是一个免费的软件，仅仅是因为分享与学习的精神而制作。
简单一句话：我将linux下的grub2引导软件移植到windows下，并且仅通过windows启动加载器加载。

关于使用：
1、首先你是在windows2000以上的操作系统下，以管理员身份安装winly引导工具。
2、您的windows系统盘必须显示是C盘。
3、您下载的ISO镜像必须按照指引重命名。（行家或可以自行修改菜单对应）


经过多次测试，完成了软件的制作。

先看看grub2 for dos的启动效果图吧。呵呵.

注：这是在NTFS区启动的grub2 for dos.

由WinLy软件安装注入。windows2000以上的版本全部适用。

简单说说我为什么采用GRUB2 for dos来引导：

winly的前面几次修改都是用grub4dos0.4.5b引导的，
在我无数次的折腾后，发现G4D无法完成在win7的ATA模式的硬盘MEM完整的ISO镜像，(IDE模式硬盘可以)
虽然也很优秀，但是却让我不得不将ISO里面的Vmiuz和initrd2个文件内置到winly才成功。这样，通用性就差了。
所以，我转向了GRUB2 for dos, 采用Ubuntu的内核编译为启动引导文件，就是大家知道的g2ldr。
这样，无论是livecd模式，还是已经安装到硬盘的linux，都可以无忧的启动了。
GRUB2的loop back loop是很强大的。。。。。
整个winly注入器+mbr修复器+菜单编辑器+风格文件+中文内核 总共才2.4M，呵呵。
而且，有些人安装了一键还原或其他的G4D，也不会冲突了。