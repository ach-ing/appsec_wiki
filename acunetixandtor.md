Modify /etc/tor/torrc:
`MaxCircuitDirtiness 10 # change tor chain every 10 seconds`

Web based Acunetix can proxy only through HTTP so we need HTTP-proxy

`apt-get install polipo`

and add this to polipo config (/etc/polipo/config):

allowedClients = 10.221.0.2

socksParentProxy = "localhost:9050"
socksProxyType = socks5

proxyAddress = "10.221.0.202"    # IPv4 only




systemctl start polipo
