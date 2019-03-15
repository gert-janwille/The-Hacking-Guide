# The Hacking Cheat Sheet

## Table of Contents
* [Reconnaissance & Foot printing](#Reconnaissance-&-Foot-printing)
  * [WHOIS](#WHOIS)
  * [VHOSTS](#VHOSTS)

## Reconnaissance & Foot printing

### WHOIS
Useful for finding out technical domain information
- Owner name, email and address
- Nameservers
- Other websites on the same webserver
- Network block (often referred to with it’s AS number, such as AS34762)
- …

#### Whois servers
- Whois.geektools.com (whois-proxy)
- Whois.crsnic.net (with wildcards, limited to .com, .net, .org and .edu domains)
- Whois.networksolutions.com (with wildcards, limited to .com, .net, .org and .edu domains)).
- Whois.ripe.net (for all European queries)
- www.dns.be (for all Belgian queries)

#### Sites
- [http://whois.net/](http://whois.net/)  (very good starting point)
- [http://www.ip-adress.com/whois](http://www.ip-adress.com/whois) (for moving on to the IP address /  webserver)
- [http://www.network-tools.com](http://www.network-tools.com)
- [http://www.internic.net/whois.html](http://www.internic.net/whois.html)

#### Commands
```bash
whois -h whois.crsnic.net *aqtronix*
```
* Find all domains containing aqtronix and list their registrars (only for .com, .net & .edu domains)

```bash
whois -h whois.crsnic.net aqtronix.com
```
* Show registrar and owner details for domain aqtronix

```bash
whois -h whois.ripe.net 81.83.1.61
```
* Show owner information for the IP address

### VHOSTS
