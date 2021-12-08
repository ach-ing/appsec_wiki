## WAF


### Identify WAF
- [Identifying WAF and some bypass techniques by DSEC](https://habr.com/ru/company/dsec/blog/454592/)
### Bypass WAF by DNS Tool
- [bypass-firewalls-by-DNS-history TOOL](https://github.com/vincentcox/bypass-firewalls-by-DNS-history)
```console
root@root:~$ bash bypass-firewalls-by-DNS-history.sh -d domain.com -a
```
- [viewdns.info/iphistory](https://viewdns.info/iphistory/)
#### Cloudflare
- [CloudFail(crimeflare, ipinfo.io)](https://github.com/m0rtem/CloudFail) 
- [CloudFlair](https://github.com/christophetd/CloudFlair)
- [crimeflare](http://www.crimeflare.org:82/cfs.html)
- [cloudip.sh](https://github.com/Top-Hat-Sec/thsosrtl/blob/master/CloudIP/cloudip.sh)

#### HTTP headers
- https://gist.github.com/ach-ing/ea4206702ca3b98c07154e8dae73c158
```
CF-Connecting_IP: 127.0.0.1
Client-IP: 127.0.0.1
Referer: https://127.0.0.1
True-Client-IP: 127.0.0.1
X-Client-IP: 127.0.0.1
X-Forwarded-For: 127.0.0.1
X-Originating-IP: 127.0.0.1
X-Real-IP: 127.0.0.1
X-Remote-Addr: 127.0.0.1
X-Remote-IP: 127.0.0.1
```
