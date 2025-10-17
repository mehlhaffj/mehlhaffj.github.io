---
layout: page
title: Research
permalink: /projects/
description: 
nav: true
nav_order: 3
display_categories: [by theme]
horizontal: false
---

<div style="width: 100%; text-align: right; margin-bottom: 0;">
<h2>
<font color="#E5E5E5">at a glance</font>
</h2>
</div>
<hr style="margin-top: -4px;">

<div class="row align-items-center">
    <div class="col-sm mt-3 mt-md-0">
        <p>
            When black holes actively feed, they sometimes launch highly collimated, powerful, and rapidly propagating plasma jets into their environments. One famous example of such a jet is the one from the radio galaxy Cygnus A, pictured <span class="d-inline d-sm-none">below</span><span class="d-none d-sm-inline">here</span>.
        </p>
        <p>
            The power source for the jet, very likely the supermassive black hole at the center of the galaxy, is far too small to appear in the image.
        </p>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cygnusa.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Composite image of Cygnus A with X-ray light (NASA/CXC/SAO) colored blue, optical light (NASA/STScI) colored yellow, and radio (NSF/NRAO/AUI/VLA) colored red.
        </div>
    </div>
</div>

<div class="row align-items-center">
    <div class="col-sm mt-3 mt-md-0">
        <p>That last image is an observational point of view. A theoretical picture of a jetted black hole, containing several features that these systems are thought to have, might resemble the sketch <span class="d-inline d-sm-none">below</span><span class="d-none d-sm-inline">to the right</span>.
        </p>
        <p>Theoretically, a black hole acts as a kind of engine. Its fuel is the gravitational energy of the plasma falling onto it in the form of an accretion disk. Some of this energy is transformed by the black hole into the energy of the launched jet.
        </p>
        <p>The accretion disk is also likely threaded by a magnetic field. This magnetic field is in some cases thought to form a dilute magnetized atmosphere--called a corona--above the disk. </p>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/jet_schematic_reduced.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Theoretical cartoon image of a jetted black hole. Only one of the bipolar jets is drawn.
        </div>
    </div>
</div>

<strong>My major research themes focus largely on the physics at different locations in a jetted black hole system: <font color="#980098">jet</font>, <font color="#00B4B4">corona</font>, and <font color="#FFBFBF">disk</font>.</strong>

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
