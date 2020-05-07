---
title: Challenges
layout:  null
altfooter: true
tab: true
order: 2
tags: juiceshop
---

## Challenge Categories

{% assign categories = site.data.challenges | group_by:"category" | sort: "name" %}

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
