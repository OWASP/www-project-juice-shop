---
title: Supporters
layout:  null
tab: true
order: 8
tags: juiceshop
---

## Project Supporters

> You can attribute your donation to the OWASP Juice Shop project by
> using
> [this link](/donate?reponame=www-project-juice-shop&title=OWASP+Juice+Shop)<!-- @IGNORE PREVIOUS: link -->
> or the green "Donate"-button while on any tab of the Juice Shop
> project page!

### Top Supporters

[![Denim Group](assets/images/300px-Denim-group_trans.png)](http://www.denimgroup.com/)
[![New Work SE](assets/images/NewWork_SE_Logo_RGB_Pos.png)](https://www.new-work.se/en/about-new-work-se)

#### All Corporate Supporters

* [Denim Group](http://www.denimgroup.com/)<sup>(2018-2019)</sup> <!-- >=1000€ @ 26.08.2018 & 20.09.2019 -->
* [secuvera](https://www.secuvera.de/)<sup>(2018-2019)</sup>
* [New Work SE](https://www.new-work.se/en/about-new-work-se)<sup>(2019)</sup> <!-- >=1000€ @ 19.12.2019 -->
* [PlexTrac](https://plextrac.com)<sup>(2019)</sup>
* [Silpion](https://silpion.de)<sup>(2019)</sup>
* [iteratec](https://www.iteratec.de/)<sup>(2017)</sup> <!-- >=1000€ @ 30.11.2017 -->
* [eSailors](https://www.esailors.de/)<sup>(2016)</sup> <!-- >=1000€ @ 31.07.2017 -->
* [XING](https://corporate.xing.com/en/about-xing/security/)<sup>(2016)</sup> <!-- >=1000€ @ 26.09.2016 -->

#### All Individual Supporters

{% assign individual_supporter = site.data.ow_attributions | uniq %}
{% for supporter in individual_supporter %}
* {{ supporter | strip_html | strip_newlines | strip }}
{% endfor %}
* _You want to appear on this list?_
  [Donate to OWASP here! 🤲](/donate?reponame=www-project-juice-shop&title=OWASP+Juice+Shop)<!-- @IGNORE PREVIOUS: link -->

#### All Corporate-sponsored Code Contributions

* [#1221](https://github.com/bkimminich/juice-shop/pull/1221),[#1356](https://github.com/bkimminich/juice-shop/pull/1356): [Panasonic Information Systems Company Europe](https://application.job.panasonic.eu/data/ruP0pHQvHrGZJKvL/rc.php?nav=jobsearch&custval12=ite&lang=EN&custval11=PBSEU_GER)<sup>(2019-2020)</sup>

<small><small>_In order to be recognized as a corporate code sponsor an
offical written confirmation of waiving all IP to the contributed code
is required._</small></small>

#### LeanPub Royalties

[![Pwning OWASP Juice Shop](https://raw.githubusercontent.com/bkimminich/pwning-juice-shop/master/cover_small.jpg)](https://leanpub.com/juice-shop)

$1,251.68 of royalties from [Björn Kimminich](https://kimminich.de)'s
eBook have been donated to the project between 09/2017 and 07/2019.

<!--
### Current Project Balance

You can find the current project balance along with a history of all
donations and spendings in the
[Chapter and Project Transactions](https://docs.google.com/spreadsheets/d/14UWhT7SbJAmNBES1ZYdRk8N5f8S2jVkbQbLZz26eM0I/edit#gid=1346179950&range=C323)
spreadsheet.
-->

---

_The OWASP Foundation is very grateful for the support by the
individuals and organizations listed. However please note, the OWASP
Foundation is strictly vendor neutral and does not endorse any of its
supporters._
