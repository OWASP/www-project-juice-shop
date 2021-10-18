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
[step-by-step tutorial](https://pwning.owasp-juice.shop/part1/challenges.html#hacking-instructor)
for that particular challenge on our public
<https://demo.owasp-juice.shop> instance. If you are entirely new to the
Juice Shop, we recommend doing them in the listed order. With the
(optional)
[Tutorial Mode](https://pwning.owasp-juice.shop/part1/challenges.html#tutorial-mode)
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
</table>

## Coding Challenges

{% assign codingChallenges = site.data.challenges | where_exp: "item", "site.data.snippets.challenges contains item.key" | sort: "name" %}

For {{ codingChallenges.size }} challenges an additional coding challenge is available. In their "Find It" phase they teach
spotting vulnerabilities in the actual codebase of the Juice Shop. In the "Fix It" phase the user then chooses the most appropriate
fix from a list. Solve any of the hacking challenges below to enable a button on the Score Board that launches the corresponding
coding challenge.

{% for codingChallenge in codingChallenges %}
* {{ codingChallenge.name }}
{% endfor %}
