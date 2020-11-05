Редактировать файл /etc/tor/torrc следующим образом:
  MaxCircuitDirtiness 10 # change tor chain every 10 seconds

вебочный Acunetix может проксировать только через HTTP так что нужно поднять HTTP-proxy


apt-get install polipo

and add this to polipo config (/etc/polipo/config):

allowedClients = 10.221.0.2

socksParentProxy = "localhost:9050"
socksProxyType = socks5

proxyAddress = "10.221.0.202"    # IPv4 only




systemctl start polipo
