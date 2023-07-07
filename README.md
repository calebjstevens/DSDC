---
layout: home
title: DSDC
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: DSDC
---
<img src="/assets/images/logo.jpg" alt="Logo">

# Data Science Discovery Course

The Data Science Discovery Course is a month long dive into core data science concepts aimed at high schoolers or recent grads. This class is open to all no matter your familiarity with data science or programming. We urge you to step out of your comfort zones and learn something new!

This website is organized as follows:

- a [course calendar](calendar.md),
- a [staff](staff.md) page,
- and an about [about](about.md) page.

## Meet the Instructors

{% assign instructors = site.staffers | where: 'role', 'Instructor' %} {% for staffer in instructors %} {{ staffer }} {% endfor %}



