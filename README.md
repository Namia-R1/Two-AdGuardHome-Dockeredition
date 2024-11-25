# 双adg一键安装脚本docker版 by [Namia-R]
# 基于你已经安装了docker版agd可以使用模板进行复制和上传，或者docker版自己配置

1文件夹找到 /mnt/mmcblk2p4/adg/confdir1，上传AdGuardHome.yaml到confdir1此为docker的上传路径博主本人只是把它当作了第二分dns用作拦截国外广告

2你已经下载了agd并且在服务里面找到了agd你可以直接复制AdGuardHome-cn.yaml此文件里面的
并且在adg手动复制粘贴就行。
3搭配mosdns或者smtdns运行，插件包的agd不作为dns服务器选择无，如果你用我模版记得看对应端口转发和访问端口转发如果不喜欢自行改。
## 其他固件如X86下的op如要使用此脚本，还需要手动创建两个文件夹路径，然后继续运行脚本

     mkdir -p /mnt/mmcblk2p4/adg
     
这个命令适合N1下的openwrt直接创建

     wget https://raw.githubusercontent.com/Namia-R/Two-docker-agd/main/adg.sh && sh adg.sh  
操作顺序

3111100311

# 广告规则

国内纯ip，首选dns

     223.5.5.5
     119.29.29.29
     180.76.76.76
     101.226.4.6
     1.2.4.8
     101.101.101.101
     8.8.8.8
     1.1.1.1
     185.222.222.222
     94.140.14.14
     208.67.222.222
     9.9.9.9
     114.114.114.114	
     117.50.10.10

备用国内外ip，dns

     223.6.6.6
     218.30.118.6
     210.2.4.8
     101.102.103.104
     8.8.4.4
     1.0.0.1
     45.11.45.11
     94.140.15.15
     149.112.112.112
     114.114.115.115
     52.80.52.52

国内加密，180，ip是百度除外

     https://doh.pub/dns-query
     https://dns.alidns.com/dns-query
     https://doh.360.cn
     180.76.76.76

国外加密

     https://dns.google/dns-query
     https://dns.twnic.tw/dns-query
     https://doh.opendns.com/dns-query
     https://cloudflare-dns.com/dns-query

日本dns

     https://doh.dns.sb/dns-query

台湾dns

     https://dns.twnic.tw/dns-query


俄罗斯dns

     https://common.dot.dns.yandex.net

AdGuard dns

     https://dns.adguard-dns.com/dns-query

国内

百万ADH广告拦截过滤规则

     https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/all.txt

DNS 拦截

     https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt
     https://mirror.ghproxy.com/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt

自动更新DNS拦截规则

     https://mirror.ghproxy.com/raw.githubusercontent.com/8680/GOODBYEADS/master/dns.txt
自动更新DNS 白名单

     https://raw.githubusercontent.com/8680/GOODBYEADS/master/allow.txt

广告拦截

     https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/light.txt

广告终结者使用的拦截规则，基于ChinaList+EasyList修正

     http://sub.adtchrome.com/adt-chinalist-easylist.txt

屏蔽一些1024站的弹窗广告和辣鸡澳门赌场的广告

     https://raw.githubusercontent.com/Goooler/1024_hosts/master/hosts

屏蔽一些中国视频网站的广告

     https://raw.githubusercontent.com/jdlingyu/ad-wars/master/hosts

neoHosts-屏蔽 JS Miner 挖矿、百度全家桶的全天候定位记录、各类统计服务（仅屏蔽 JS、不屏蔽控制台）、常见下载劫持、360 和百度的部分软件下载、CNNIC 根证书劫持、法轮功、ISIS、银河联邦等可能令人反感的激进宗教内容网站
标准版-# Basic 

     https://cdn.jsdelivr.net/gh/neoFelhz/neohosts@gh-pages/basic/hosts.txt 

严格版-# Full

     https://cdn.jsdelivr.net/gh/neoFelhz/neohosts@gh-pages/full/hosts.txt 

yhosts-屏蔽绝大多数中国网站以及APP的广告

     https://raw.githubusercontent.com/VeleSila/yhosts/master/hosts.txt

EasyList China —— EasyList针对国内的补充规则

     https://easylist-downloads.adblockplus.org/easylistchina.txt

EasyPrivacy —— 从网络上上完全删除所有形式的跟踪，包括Web错误、跟踪脚本和信息收集，从而保护您的个人数据

     https://easylist-downloads.adblockplus.org/easyprivacy.txt

Anti-AD —— 目前中文区命中率最高的广告过滤列表，实现了精确的广告屏蔽和隐私保护。屏蔽广告域名、电视盒子广告、APP内置广告

     https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/master/anti-ad-easylist.txt

ADgk —— 适用于 AdGuard for Android 的去广告规则（不保证在其他软件使用的效果）

     https://raw.githubusercontent.com/banbendalao/ADgk/master/ADgk.txt

百度搜索结果内屏蔽百家号

     https://raw.githubusercontent.com/banbendalao/ADgk/master/kill-baidu-ad.txt

知乎过滤器 严格版

     标准版：https://raw.githubusercontent.com/zsakvo/AdGuard-Custom-Rule/master/rule/zhihu.txt

     严格版：https://raw.githubusercontent.com/zsakvo/AdGuard-Custom-Rule/master/rule/zhihu-strict.txt

大圣净化 - 针对国内视频网站

     https://raw.githubusercontent.com/jdlingyu/ad-wars/master/hosts


#  国外


EasyList-去除国际网页中大多数广告，包括不需要的框架、图像和对象

     https://easylist-downloads.adblockplus.org/easylist.txt

屏蔽网站的 cookies 相关的警告

     https://www.i-dont-care-about-cookies.eu/abp/

屏蔽美欧地区英文网站相关的广告

     https://winhelp2002.mvps.org/hosts.txt

屏蔽韩国人使用的网站广告

     https://raw.githubusercontent.com/yous/YousList/master/hosts.txt

ADH广告拦截过滤国外规则

     https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/skyrules.txt
