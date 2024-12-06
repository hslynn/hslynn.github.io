---
layout:  page
title: 二皮家的黄箱箱儿 
published: true 
---
# {{page.title}}

<table align="center" border="3" width="402">

  <tbody>
    <tr>
      <td>日期</td>
      <td>皮皮</td>
      <td>二哥</td>
      <td>支出</td>
      <td>备注</td>
    </tr>
{% assign pipi_total = 0 %}
{% for entry in site.data.ledger %}
    {% assign pipi_total = pipi_total | plus: entry.pipi %}
    {% assign erge_total = erge_total | plus: entry.erge %}
    {% assign spend_total = spend_total | plus: entry.spend %}
    <tr>
      <td>{{ entry.date }}</td>
      <td>{{ entry.pipi }}</td>
      <td>{{ entry.erge }}</td>
      <td>{{ entry.spend}}</td>
      <td>{{ entry.note }}</td>
    </tr>
{% endfor %}
    <tr>
      <td>合计</td>
      <td>{{ pipi_total }}</td>
      <td>{{ erge_total }}</td>
      <td>{{ spend_total }}</td>
      <td>{{ pipi_total | plus: erge_total | plus: spend_total}}</td>
    </tr>
  </tbody>
  <colgroup>
    <col style="width: 25%;">
    <col style="width: 25%;">
    <col style="width: 25%;">
    <col style="width: 25%;">
    <col style="width: 25%;">
  </colgroup>
</table>

