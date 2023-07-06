---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

## Instructors

{% comment %} {% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %} 

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %} {% endcomment %}

<style>
  .staffer-container {
    display: inline-block;
    /* Add any additional styling as needed */
  }
</style>

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
  <div class="staffer-container">
    {{ staffer }}
  </div>
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
  <hr> <!-- Optional horizontal line to separate instructors and teaching assistants -->

  {% for teaching_assistant in teaching_assistants %}
    <div class="staffer-container">
      {{ teaching_assistant }}
    </div>
  {% endfor %}
{% endif %}

