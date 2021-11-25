# win10-ipv6

> Win10下配置Shadowsocks后会每半小时ipv6断开的问题
> 未解决

## 由于教育网和家里的服务器都是原生ipv6，尝试关闭了teredo
>先尝试在组策略中关闭Teredo，6to4，Isatap配置

```
//netsh接口禁用Teredo的设置状态//netsh接口的6to4设置状态禁用//netsh接口isatap设置状态禁用
netsh interface teredo set state disable 
netsh interface 6to4 set state disabled 
netsh interface isatap set state disabled 

//关闭了临时IPv6
netsh interface ipv6 set privacy state=disabled store=active
netsh interface ipv6 set privacy state=disabled store=persistent
netsh interface ipv6 set global randomizeidentifiers=disabled store=active
netsh interface ipv6 set global randomizeidentifiers=disabled store=persistent

ipconfig /release6
ipconfig /renew6
ipconfig /flushdns

ping -6 ipv6.test-ipv6.com

// 重置 IPv6 配置
//不知是不是这里重置ipv6配置这个原因，导致还是不行，实在不行写个每半小时刷新ipv6配置的脚本
netsh interface ipv6 reset
```
>但没用
>
>参考： 前两篇有奇效
>https://github.com/dou4cc/xxwiki/blob/1612ec5025b142fba3d73a6326c16caaf89422d4/IPv6-Win10.md
>
>https://www.cnblogs.com/marsggbo/p/9835467.html
>
>https://zhuanlan.zhihu.com/p/25373553
>
>https://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1842849&ordertype=1