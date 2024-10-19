---
layout: post
title:  "Lettre d'informations"
author: gspp
categories: [ et aussi... ]
image: "assets/images/infos.jpg"
---


{% assign pdfs = site.static_files | where: "pdf", true | where_exp: "item", "item.path contains 'infos_'" %}
{% assign pdfs = pdfs | sort: "path" %}

{% for pdf in pdfs %}
  <a href="{{ pdf.path }}">{{ pdf.path | split: "/" | last }}</a><br>
{% endfor %}
