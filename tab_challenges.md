---
title: Challenges
layout:  null
tab: true
order: 2
tags: juiceshop
---

## Hacking Challenges

{% assign categories = site.data.challenges | group_by:"category" | sort: "name" %}

<table>
  <tr>
    <th>Category</th>
    <th>#</th>
    <th>Challenges</th>
  </tr>
  {% for category in categories %}
  <tr>
    <td style="width: 250px">{{ category.name }}</td>
    <td style="width: 80px">{{ category.items.size }}</td>
    <td><small>{{ category.items | group_by:"name" | sort: "name" | map: "name" | join: ", " }}</small></td>
  </tr>
  {% endfor %}
  <tr>
    <td style="white-space:nowrap;"><strong>Total Σ</strong></td>
    <td colspan="2">{{ site.data.challenges.size }}</td>
  </tr>
</table>
