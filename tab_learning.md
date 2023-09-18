---
title: Learning
layout:  null
altfooter: true
tab: true
order: 4
tags: juiceshop
---

## Hacking Instructor Tutorials

{% assign tutorials = site.data.challenges | where_exp: "item", "item.tutorial != null" | sort: "tutorial.order" %}

![Juicy Bot](https://raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuicyBot_MedicalMask.png)

Click on a link in the table below to launch a
[step-by-step tutorial](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_hacking_instructor)
for that particular challenge on our public
<https://demo.owasp-juice.shop> instance. If you are entirely new to the
Juice Shop, we recommend doing them in the listed order. With the
(optional)
[Tutorial Mode](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_tutorial_mode)
you can even enforce that the {{ tutorials.size }} tutorial challenges
have to be performed gradually in order to unlock the other {{
site.data.challenges.size | minus: tutorials.size }} challenges.

<table>
  <tr>
    <th>Challenge</th>
    <th>Category</th>
    <th>Difficulty</th>
  </tr>
  {% for tutorial in tutorials %}
  <tr>
    <td style="min-width: 190px"><a href="https://demo.owasp-juice.shop/#/hacking-instructor?challenge={{ tutorial.name }}" target="_blank">{{ tutorial.name }}</a></td>
    <td style="min-width: 190px">{{ tutorial.category }}</td>
    <td style="min-width: 100px">
    {% assign difficulty = tutorial.difficulty | to_integer %}
    {% for i in (1..difficulty) %}⭐{% endfor %}
    </td>
  </tr>
  {% endfor %}
  <tr>
    <td style="min-width: 190px"><a href="https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Coding%20Challenges" target="_blank">Coding Challenges</a></td>
    <td style="min-width: 190px">n/a</td>
    <td style="min-width: 100px">n/a</td>
  </tr>
</table>

## Coding Challenges

{% assign categories = site.data.challenges | where_exp: "item", "site.data.snippets.challenges contains item.key" | group_by:"category" | sort: "name" %}

For {{ site.data.snippets.challenges.size }} challenges an additional [coding challenge](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_coding_challenges) is available. In their "Find It" phase they teach
spotting vulnerabilities in the actual codebase of the Juice Shop. In the "Fix It" phase the user then chooses the most appropriate
fix from a list. Solve any of the hacking challenges below to enable a button on the Score Board that launches the corresponding
coding challenge:
<br><br>

<table>
  <tr>
    <th>Category</th>
    <th>#</th>
    <th>Challenges</th>
  </tr>
  {% for category in categories %}
  <tr>
    <td style="min-width: 190px">{{ category.name }}</td>
    <td style="min-width: 60px">{{ category.items.size }}</td>
    <td><small>{{ category.items | group_by:"name" | sort: "name" | map: "name" | join: ", " }}</small></td>
  </tr>
  {% endfor %}
  <tr>
    <td><strong>Total Σ</strong></td>
    <td colspan="2">{{ site.data.snippets.challenges.size }}</td>
  </tr>
</table>

## Mitigation Links

{% assign mitigations = site.data.challenges | group_by:"mitigationUrl" | sort: "name" %}

For many solved challenges links to mitigation techniques are presented on the Score Board by offering a link
to a corresponding [OWASP Cheat Sheet](https://cheatsheetseries.owasp.org/) explaining how to avoid that kind of vulnerability in the first place. The
following cheat sheets are referred to by OWASP Juice Shop as mitigation links:

<ul>
  {% for mitigation in mitigations %}
    {% if mitigation.name and mitigation.name.size != 0 %}
      <li><small><a href="{{ mitigation.name }}" target="_blank">{{ mitigation.name | remove: "https://cheatsheetseries.owasp.org/cheatsheets/" | remove: ".html" | replace: "_", " " }}</a></small></li>
    {% endif %}
  {% endfor %}
</ul>
