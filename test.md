---
layout: gym-default
title: Aquent Gymnasium | Course Catalog
meta_description: Catalog of all Gymnasium courses
---

<header class="main-header">
  <h1>Course Catalog</h1>
</header>


<h2>Full Courses</h2>
<ul>
{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "full" %}
<li>{{ course.course }} - <a href="{{ course.course_URL }}">{{ course.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

<h2>Gym Shorts</h2>
<ul>
{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "short" %}
<li>{{ course.course }} - <a href="{{ course.course_URL }}">{{ course.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
