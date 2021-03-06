# mos-chinadns

* 支持DoH，IPv6，EDNS Client Subnet(ECS)，按域名分流
* 可一步实现传统方案 `ChinaDNS(IP分流) + dnsmasq-china-list + dnsmasq(域名分流) + dnscrypt(DoH)`的效果
* 分流更准：
  * 同时考虑IP和域名
  * 国内域名国内服务器解析，确保低延时
  * 国际域名国外服务器解析，确保无污染
* 性能更高：
  * DoH性能可能是dnscrypt的10倍
  * 域名分流性能可能是dnsmasq的千倍
  * 显著降低低运算力设备(如路由)的负载与延时
* 多平台，配置简单，开箱即用

更多功能、使用教程以及手册，详见：[wiki](https://github.com/IrineSistiana/mos-chinadns/wiki)。

---

## Open Source Components / Libraries / Reference

部分设计参考

* [ChinaDNS](https://github.com/shadowsocks/ChinaDNS): [GPLv3](https://github.com/shadowsocks/ChinaDNS/blob/master/COPYING)

依赖

* [sirupsen/logrus](https://github.com/sirupsen/logrus): [MIT](https://github.com/sirupsen/logrus/blob/master/LICENSE)
* [miekg/dns](https://github.com/miekg/dns): [LICENSE](https://github.com/miekg/dns/blob/master/LICENSE)
* [valyala/fasthttp](https://github.com/valyala/fasthttp):[MIT](https://github.com/valyala/fasthttp/blob/master/LICENSE)

资源

* 大陆域名表`chn_domain.list`数据来自: [dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list): [LICENSE](https://github.com/felixonmars/dnsmasq-china-list/blob/master/LICENSE)
* 大陆IP表`chn.list`数据来自: [APNIC](https://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest)
