---
layout: gym-default
title: Aquent Gymnasium | Course Catalog
meta_description: Catalog of all Gymnasium courses
---

<!-- <header class="main-header">
  <h1>Course Catalog</h1>
</header> -->

<section id="full-courses">

<h2>Full Courses</h2>
<p>All our full courses are taught by experienced practitioners and focused on in-demand skills and technologies. Each includes 3 to 6 hours of video instruction, quizzes, assignments, a final exam, and certification when you pass!</p>

{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "full" %}

<article class="course" id="{{ course.course | downcase }}">

<img src="{{ course.course_art }}" height="60" width="60">
<h3>{{ course.title }}</h3>
<p>{{ course.short_description }}</p>
<a href="{{ course.course_URL }}">Learn More</a>

<section>
<h4>Skills Covered</h4>
<ul>
{% for item in course.skills %}
<li>{{item}}</li>
{% endfor %}
</ul>
</section>

<section>
<h4>This Course is For</h4>
<ul>
{% for item in course.audience %}
<li>{{item}}</li>
{% endfor %}
</ul>

</section>

</article>

{% endif %}
{% endfor %}
</section>

<section id="gym-shorts">

<h2>Gym Shorts</h2>
<p>Gym Shorts are short, snackable courses that all last under an hour. Like our longer courses, they are practical, taught by experienced practitioners, and focused on in-demand skills and technologies.</p>

{% assign sorted_courses = site.data.catalog | sort: 'course' %}
{% for course in sorted_courses %}
{% if course.type == "short" %}

<article class="course" id="{{ course.course | downcase }}">

<img src="{{ course.course_art }}" height="60" width="60">
<h3>{{ course.title }}</h3>
<p>{{ course.short_description }}</p>
<a href="{{ course.course_URL }}">Learn More</a>

<section>
<h4>Skills Covered</h4>
<ul>
{% for item in course.skills %}
<li>{{item}}</li>
{% endfor %}
</ul>
</section>

<section>
<h4>This Course is For</h4>
<ul>
{% for item in course.audience %}
<li>{{item}}</li>
{% endfor %}
</ul>
</section>

</article>

{% endif %}
{% endfor %}
</section>
