---
layout: gym-default
title: Aquent Gymnasium | Course Catalog
meta_description: Catalog of all Gymnasium courses
---

<header class="main-header">
  <h1>Course Catalog</h1>
</header>

<h2>Full Courses</h2>
<p>Description of Full Courses goes here.</p>
{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "full" %}
<h3><img src="{{ course.course_art }}" height="60" width="60">{{ course.title }}</h3>
<p>{{ course.short_description }}
<br />
<a href="{{ course.course_URL }}">Learn More</a></p>

<h4>Skills Covered</h4>
<ul>
{% for item in course.skills %}
<li>{{item}}</li>
{% endfor %}
</ul>

<h4>This Course is For</h4>
<ul>
{% for item in course.audience %}
<li>{{item}}</li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

<h2>Gym Shorts</h2>
<p>Description of Gym Shorts goes here.</p>
{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "short" %}
<h3><img src="{{ course.course_art }}" height="60" width="60">{{ course.title }}</h3>
<p>{{ course.short_description }}
<br />
<a href="{{ course.course_URL }}">Learn More</a></p>

<h4>Skills Covered</h4>
<ul>
{% for item in course.skills %}
<li>{{item}}</li>
{% endfor %}
</ul>

<h4>This Course is For</h4>
<ul>
{% for item in course.audience %}
<li>{{item}}</li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}
