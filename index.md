# Homework For ICT4HM003-3001

There was a requirement to return homework as a website link.
So I installed Visul Studio Code and Git on to my Windows machine.
Might as well have used the Ubuntu in VirtualBox but this is more exiting. Isn't it?
I haven't really used Windows for coding, that is at least not with Git.

## h1 

### a

_Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability, impact and risk_

I tried not to write about Zoom, which has been so much in the news due to their 
questionable security features. Instead I found about a security flaw in [Zyxel routers](https://krebsonsecurity.com/2020/03/zxyel-flaw-powers-new-mirai-iot-botnet-strain/).

There was (and without an install of a security patch still is) a security flaw that allowed attacers to access Zyxel routers and VPN firewall products.

The same vulnerability was also found to be in use in a new variant of [Mirai](https://en.wikipedia.org/wiki/Mirai_(malware)) dubbed Mukashi.

Mukashi was targeting Zyxel VPN firewalls and NAS's, by scanning Internet to find suitable targets.

Vulnerability was in a program named `weblogin.cgi` that is in use in some [Zyxel's NAS and firewall products](https://www.zyxel.com/support/remote-code-execution-vulnerability-of-NAS-products.shtml)

There are 27 models listed with available patch on Zyxels web site, but also 10 models listed as vulnerable, but without an availble fix. There was no estimate on the number of affected devices, but [according to Zyxel](https://www.zyxel.com/fi/fi/about_zyxel/company_overview.shtml) there are 100 million devices around the world in total.

The vulnerability allowed for remote code execution. 

### b

_Use either (Hutchins et al 2011) cyber kill chain or MITRE ATT&CK framework for analyzing the incident you used in a. You can pick any incident you want, but try to pick a source that gives you enough technical and business detail to do some analysis. (If you're in a hurry, cyber kill chain is much simpler. If you're technically skillful, you might find ATT&CK be very interesting)_

### c

_Use attack tree to analyze the security of some imaginary example target._

### d

_MITTRE ATT&CK is about tactics, techniques and procedures. Give example of each from the framework._


### e

_Accept course rules in Moodle, so that we can talk about practical exploits._



### f

_Voluntary bonus: What do you consider the fundamentals of security? What are the theoretical foundations you would teach on the first day?_
