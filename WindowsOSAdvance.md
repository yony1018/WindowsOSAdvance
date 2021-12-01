# WindowsOSAdvance

***

## Configs

### WindowsUpdate

> 如何关闭这个烦人的东西

参考知乎[组策略调更新服务器](https://www.zhihu.com/question/65332770)的方法

> Win+R输入 geddit.msc 打开组策略
>
> > 计算机配置
> >
> > > 管理模板
> > >
> > > > windows组件
> > > >
> > > > > Windows更新
> > > > >
> > > > > > 指定Intranet microsoft更新服务位置
>
> 三个地址框全填任意网址	如: www.baidu.com

### 右键菜单添加命令行打开程序

> 参考：[(49条消息) Windows10右键添加“在此处打开命令窗口”_会意的博客-CSDN博客_在此处打开命令窗口](https://blog.csdn.net/mooneve/article/details/78821843)
>
> 创建并运行 opencmdhere.reg 文件，内容如下
>
> ```
> Windows Registry Editor Version 5.00
> 
> [HKEY_CLASSES_ROOT\Directory\shell\OpenCmdHere]
> @="OpenWithCMD"
> "Icon"="cmd.exe"
> 
> [HKEY_CLASSES_ROOT\Directory\shell\OpenCmdHere\command]
> @="cmd.exe /s /k pushd \"%V\""
> 
> [HKEY_CLASSES_ROOT\Directory\Background\shell\OpenCmdHere]
> @="OpenWithCMD"
> "Icon"="cmd.exe"
> 
> [HKEY_CLASSES_ROOT\Directory\Background\shell\OpenCmdHere\command]
> @="cmd.exe /s /k pushd \"%V\""
> 
> [HKEY_CLASSES_ROOT\Drive\shell\OpenCmdHere]
> @="OpenWithCMD"
> "Icon"="cmd.exe"
> 
> [HKEY_CLASSES_ROOT\Drive\shell\OpenCmdHere\command]
> @="cmd.exe /s /k pushd \"%V\""
> 
> [HKEY_CLASSES_ROOT\LibraryFolder\background\shell\OpenCmdHere]
> @="OpenWithCMD"
> "Icon"="cmd.exe"
> 
> [HKEY_CLASSES_ROOT\LibraryFolder\background\shell\OpenCmdHere\command]
> @="cmd.exe /s /k pushd \"%V\""
> 
> ```
>

### SuperCMD

> [通过 Win + R 默认以管理员身份打开 cmd_草根「幻想家」Blog-CSDN博客](https://blog.csdn.net/qq_42765363/article/details/115214222)
>
> 创建`C:\Windows\System32\cmd.exe`的快捷方式
>
> 放到 `C:\Windows` 目录下
>
> 连后缀一起改为 `scmd`，调整快捷方式为管理员运行
>
> 在Win+R中输入scmd -> SuperCMD

## ShortCuts

> `Alt+Space back` 打开当前激活窗口的窗口操作栏(出现在左上角)
>
> `Alt+Space back -> C` 关闭当前窗口

## ToolS

> Windows有许多超级好用的第三方/官方工具

### PowerToys

### Edge

> ~~不能装插件的浏览器根本用不了~~
>
> Edge官方开发的各种工具属于是天花板了 如: ~~微软数学~~
>
> 尤其是服务器在中国可以同步账号信息
>
> 所以本人认为使用体验由于Chrome

### AquaSnap

> PowerToys和AuqaSnap的组合拳真的让我浴霸(bushi)不能

### Everything

> 我头一次知道找文件能这么快

### QuickLook

### WallpaperEngine

> 平台与资源内容绝对Top1的动态壁纸桌面

### BandiZip

### 傲梅分区助手

### 远程桌面

> 本人可以说是浸淫RDP多年了
>
> 大二那会儿把游戏本卖了之后就满脑子想着云游戏
>
> 渲染任务啥的也都是在家用服务器里跑的

#### 办公效率:WinRDP/ToDesk/向日葵/AnyDesk

> 只要配置好防火墙和加密,WinRDP绝对永远滴神,适应性很高

#### 臭打游戏的:Moonlight

> !!!延迟必须20ms以下!!!
>
> 那想必是Moonlight之类的串流软件:5G网络延迟勉强25ms
>
> ~~(可以自己调教的也就Moonlight了)~~
>
> GeforceNow不用想服务器老远了
>
> SteamLink要花钱的

### 科学上网代理

> 大一小白嘛,就直接买的那些比较知名的VPN,连VPN是啥都不知道hhh
>
> 后来发现只是满足上网需求的话自己架梯子更香

#### Shadowsocks

#### Proifier

#### Clash

### FreeDownloadManager

> 更简洁好用吧算是

### qBittorrent

### XnViewMP 

> 本人视为改名软件用

### CrystalDiskmark&ICrystalDiskInfo

### 写盘软件

> 这种的就很多了,基本不同的osi安装的时候教程里有写哪种就用哪种

#### BalenaEthcer

#### EasyUEFI

### iSlideTools

> PPT制作自动化
>
> ~~普通使用遇到界面大小bug请停用~~

### 格式工厂

### 2345看图王精简优化绿色版

> 2345虽是养蛊,但图片浏览器这东西做的真的好

## DevelopersOperated

### VsStudio

### CMake

### Anaconda

### PuTTy&WinSCP

> 运维必备

### OpenMesh

### MeshLab

### MySQL&Navicat&MSSQL

### Ext2Fsd

## FileManagement

### TreeSize（SpaceSniffer）

> 以文件/文件夹内容大小进行可视化的文件管理工具

### DropIt

> 一键式文件自动化管理工具
>
> ~~调协议文件需要学习成本和精力~~

#### DropItGuidance

### 文件同步

#### Syncthing

> 开源,P2P,云+本地同步=强大

#### EverySync

> 看UI就知道是老大哥Syncthing的发行版本
>
> 是国内的developer在做,所以有中国服务器
>
> 但好用主要是因为有iOS版

#### AllwaySync

> 本地同步软件

### TotalCommand

> 属于是难上加难了属于是

### 系统盘路径结构

> 详见Topbook提供的C盘[路径内容解析](https://topbook.cc/overview?selectedArticle=1707)

## Notes

###  Typora

> 大力感谢我一[哥们](https://github.com/Baix3XiaoRuo)的介绍,否则我还用不上这么好的编辑器
>
> Markdown永远滴神

### BookxNote

> Win端为数不多的几个类Marginnote的软件之一
>
> 功能强大全面的只有这个了

### CAJ知网论文阅读器

## StreamMedia

### Kodi

### Jellyfin

### PotPlayer

