# Homework For ICT4HM003-3001

* [h1](#h1)
* [h2](#h2)
* [h3](#h3)
* [h4](#h4)
* [h5](#h5)
* [h6](#h6)
* [h7](#h7)

## h1 

There was a requirement to return homework as a website link.
So I installed Visul Studio Code and Git on to my Windows machine.
Might as well have used the Ubuntu in VirtualBox but this is more exiting. Isn't it?
I haven't really used Windows for coding, that is, at least not with Git.

### a

_Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability, impact and risk_

I tried not to write about Zoom, which has been so much in the news due to their 
questionable security features. Instead I found about a security flaw in [Zyxel routers](https://krebsonsecurity.com/2020/03/zxyel-flaw-powers-new-mirai-iot-botnet-strain/).

There was (and without an install of a security patch still is) a security flaw that allowed attacers to access Zyxel routers and VPN firewall products.

The same vulnerability was also found to be in use in a new variant of [Mirai](https://en.wikipedia.org/wiki/Mirai_(malware)) dubbed Mukashi.

Mukashi was targeting Zyxel VPN firewalls and NAS's, by scanning Internet to find suitable targets.

Vulnerability was in a program named `weblogin.cgi` that is in use in some [Zyxel's NAS and firewall products](https://www.zyxel.com/support/remote-code-execution-vulnerability-of-NAS-products.shtml)

There are 27 models listed with available patch on Zyxels web site, but also 10 models listed as vulnerable, but without an availble fix. There was no estimate on the number of affected devices, but [according to Zyxel](https://www.zyxel.com/fi/fi/about_zyxel/company_overview.shtml) there are 100 million devices around the world in total.

The vulnerability allowed for remote code execution. It is a bit unclear if the exploit required
the affected device to have factory default or commonly-picked passwords. 

### b

_Use either (Hutchins et al 2011) cyber kill chain or MITRE ATT&CK framework for analyzing the incident you used in a. You can pick any incident you want, but try to pick a source that gives you enough technical and business detail to do some analysis. (If you're in a hurry, cyber kill chain is much simpler. If you're technically skillful, you might find ATT&CK be very interesting)_

I think I'm technically skillful, but I _am_ in a hurry, so let's analyze Zyxel's problem through
Cyber Kill Chain.

**Reconnaissance:** The Mukashi malware actively scans the Internet to find vulnerable devices.

**Weaponization:** The Mukashi malware itself, maybe?

**Delivery:** Injected through login username field [Mukashi, the new Mirai variant that targets Zyxel NAS](https://securityaffairs.co/wordpress/100116/cyber-crime/mukashi-mirai-variant-targets-zyxel.html)

**Exploitation:** The `weblogin.cgi` didn't properly sanitize user input. Through this was possible to gain access to system. NAS devices also include a `setuid` utility that can be used to run any command with root privileges.

**Installation:** Injected command would download more malware code to system.

**Command & Control (C2):** Infected systems would report fo a control server.

**Actions On Objectives:** Downloading more malware. Possibly launching distributed denial of service (DDoS) attacs.

Well, that wasn't simpler at all. Maybe I'm not as technically skilled as I thought I was. The weaponization part was a bit difficult. Would it make sense to have the chain parts in different order.

### c

_Use attack tree to analyze the security of some imaginary example target._

```text
Goal: Get an excellet grade from this course

1. Hack the database [P] (OR)
   1.1. Gain access to school grades system (OR)
    1.1.1. Gain access to logged in teachers computer [I]
    1.1.2. Steal Credentials [I]
    1.1.3. Buy Credentials [P]
      1.1.4.1. Get money [I]
    1.1.4. Hire a guy to hack the database [P]
      1.1.4.1. Get money [I]
      1.1.4.2. Contact someone who has the skills [I]
2. Bribe the teacher [I :)] (OR)
  2.1. Get money [I]
3. Work really hard [P] (OR)
  3.1. Spend one hour a day studying [P] (OR) (Countermeasure: Netflix)(Counter-countermeasure: Turn off TV)
  3.2. Spend at least on full workday studying [P] (OR) (Countermeasure: Pastime activities)(Counter-countermeasure: Corona lockdown)

P = Possible
I = Impossible
```

It seems that I'll be studying really hard. ([Hacking databases is hard too](http://nedroid.com/2012/05/honk-the-databus/)).

### d

_MITTRE ATT&CK is about tactics, techniques and procedures. Give example of each from the framework._

**Tactics:** Mobile - Initial Access. Attack vector for gaining access to a mobile device.

**Techniques:** There were nine techniques listed for Mobile - Initial Access, and _Lockscreen Bypass_ was one of them. Code guessing, biometric spoofing or other vulnerabilities. 

### e

_Accept course rules in Moodle, so that we can talk about practical exploits._

Done and done.

### f

_Voluntary bonus: What do you consider the fundamentals of security? What are the theoretical foundations you would teach on the first day?_

I don't know if there is any theory behind this, but: be informed, read the news, be consevative when adopting new technology, test your backups.

Maybe the [Krebs’s 3 Basic Rules for Online Safety](https://krebsonsecurity.com/2011/05/krebss-3-basic-rules-for-online-safety/).

## h2

TODO

## h3

TODO

## h4

TODO

## h5

TODO

## h6

TODO

## h7

TODO
