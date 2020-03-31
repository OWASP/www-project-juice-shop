---
title: Challenges
layout:  null
tab: true
order: 2
tags: juiceshop
---

## Challenge Categories

{% assign categories = site.data.challenges | group_by:"category" | sort: "name" %}

{% assign tutorials = site.data.challenges | where_exp: "item", "item.tutorial != null" | sort: "tutorial.order" %}

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
    <td colspan="2">{{ site.data.challenges.size }}</td>
  </tr>
</table>

![Juicy Bot](https://raw.githubusercontent.com/bkimminich/juice-shop/master/frontend/src/assets/public/images/juicyBot.png)

## Hacking Instructor Tutorials

Click on a link in the table below to launch a <a
href="https://pwning.owasp-juice.shop/part1/challenges.html#hacking-instructor"
target="_blank">step-by-step tutorial</a> for that particular challenge
on our public <a href="https://demo.owasp-juice.shop"
target="_blank">https://demo.owasp-juice.shop</a> instance. If you are
entirely new to the Juice Shop, we recommend doing them in the listed
order.

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

