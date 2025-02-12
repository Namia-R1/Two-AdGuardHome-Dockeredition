#  双AdGuardHome一键安装脚本及docker AdGuardHome一键安装版  by [Namia-X]

# 基于你已经安装了docker版agd可以使用模板进行复制和上传，或者docker版自己配置

- 1 文件夹找到 /mnt/mmcblk2p4/adg/confdir1，上传AdGuardHome.yaml到confdir1此为docker版本配置yaml文件上传路径，博主本人只是把它当作了第二分dns用作拦截国内外广告你可以自己找喜欢的dns去改变，如有失效的请提交出来我，我去补充。
- 2 你已经下载了agd并且在服务里面找到了agd你可以直接复制AdGuardHome-cn.yaml此文件里面的，在adg模板手动复制粘贴就行。
- 3 搭配mosdns或者smtdns运行，插件包的agd不作为dns服务器选择无，如果你用我模版记得看对应端口转发和访问端口转发如果不喜欢自行改。
- 4不需要删掉固件自带的agd，你不嫌麻烦可以全docker板agd。

## 其他固件如X86和RK瑞芯微处理器下的op如要使用此脚本，还需要手动创建两个文件夹路径，然后继续运行脚本
     mkdir -p /mnt/mmcblk2p4/adg
     
这个命令适合N1下的openwrt直接创建

     wget https://raw.githubusercontent.com/Namia-R1/Two-docker-agd/main/adg.sh && sh adg.sh  
     
操作顺序
3111100311

#  [`悟空的日常`]( https://github.com/wukongdaily) 所撰写的iStore商店和设置向导 by [wukongdaily]

# 安装iStore商店(ARM64 & x86-64通用)
     wget -qO imm.sh https://cafe.cpolar.top/wkdaily/zero3/raw/branch/main/zero3/imm.sh && chmod +x imm.sh && ./imm.sh
# 安装网络向导和首页(ARM64 & x86-64通用)
     is-opkg install luci-i18n-quickstart-zh-cn

以下是你提供的DNS服务器列表，按**国内**和**国外**分类，并标注了注释，方便你复制和使用：

---

### **国内DNS服务器**
```plaintext
# 阿里DNS（AliDNS）
223.5.5.5
223.6.6.6

# 腾讯DNS（DNSPod）
119.29.29.29

# 百度DNS
180.76.76.76

# 中国电信
101.226.4.6
218.30.118.6

# CNNIC（中国互联网络信息中心）
1.2.4.8
210.2.4.8

# 台湾中华电信
101.101.101.101

# 114DNS
114.114.114.114
114.114.115.115

# OneDNS
117.50.10.10

# 腾讯云DNS
52.80.52.52
```

---

### **国外DNS服务器**
```plaintext
# Google Public DNS
8.8.8.8
8.8.4.4

# Cloudflare DNS
1.1.1.1
1.0.0.1

# dns.sb
185.222.222.222

# AdGuard DNS
94.140.14.14
94.140.15.15

# OpenDNS
208.67.222.222

# Quad9 DNS
9.9.9.9
149.112.112.112
```

---

### **失效的DNS服务器**
```plaintext
# 非常规DNS，不建议使用
101.102.103.104
45.11.45.11
```

---

### **使用说明**
1. **国内DNS**：适合访问国内网站，速度快，推荐阿里DNS、腾讯DNS、114DNS。
2. **国外DNS**：适合访问国际网站，隐私保护强，推荐Cloudflare DNS、Google DNS。
3. **失效DNS**：不建议使用。

---
### **国内推荐的加密DNS服务**
1. **阿里DNS（AliDNS）**  
   - **DoH地址**：
     ```
     https://dns.alidns.com/dns-query
     ```
   - **DoT地址**：
     ```
     dns.alidns.com
     ```

2. **腾讯DNS（DNSPod）**  
   - **DoH地址**：
     ```
     https://doh.pub/dns-query
     ```
   - **DoT地址**：
     ```
     dot.pub
     ```

3. **114DNS**  
   - **DoH地址**：
     ```
     https://dns.114dns.com/dns-query
     ```
   - **DoT地址**：
     ```
     dns.114dns.com
     ```

4. **CNNIC DNS**  
   - **DoH地址**：
     ```
     https://dns.cnnic.cn/dns-query
     ```
   - **DoT地址**：
     ```
     dns.cnnic.cn
     ```

---

### **国际推荐的加密DNS服务**
1. **Cloudflare DNS**  
   - **DoH地址**：
     ```
     https://cloudflare-dns.com/dns-query
     ```
   - **DoT地址**：
     ```
     one.one.one.one
     ```

2. **Google Public DNS**  
   - **DoH地址**：
     ```
     https://dns.google/dns-query
     ```
   - **DoT地址**：
     ```
     dns.google
     ```

3. **Quad9 DNS**  
   - **DoH地址**：
     ```
     https://dns.quad9.net/dns-query
     ```
   - **DoT地址**：
     ```
     dns.quad9.net
     ```

---

国内

百万ADH广告拦截过滤规则

     https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/all.txt

DNS 拦截

     https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt
     https://mirror.ghproxy.com/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt

广告拦截

     https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/light.txt

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
