[general]
excluded_routes=192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, 17.0.0.0/8
network_check_url=http://cp.cloudflare.com/generate_204
server_check_url=http://www.qualcomm.cn/generate_204
geo_location_checker=http://ip-api.com/json/?lang=zh-CN, https://github.com/KOP-XIAO/QuantumultX/raw/master/Scripts/IP_API.js
resource_parser_url=https://raw.githubusercontent.com/zwf234/Scriptable/master/resource-parser.js
profile_img_url= https://gitee.com/glc66/vess/raw/master/tp/An.JPEG
dns_exclusion_list = *.cmpassport.com, *.jegotrip.com.cn, *.icitymobile.mobi, id6.me, *.icitymobile.mobi, *.pingan.com.cn, *.cmbchina.com, *.localnetwork.uop, mfs.ykimg.com*.ttf

[dns]
no-ipv6
server=119.29.29.29
server=223.5.5.5
server=1.2.4.8
server=/*.taobao.com/223.5.5.5
server=/*.tmall.com/223.5.5.5
server=/*.alipay.com/223.5.5.5
server=/*.alicdn.com/223.5.5.5
server=/*.aliyun.com/223.5.5.5
server=/*.jd.com/119.28.28.28
server=/*.qq.com/119.28.28.28
server=/*.tencent.com/119.28.28.28
server=/*.weixin.com/119.28.28.28
server=/*.bilibili.com/119.29.29.29
server=/hdslb.com/119.29.29.29
server=/*.163.com/119.29.29.29
server=/*.126.com/119.29.29.29
server=/*.126.net/119.29.29.29
server=/*.127.net/119.29.29.29
server=/*.netease.com/119.29.29.29
server=/*.mi.com/119.29.29.29
server=/*.xiaomi.com/119.29.29.29
address=/mtalk.google.com/108.177.125.188

[http_backend] 
https://raw.githubusercontent.com/chavyleung/scripts/master/box/chavy.boxjs.js, tag=BoxJs, path=^/, img-url=https://qxnav.com/rules/QuantumultX/img/box.png, enabled=false
#BoxJs改为使用http backend方式，访问地址改为http://127.0.0.1:9999，更新配置后请长按风车-更新，然后重启代理

[policy]
static=海外服务, 优选节点1, 优选节点2, 优选节点3,负载均衡,自选节点, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Global.png
#优选节点默认每一小时进行一次延迟检测，想更换检测时间的请修改check-interval参数。
url-latency-benchmark=优选节点1, resource-tag-regex=^(LULIN), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png
url-latency-benchmark=优选节点2, resource-tag-regex=^(LINLIN), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png
url-latency-benchmark=优选节点3, resource-tag-regex=^(五毛钱), server-tag-regex=^(?!.*网易云), check-interval=3600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Urltest.png
round-robin=负载均衡, resource-tag-regex=^(五毛钱), server-tag-regex=^(?!.*网易云), img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Roundrobin.png
static=自选节点, proxy, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Static.png
static=大陆服务, direct, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/China.png
static=网易云音乐, server-tag-regex=^(music|𝐌𝐮𝐬𝐢𝐜|Unbolck|网易|解锁), img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Netease.png
static=屏蔽广告, reject, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Adblock.png
static=AdBlock, direct, reject, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/Final.png
static=Mainland, direct, img-url=https://raw.githubusercontent.com/Orz-3/face/master/Bili.png
static=Outside, direct, 海外服务, img-url=https://raw.githubusercontent.com/Orz-3/face/master/YouTube.png
static=港台番剧, 优选节点3, 自选节点, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/StreamingSE.png
#url-latency-benchmark=香港, server-tag-regex=(?=.*(港|HK|(?i)Hong))^((?!(台|日|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/HK.png
#url-latency-benchmark=台湾, server-tag-regex=(?=.*(台|TW|(?i)Taiwan))^((?!(港|日|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/TW.png
#url-latency-benchmark=日本, server-tag-regex=(?=.*(日|JP|(?i)Japan))^((?!(港|台|韩|新|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/JP.png
#url-latency-benchmark=新加坡, server-tag-regex=(?=.*(新|狮|獅|SG|(?i)Singapore))^((?!(港|台|日|韩|美)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/SG.png
#url-latency-benchmark=美国, server-tag-regex=(?=.*(美|US|(?i)States|American))^((?!(港|台|日|韩|新)).)*$, check-interval=600, tolerance=0, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/US.png




[server_local]
http=120.232.251.206:29980, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=关注公众号：阿璟爱玩机
http=183.240.9.28:29980, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false,  tag=关注公众号@阿璟爱玩机
http=183.240.9.29:29980, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联¹关注公众号@阿璟爱玩机
http=183.240.9.30:29980, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联²关注公众号@阿璟爱玩机
http=183.240.9.31:29980, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false,  tag=永不失联³关注公众号@阿璟爱玩机
http=120.232.251.206:29979, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⁴关注公众号@阿璟爱玩机
http=183.240.9.28:29979, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⁵关注公众号@阿璟爱玩机
http=183.240.9.28:29982, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⁷关注公众号@阿璟爱玩机
http=183.240.9.28:29983, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⁸关注公众号@阿璟爱玩机
http=183.240.9.28:29984, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false,  tag=永不失联⁹关注公众号@阿璟爱玩机
http=183.240.9.28:29987, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⁺关注公众号@阿璟爱玩机
http=183.240.9.28:29988, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₀关注公众号@阿璟爱玩机
http=183.240.9.29:29979, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₁关注公众号@阿璟爱玩机
http=183.240.9.29:29982, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₂关注公众号@阿璟爱玩机
http=183.240.9.29:29983, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₃关注公众号@阿璟爱玩机
http=183.240.9.29:29984, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₄关注公众号@阿璟爱玩机
http=183.240.9.29:29987, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₅关注公众号@阿璟爱玩机
http=183.240.9.29:29988, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₆关注公众号@阿璟爱玩机
http=183.240.9.30:29979, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₇关注公众号@阿璟爱玩机
http=183.240.9.30:29982, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₈关注公众号@阿璟爱玩机
http=183.240.9.30:29983, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联₉关注公众号@阿璟爱玩机
http=183.240.9.30:29984, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联ₒ关注公众号@阿璟爱玩机
http=183.240.9.30:29987, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联①关注公众号@阿璟爱玩机
http=183.240.9.30:29988, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联②关注公众号@阿璟爱玩机
http=183.240.9.31:29979, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联③关注公众号@阿璟爱玩机
http=183.240.9.31:29982, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联④关注公众号@阿璟爱玩机
http=183.240.9.31:29983, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⑤关注公众号@阿璟爱玩机
http=183.240.9.31:29984, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⑥关注公众号@阿璟爱玩机
http=183.240.9.31:29987, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⑦关注公众号@阿璟爱玩机
http=183.240.9.31:29988, username=442993652168396800, password=2ef91648-089f-4c81-b34d-06f072ec51dd, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联⑧关注公众号@阿璟爱玩机


vmess=103.176.113.132:80, method=chacha20-ietf-poly1305, password=9aa75b1a-a84d-451e-8d45-613de362b60f, obfs=ws, obfs-host=viettel.akamaized.net, obfs-uri=/kvw0870h/, fast-open=true, udp-relay=true, aead=true, tag=永不失联⑨关注公众号@阿璟爱玩机
vmess=103.177.146.77:80, method=chacha20-ietf-poly1305, password=9aa75b1a-a84d-451e-8d45-613de362b60f, obfs=ws, obfs-host=viettel.akamaized.net, obfs-uri=/zingfast/, fast-open=true, udp-relay=true, aead=true, tag=永不失联⑩关注公众号@阿璟爱玩机
vmess=103.177.146.79:80, method=chacha20-ietf-poly1305, password=9aa75b1a-a84d-451e-8d45-613de362b60f, obfs=ws, obfs-host=viettel.akamaized.net, obfs-uri=/zingfast/, fast-open=true, udp-relay=true, aead=true, tag=永不失联①①关注公众号@阿璟爱玩机

shadowsocks=ieplszhk-sz.qqgg.work:56326, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①②关注公众号@阿璟爱玩机
shadowsocks=jx-002.yyuuii.cyou:10019, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①③关注公众号@阿璟爱玩机
shadowsocks=jx-002.yyuuii.cyou:12021, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①④关注公众号@阿璟爱玩机
shadowsocks=jx-002.yyuuii.cyou:10020, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①⑤关注公众号@阿璟爱玩机
shadowsocks=iepl-hn01.qqgg.work:48293, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①⑥关注公众号@阿璟爱玩机
shadowsocks=jx-002.yyuuii.cyou:10018, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①⑦关注公众号@阿璟爱玩机
shadowsocks=iepl-hn01.qqgg.work:20098, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①⑧关注公众号@阿璟爱玩机
shadowsocks=jx-002.yyuuii.cyou:10019, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联①⑨关注公众号@阿璟爱玩机
shadowsocks=iepl-hn01.qqgg.work:21637, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联②①关注公众号@阿璟爱玩机
shadowsocks=iepl-hn01.qqgg.work:46164, method=aes-256-cfb, password=hGkQ6915tD, ssr-protocol=auth_aes128_md5, ssr-protocol-param=32381:C2pHyiQfgm, obfs=tls1.2_ticket_auth, obfs-host=ajax.microsoft.com, fast-open=false, udp-relay=false, tag=永不失联②②关注公众号@阿璟爱玩机
trojan=www.zx07.top:443, password=L1qNeGrY58ApwrRA, over-tls=true, tls-verification=false, fast-open=false, udp-relay=false, tag=永不失联②③关注公众号@阿璟爱玩机


shadowsocks=154.9.204.15:60000,method=none, password=baredirectnana, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②④关注公众号@阿璟爱玩机
shadowsocks=154.3.5.248:60086,method=none, password=%$#meworkersthod, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②⑤关注公众号@阿璟爱玩机
shadowsocks=154.3.5.250:40086,method=none, password=protocIOS*12ola, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②⑥关注公众号@阿璟爱玩机
shadowsocks=154.9.204.30:50000,method=none, password=server_IJYTGFipv6, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②⑦关注公众号@阿璟爱玩机
shadowsocks=154.9.204.156:60000,method=none, password=networkseIIUTY@__tup, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②⑧关注公众号@阿璟爱玩机
shadowsocks=154.3.6.24:40088,method=none, password=serIOSTZrver@, ssr-protocol=auth_chain_a, obfs=plain, fast-open=false, udp-relay=false, tag=永不失联②⑨关注公众号@阿璟爱玩机

http=106.52.127.72:19951, fast-open=false, udp-relay=false, tag=🎧 解锁网易云音乐
# 本地服务器部分，自行添加即可

#请使用 Safari 浏览器访问网站。首先下载 证书 (https://qxnav.com/rules/QuantumultX/CA/wyy_ca.crt)，进入「设置」>「通用」>「描述文件」，安装「UnblockNeteaseMusic Root CA」，并在「设置」>「通用」>「关于本机」>「证书信任设置」开启对「UnblockNeteaseMusic Root CA」的信任。
#证书下载地址：https://qxnav.com/rules/QuantumultX/CA/wyy_ca.crt


[server_remote]
https://ssrr.xyz/api/v1/client/subscribe?token=b23de6c959073db6a611c31d13b1d765, tag=LULIN, img-url=https://gitee.com/glc66/vess/raw/master/tp/luc.png, update-interval=43200, opt-parser=true, enabled=true
https://anmuheipp.netlify.app/, tag=LINLIN, img-url=https://gitee.com/glc66/vess/raw/master/tp/lin.png, update-interval=43200, opt-parser=true, enabled=true
https://xsus.xyz/api/v1/client/subscribe?token=124146b1d16099e66e2c16bb3a669ef3, tag=五毛钱, img-url=https://gitee.com/glc66/vess/raw/master/tp/lin.png, update-interval=43200, opt-parser=true, enabled=true
#解锁网易云灰色音乐原订阅地址：https://git.io/JfNq3
https://qxnav.com/rules/QuantumultX/gz/wyy.list, tag=网易云解锁灰色, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Netease_Music.png, update-interval=86400, opt-parser=true, enabled=true
# 节点远程订阅，自行添加


[filter_remote]
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Filter/NeteaseMusic.list, tag=解锁网易云音乐, force-policy=网易云音乐, update-interval=-1, opt-parser=false, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Unbreak.list, tag=规则修正, force-policy=direct, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Advertising.list, tag=广告拦截, force-policy=reject, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/Surge/AdRule.list, tag=广告拦截, force-policy=reject, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Hijacking.list, tag=运营劫持, force-policy=reject, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Privacy.list, tag=隐私保护, force-policy=reject, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Video/TikTok.list, tag=海外抖音, force-policy=海外服务, update-interval=86400, opt-parser=true, enabled=true
#https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Region/HK.list, tag=流媒体HK, force-policy=香港, update-interval=86400, opt-parser=true, enabled=true
#https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Region/TW.list, tag=流媒体TW, force-policy=台湾, update-interval=86400, opt-parser=true, enabled=true
#https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Region/JP.list, tag=流媒体JP, force-policy=日本, update-interval=86400, opt-parser=true, enabled=true
#https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Region/US.list, tag=流媒体US, force-policy=美国, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Streaming.list, tag=国际媒体, force-policy=海外服务, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/StreamingSE.list, tag=港台番剧, force-policy=港台番剧, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Global.list, tag=全球加速, force-policy=海外服务, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Extra/Apple/Apple.list, tag=苹果服务, force-policy=苹果服务, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/China.list, tag=国内网站, force-policy=direct, update-interval=86400, opt-parser=true, enabled=true
https://raw.githubusercontent.com/17mon/china_ip_list/master/china_ip_list.txt#type=rule, tag=ChinaIPv4, force-policy=direct, update-interval=86400, opt-parser=true, enabled=true
https://gaoyifan.github.io/china-operator-ip/chinanet6.txt#type=rule, tag=ChinaIPv6, force-policy=direct, update-interval=86400, opt-parser=true, enabled=true
[filter_local]
# 本地分流规则(相同规则下，本地规则将覆盖远程规则，优先生效)
# 绕过企业证书过期
host, ocsp.apple.com, reject
#YouTube 去底部广告
host-suffix, ehg-youtube.hitbox.com, reject

# 屏蔽系统更新
host, ns.itunes.apple.com,屏蔽广告
host, appldnld.apple.com,屏蔽广告
host, mesu.apple.com,屏蔽广告
host, xp.apple.com,屏蔽广告
host, gdmf.apple.com,屏蔽广告

# 避免迅雷版权问题
host, hub5idx.v6.shub.sandai.net,reject
host, hub5emu.v6.shub.sandai.net,reject
host, hub5btmain.v6.shub.sandai.net,reject

# 其他
host-suffix, local, direct
host-keyword, merlinblog, proxy
ip-cidr, 10.0.0.0/8, direct
ip-cidr, 17.0.0.0/8, direct
ip-cidr, 100.64.0.0/10, direct
ip-cidr, 127.0.0.0/8, direct
ip-cidr, 172.16.0.0/12, direct
ip-cidr, 192.168.0.0/16, direct
geoip, cn, 大陆服务
final, 大陆服务

[rewrite_remote]
# rewrite 复写远程订阅
#>>>>>>>>>>>解锁会员
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Rewrite/UnlockApp.conf, tag=墨鱼专属VIP[请自行添加hostname]@ddgksf2013
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/UnlockVip/Spotify.conf, tag=Spotify破解VIP@app2smile
https://subweb.s3.fr-par.scw.cloud/Module/embyUnlocked.conf, tag=emby解锁会员权限
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/UnlockVip/Rrtv.conf, tag=人人视频VIP@ddgksf2013
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/AdBlock/Bilibili.conf, tag=B站去广告+1080P高码率@ddgksf2013
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/UnlockVip/Kuwo.conf, tag=酷我音乐VIP@ddgksf2013



#>>>>>>>>>>>软件增强
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Rewrite/UnlockVip/BaiduCloud.conf, tag=百度网盘倍速@ddgksf2013
https://raw.githubusercontent.com/zZPiglet/Task/master/UnblockURLinWeChat.conf, tag=微信解锁被屏蔽的URL@zZPiglet
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/Function/BilibiliAutoRegion.conf, tag=Bilibili换区脚本@NobyDa
https://raw.githubusercontent.com/Orz-3/QuantumultX/master/JD_TB_price.conf, tag=比价脚本@Orz-3
https://raw.githubusercontent.com/Orz-3/QuantumultX/master/TikTok.conf, tag=Tiktok解锁@Orz-3
https://raw.githubusercontent.com/Orz-3/QuantumultX/master/Netflix_ratings.conf, tag=Netflix评分@Orz-3
;https://github.com/VirgilClyne/iRingo/raw/main/qxrewrite/Siri.qxrewrite, tag=Siri与搜索2.0@VirgilClyne
;https://raw.githubusercontent.com/id77/QuantumultX/master/rewrite/Youtube_CC.conf#out=Hant, tag=油管字幕翻译@id77


#>>>>>>>>>>>应用去广告
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Rewrite/AdBlock/StartUp.conf, tag=应用去开屏广告@ddgksf2013
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/script/zhihu/zhihu_plus.qxrewrite, tag=知乎去广告及体验增强@blackmatrix7
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/script/smzdm/smzdm_remove_ads.qxrewrite, tag=什么值得买去广告@blackmatrix7
https://github.com/app2smile/rules/raw/master/module/tieba-qx.conf, tag=百度贴吧超级去广告@app2smile
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Applet/QuanX.conf, tag=微信小程序去广告@ddgksf2013
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/AdBlock/YoutubeAds.conf, tag=油管去广告@DivineEngine
https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/AdBlock/Weibo.conf, tag=微博去广告@zmqcherish


#>>>>>>>>>>>通用去广告
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Quantumult/Rewrite/Block/AdvertisingPlus.conf, tag=去广告脚本@DivineEngine
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Quantumult/Rewrite/Block/Advertising.conf, tag=去广告重写@DivineEngine
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/Rewrite_lhie1.conf, tag=去广告重写@lhie1
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Quantumult/Rewrite/General.conf, tag=神机重定向@DivineEngine


#>>>>>>>>>>>网页优化
https://github.com/ddgksf2013/Cuttlefish/raw/master/Html/WebAdBlock.conf, tag=影视网站去广告@ddgksf2013
https://raw.githubusercontent.com/ddgksf2013/Cuttlefish/master/Rewrite/Function/Q-Search.conf, tag=Safari超级搜索@ddgksf2013
;https://github.com/ddgksf2013/Cuttlefish/raw/master/Rewrite/Function/EndlessGoogle.conf, tag=Google自动翻页@langkhach

https://gitee.com/glc66/Quantumult-X/raw/master/quantumult%20X/getCookie.md, tag=获取Cookie（获取完就禁用）, update-interval=86400, opt-parser=false, enabled=false
https://gitee.com/chavyleung/scripts/raw/master/box/rewrite/boxjs.rewrite.quanx.tf.conf, tag=BoxJs tf版, update-interval=86400, opt-parser=false, enabled=false
https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.conf, tag=BoxJS 商店版, update-interval=86400, opt-parser=false, enabled=true


[rewrite_local]
#本地复写规则


#Task远程订阅  https://raw.githubusercontent.com/zwf234/rules/master/qixin.json
#添加方法：打开构造请求，最上方第一个按钮，右上角+号添加即可
[task_local]
10 12,18 * * * https://raw.githubusercontent.com/id77/QuantumultX/master/task/jdWuLiu.js, tag=京东物流派件提醒, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true
2 9 * * * https://qxnav.com/rules/QuantumultX/js/jd_bean_change.js, tag=京豆变动通知, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true
55 23 * * * https://qxnav.com/rules/QuantumultX/js/zwf234/jd_unsubscribe.js, tag=取关京东店铺商品, img-url=https://qxnav.com/rules/QuantumultX/img/jd.png, enabled=true
0 8-22/3 * * * https://raw.githubusercontent.com/Peng-YM/QuanX/master/Tasks/nCov.js, tag=疫情动态, img-url=https://qxnav.com/rules/QuantumultX/img/COVID-19.png, enabled=true
0 8 * * * https://raw.githubusercontent.com/NobyDa/Script/master/JD-DailyBonus/JD_DailyBonus.js, tag=京东签到, img-url=https://raw.githubusercontent.com/NobyDa/mini/master/Color/jd.png, enabled=true
0 2 * * * https://raw.githubusercontent.com/toulanboy/scripts/master/weibo/weibotalk.js, tag=微博超话

[mitm]
# 以下为证书&主机名部分
hostname = -*snssdk.com, -*amemv.com, bean.m.jd.com, *.example.com, *.sample.com
passphrase = 6EE87080
p12 = MIIKsQIBAzCCCnsGCSqGSIb3DQEHAaCCCmwEggpoMIIKZDCCBL8GCSqGSIb3DQEHBqCCBLAwggSsAgEAMIIEpQYJKoZIhvcNAQcBMBwGCiqGSIb3DQEMAQYwDgQIggxuPEeMwWsCAggAgIIEeCSlNyCmVHFvbNRWHUY0GGqyxxoIxBbTWWzvyD6rYk2pjbQbe47CHfK+Mw3bWOKY7lmisLcCjrLkuunDC6oBtroJTMI1Jvc1blQAWe02ppaTRzFGNolCV3Sb2Wb9E4n2VjrRmp+Uy/PYEYfNxXeIlw8f3zg6vmGD05VEt68Og3TL6fY0VOuffGsoQIaOmJTEKMcx/mBs0SNhD3xMMlbK6hyHCtHwjPMaV1USgJso+u6GvT8OoBJsf/ugGp5+XWPQzHt2fGMFS02gzFY1gLgQOksXGsJnS39yVSvKiksrKfRrhs8jSEbpchFTaUQL7JoLu+F3054fEPEcaWMbRmqYzk4srvJuBD59i9IVLtGQPsMjn/cMMoslWDxJZ9nYLX7KYZNuuZdZRUtgbSxBa/FQasDMpSBXEedRfGAPEZvDJPsODeWtlhqHrGbqhqR1Iz4ypAhOIpsFBfXTSgM7Wmn/DO9PLhlreHSTMwk7LnRUS0tXM2ddViamrG19iVhmwx9GUa4oXlgXHt7e5ykdxxb8y6io4MGQ0tsKh/TjA5VdTDdZMUsJBMdqF0v5+HRFwcbFxWcT2c/w/qDcPdxnQ6D6gvN5rT6GEzRwDiQdYmgPSontZPVobi0/ru25z9fPfEL+XhpvZmudtCQ/NW2N7or17/kAUrI34h+SVl1iUP4Unb3EMPUFvH+FQP9f0JMzpYH68M01x5DC2hwpkB3vhVl6vJozRh6KbTyKfU7KGk6Z6Nd0+ZnEIhiVTOomYIxfyH4B0oqVdtRdjlitQmlQoUTRNGRrXDfASIlGpKPwis6OWlA8RHOw92pb6fRcnBo5j8IVacJPMXCgmImsEJJulXbIQtTctIeXy9GKK48Da17kfPOpDtqkm28lFZWMvjsgWeF9vQu8YAXDQiLeApNyHfLuTZQj+3G5nFN4aCwaLYBiILEDNcNMYCOwx0eSXlcyrJh9/EyDIScJK5PPk7wPypzgZy6FNAmNcwyWCAP5wYwGRahNFvu872YLOwqW1c0jXSpuMjx9U/TpGYXWeeL4cP+ycrPey8JtjdP+FmtATmU4+eOlQm10+TO/tdhfMGCtVrA8kSWhWNkalrqQV/rBvmMVhq1GHbcr3+83sea3TE5//G3XC9gYQ0XghAHhdMgGZcD+J+0f3qoZoT2lqIlWq5z9RaiWLEw+IUmH5iAjDGItk2Nqz5G8LyqyT5mkuAUkNuVlRS4yFpDw4l8ws0di3l1+KAilm4AZN1onbJT8iBXfOwm7F9EBmvDv9Jaq7IESG42EHmis2gYW1n2cEBVfPSfyUD6r+afaXf5tBFBoDeylw4P/f6/VL/ZxgIj50k2hnFHcPiXNSqbCsjjwfwwFlFfIHtrA3xPiSVsqWp3+92wNDEgaY7UGfZn3ficEH1G0gaug7ZGKJi9WZCXRhjS3NHa6grThP7ht/aoRGuee2QaM+U6fD20eNrkkhzFVYH2moPJA+YmeOSLi5YWV5MUD/kVcTsY2NjJRlpWIHeKFCjIJKeB6JF44iex+hLcwggWdBgkqhkiG9w0BBwGgggWOBIIFijCCBYYwggWCBgsqhkiG9w0BDAoBAqCCBO4wggTqMBwGCiqGSIb3DQEMAQMwDgQIMdg5ojjYxXUCAggABIIEyPaR9gINFi/Z7NA/6WNqtBAeE/x4NiqKt23Qjbrq8KSKsXOIlpJuq5PZod5V10LF0MG/Y7acBktHLGYgqaXqI9GB4mXE3LP4ZjqhmYtSlhTzvFyS6QLUVhGCW6vaPKTCxQdZuBy+K5sR6ll4YrhdJMXs3qLFgH9XnYqUsypVpTc7YwbU0lpI8MMLDBVIXUunQCjcx2nI5mzL4JG5oFp6UDAd+y3RTHB/USVWfLIaYQM2j247ynMkKxY/a5LZGuClGe5FDsbe7cBET7VJUiSrL70d3zEiw2BYzPR/gfGQfhFFvH9NKB5gvUr43YMH1DaYzsj0aC9hCM995hZO9A7nmBSRbhfHpfumZBmpatRd6Q2EodrLg/qKaJ6GpTuWMAAKyXd11qWyVgHMJaP3fnOwgwArfmSF0eKTl+T7aPyNIB4TVHIkq0nckLWLljWhQfDj+Fj0F1KkLCeHZvnJ2D/IAEZ3PqX9YliPmgYlwgd9J05Erj65kLIBDjG7d0VCZ+lWx/WZcl4ULc1A16fS6SFoShfkUMXVaIAlX66PFv4CtybwEnn3wBeqzUE9TNkde9PLlcAcR/9RBv0qRTtI0Y2ZMXPOLufjwNldaJ1T1WNuji39vGo6sJaQ/47hU3A2DdfZ2kmAzjXiLHMq4OXwAC2vjvnZxevTVkjmLH63awrb35jjuNoz4KUGOMVrRIQbN9xDfLVBAbzGkv4TnwFzQ4rFDyNEkrmdPuWfDCx6GvZ3zjubROI4WFCHqyJujd+dfrqv9nSiUSrAjGTaLNS7vc/56b3sWI0v75lCmFtUD44F2sp8MFXIDIzBkIgpERhKIiI2mhPn7MexMXA+61ie86s7b/WtLnV/Q0F0YBsNDGEWa7D5G9rXYrlq75W1LfxQ4Nb+0PgheU3FJrWSecQ1r2kVa5DM1EVM33IVp8P2AIdWSleB1Xu2a2s2XbsDbnqiUdtOtI26/1qmHQ1W01KcZwYK/8uVJGdCkrjakMAHKbcQ1IvSts2DblrY1fTrBQ7EQcEh2fxN7Qb23/gNwIJLXByvLNqCD6aSMJUPqWRmC/1ft9OFpmlYkCnTncteTe2d/1WQg4UiMMJXpok+zOfWFUHN203AyhnAM/V38S2Ve69QCSii8b2HICjdvmgRMwCDs0HciS0SH3UsMHmN5/dSLtcmFrxJ2c8hEjciJ8lybu3jkeLMAmfJJD+Xj1t2vfze2jz/OjcveIXTelFwFEB/wIDvhA+R1EZqn3UQdsnddmsLKAFJ2pLkmb29yE/v69LAJLZTUlJAVg4Ug42yp8x5UkiLNS+AseQ5WafkISL7Gsb+jQ7VGH1N+G2YyIr82afB9O4p+hccPVeGF+njvqPSqZvmO7QIQaHClCuYlmA2YUmvTfU3MzmPO6DFIX0kArZw4dzcuqViDdjnOoKJXkF9SQ1mqEUFUy5ytuE/97qk6mIGUYbp3TBEwRc7w2nf3Z1M3s34WXXIVCSFW8+IKHIWFNOMB9J7pWcSgUv9a7XQs+l0kPFTIg+61y+9HilJFpL0MwHbeZJDTY4/uhbK5w+8EezutxirdxT+SJBGZshxNDURMzYGEeguWVjCOgsRvlyFQqrvrJHHwTgl4K8TPIZFQLR1FuFN7GJsqvXYXDGBgDAjBgkqhkiG9w0BCRUxFgQUddFpZDiyl6kqVJrjnoPzAES5Ge0wWQYJKoZIhvcNAQkUMUweSgBRAHUAYQBuAHQAdQBtAHUAbAB0ACAAWAAgAEMAQQAgADYARQBFADgANwAwADgAMAAgACgAOQAgAE4AbwB2ACAAMgAwADIAMAApMC0wITAJBgUrDgMCGgUABBQ6GXjcpbU/+vRfIxHCAQVAETM/RgQI8AfaUxmWzuA=
