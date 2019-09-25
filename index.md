---

layout: col-sidebar
title: OWASP Juice Shop
tags: example-tag
level: 4

---

> [The most trustworthy online shop out there.](https://twitter.com/dschadow/status/706781693504589824)
> ([@dschadow](https://github.com/dschadow)) —
> [The best juice shop on the whole internet!](https://twitter.com/shehackspurple/status/907335357775085568)
> ([@shehackspurple](https://twitter.com/shehackspurple)) —
> [Actually the most bug-free vulnerable application in existence!](https://youtu.be/TXAztSpYpvE?t=26m35s)
> ([@vanderaj](https://twitter.com/vanderaj)) —
> [First you 😂😂then you 😢](https://twitter.com/kramse/status/1073168529405472768)
> ([@kramse](https://twitter.com/kramse))

OWASP Juice Shop is probably the most modern and sophisticated insecure
web application! It can be used in security trainings, awareness demos,
CTFs and as a guinea pig for security tools! Juice Shop encompasses
vulnerabilities from the entire
[OWASP Top Ten](https://www.owasp.org/index.php/OWASP_Top_Ten) along
with many other security flaws found in real-world applications!

![Juice Shop logo](https://raw.githubusercontent.com/bkimminich/juice-shop/develop/frontend/src/assets/public/images/JuiceShop_Logo_100px.png)

## Description

Juice Shop is written in Node.js, Express and Angular. It was the first application written entirely in JavaScript listed in the [OWASP VWA Directory](https://www.owasp.org/index.php/OWASP_Vulnerable_Web_Applications_Directory_Project).

The application contains a vast number of hacking challenges of varying difficulty where the user is supposed to exploit the underlying vulnerabilities. The hacking progress is tracked on a score board. Finding this score board is actually one of the (easy) challenges!

Apart from the hacker and awareness training use case, pentesting proxies or security scanners can use Juice Shop as a "guinea pig"-application to check how well their tools cope with JavaScript-heavy application frontends and REST APIs.

_Translating "dump" or "useless outfit" into German yields "Saftladen" which can be reverse-translated word by word into "juice shop". Hence the project name. That the initials "JS" match with those of "JavaScript" was purely coincidental!_

## Main Selling Points

* **Free and Open source**: Licensed under the [MIT license](https://github.com/bkimminich/juice-shop/blob/master/LICENSE) with no hidden costs or caveats
* [**Easy-to-install**](https://github.com/bkimminich/juice-shop#setup): Choose between [node.js](http://nodejs.org), [Docker](https://www.docker.com) and [Vagrant](https://www.vagrantup.com/downloads.html) to run on Windows/Mac/Linux
* **Self-contained**: Additional dependencies are pre-packaged or will be resolved and downloaded automatically
* **Self-healing**: The simple SQLite and MarsDB databases are wiped and repopulated from scratch on every server startup
* **Gamification**: The application notifies you on solved challenges and keeps track of successfully exploited vulnerabilities on a Score Board
* **Re-branding**: Fully customizable in business context and look & feel to your own corporate or customer requirements
* **CTF-support**: Challenge notifications optionally contain a flag code for your own [Capture-The-Flag events](https://github.com/bkimminich/juice-shop-ctf)

## Application Architecture

![Architecture diagram](https://raw.githubusercontent.com/bkimminich/pwning-juice-shop/master/introduction/img/architecture-diagram.png)

## Licensing

This program is free software: You can redistribute it and/or modify it under the terms of the [MIT License](https://github.com/bkimminich/juice-shop/blob/master/LICENSE). OWASP Juice Shop and any contributions are Copyright © by Bjoern Kimminich 2014-2019.