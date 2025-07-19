---
layout: home
title: Home
nav_order: 1
has_toc: false
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<!-- 
This will be the home page of your module. It should give a small introduction to the student about the workshop topic.
Add, edit, or remove any content below for the workshop in question. -->

<!-- Title slide image. Replace img src with your own, or comment this out. -->
<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

<!-- Main header -->
# 2025-2026 Digital Research Workshops

Launched in 2023-2024, Digital Research workshops draw on the expertise of colleagues in the Digital Research Commons Pilot. Digital Research workshops help registrants with information security, website development, code and research information management, and research impact.

These workshops welcome students, staff, and faculty from any discipline, as well as the public at large. Some are also geared towards beginners, so even if you’re new to digital research, we encourage you to sign up and learn!

## 2024-25 DMDS Workshops

<!-- If creating or installing is covered in the module (preparation), mention that in brackets. -->

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
{% if workshop.title != null and workshop.title != "Home" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>

## Land Acknowledgement

<!-- Grabs the default SCDS land acknowledgment. If you want to use a custom one, replace this line with it. -->
{% include def/land_ack.md %}