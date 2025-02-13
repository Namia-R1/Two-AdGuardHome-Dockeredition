#  双AdGuardHome一键安装脚本及docker AdGuardHome一键安装版  by [Namia-X]

### **基于你已经安装了docker版agd可以使用模板进行复制和上传，或者docker版自己配置

- 1 文件夹找到 /mnt/mmcblk2p4/adg/confdir1，上传AdGuardHome.yaml到confdir1此为docker版本配置yaml文件上传路径，博主本人只是把它当作了第二分dns用作拦截国内外广告你可以自己找喜欢的dns去改变，如有失效的请提交出来我，我去补充。
- 2 你已经下载了agd并且在服务里面找到了agd你可以直接复制AdGuardHome-cn.yaml此文件里面的，在adg模板手动复制粘贴就行。
- 3 搭配mosdns或者smtdns运行，插件包的agd不作为dns服务器选择无，如果你用我模版记得看对应端口转发和访问端口转发如果不喜欢自行改。
- 4不需要删掉固件自带的agd，你不嫌麻烦可以全docker板agd。

### **其他固件如X86和RK瑞芯微处理器下的op如要使用此脚本，还需要手动创建两个文件夹路径，然后继续运行脚本
     mkdir -p /mnt/mmcblk2p4/adg
     
这个命令适合N1下的openwrt直接创建

     wget https://raw.githubusercontent.com/Namia-R1/Two-docker-agd/main/adg.sh && sh adg.sh  
     
操作顺序
3111100311

### **[`悟空的日常`]( https://github.com/wukongdaily) 所撰写的iStore商店和设置向导 by [wukongdaily]

### **安装iStore商店(ARM64 & x86-64通用)
     wget -qO imm.sh https://cafe.cpolar.top/wkdaily/zero3/raw/branch/main/zero3/imm.sh && chmod +x imm.sh && ./imm.sh
### **安装网络向导和首页(ARM64 & x86-64通用)
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

### **国内推荐的加密DNS服务**
以下是**国内**和**国外**的加密DNS（DNS-over-HTTPS，简称DoH，或DNS-over-TLS，简称DoT）分类列表，并标注了注释。

---

### **国内加密DNS**
```plaintext
# 阿里DNS（AliDNS）
- DoH: https://dns.alidns.com/dns-query
- DoT: dns.alidns.com

# 腾讯DNS（DNSPod）
- DoH: https://doh.pub/dns-query
- DoT: dot.pub

# 114DNS
- DoH: https://dns.114dns.com/dns-query
- DoT: dns.114dns.com

# CNNIC DNS
- DoH: https://dns.cnnic.cn/dns-query
- DoT: dns.cnnic.cn
```

---

### **国外加密DNS**
```plaintext
# Cloudflare DNS
- DoH: https://cloudflare-dns.com/dns-query
- DoT: one.one.one.one

# Google Public DNS
- DoH: https://dns.google/dns-query
- DoT: dns.google

# Quad9 DNS
- DoH: https://dns.quad9.net/dns-query
- DoT: dns.quad9.net

# AdGuard DNS
- DoH: https://dns.adguard.com/dns-query
- DoT: dns.adguard.com

# OpenDNS
- DoH: https://doh.opendns.com/dns-query
- DoT: dot.opendns.com
```

---

### **使用说明**
1. **国内DNS**：适合访问国内网站，速度快，推荐阿里DNS、腾讯DNS、114DNS。
2. **国外DNS**：适合访问国际网站，隐私保护强，推荐Cloudflare DNS、Google DNS。
3. **失效DNS**：不建议使用。
4. **Windows**：在“网络设置”中配置DoH或DoT。
5. **路由器**：在路由器管理界面中配置DoT。
6. **手机**：在“私人DNS”设置中配置DoT。

---

国内

百万ADH广告拦截过滤规则

     https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/all.txt

DNS 拦截

     https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt
     https://mirror.ghproxy.com/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt

### **国内广告拦截规则**
#### **基础规则**
- **CJX's Annoyance List**：针对国内的广告和弹窗。
  ```
  https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
  ```

- **Anti-AD**：国内专用的广告拦截规则，覆盖广泛。
  ```
  https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/master/anti-ad-easylist.txt
  ```

#### **增强规则**
- **AdGuard Chinese Filter**：AdGuard官方的中文过滤规则。
  ```
  https://filters.adtidy.org/extension/chromium/filters/224.txt
  ```
- **EasyList China**：针对中国地区的广告拦截规则。
  ```
  https://easylist-downloads.adblockplus.org/easylistchina.txt
  ```
- **百万ADH广告拦截过滤规则
  ```
  https://raw.githubusercontent.com/BlueSkyXN/AdGuardHomeRules/master/all.txt

- **DNS 拦截
  ```
  https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt
  https://mirror.ghproxy.com/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt
  
---

### **国外广告拦截规则**
#### **基础规则**
- **EasyList**：最常用的广告拦截规则，覆盖大多数广告。
  ```
  https://easylist.to/easylist/easylist.txt
  ```

- **EasyPrivacy**：专注于隐私保护，屏蔽跟踪器。
  ```
  https://easylist.to/easylist/easyprivacy.txt
  ```

#### **增强规则**
- **Fanboy's Annoyance List**：屏蔽弹窗、社交媒体按钮等。
  ```
  https://easylist.to/easylist/fanboy-annoyance.txt
  ```

- **AdGuard Base Filter**：AdGuard官方的基础过滤规则。
  ```
  https://filters.adtidy.org/extension/chromium/filters/2.txt
  ```

#### **隐私保护规则**
- **Peter Lowe's Ad and Tracking Server List**：屏蔽广告和跟踪服务器。
  ```
  https://pgl.yoyo.org/adservers/serverlist.php?hostformat=adblockplus&showintro=0&mimetype=plaintext
  ```

#### **恶意网站拦截**
- **Malware Domain List**：屏蔽恶意软件和钓鱼网站。
  ```
  https://mirror1.malwaredomains.com/files/justdomains
  ```

---

### **1. 常用视频广告拦截规则**
#### **YouTube广告拦截**
- **AdGuard YouTube Filter**：
  ```
  https://filters.adtidy.org/extension/chromium/filters/17.txt
  ```
  - 特点：AdGuard官方的YouTube广告拦截规则。

- **uBlock Filters – Annoyances**：
  ```
  https://raw.githubusercontent.com/uBlockOrigin/uAssets/master/filters/annoyances.txt
  ```
  - 特点：屏蔽YouTube广告和其他烦人内容。

- **YouTube AdBlock List**：
  ```
  https://raw.githubusercontent.com/AdguardTeam/FiltersRegistry/master/filters/filter_17_YoutubeAds/filter.txt
  ```
  - 特点：专注于屏蔽YouTube广告。

- **Fanboy's Annoyance List**：
  ```
  https://easylist.to/easylist/fanboy-annoyance.txt
  ```
  - 特点：屏蔽国际视频网站（如YouTube、Twitch）的广告。

- **AdGuard Base Filter**：
  ```
  https://filters.adtidy.org/extension/chromium/filters/2.txt
  ```
  - 特点：AdGuard官方的基础过滤规则，覆盖视频广告。

---

#### **国内视频广告拦截**
- **CJX's Annoyance List**：
  ```
  https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
  ```
  - 特点：针对国内视频网站（如优酷、爱奇艺）的广告拦截。

- **Anti-AD**：
  ```
  https://raw.githubusercontent.com/privacy-protection-tools/anti-AD/master/anti-ad-easylist.txt
  ```
  - 特点：国内专用的广告拦截规则，覆盖视频广告。

