---
layout: page
permalink: /climbing/
title: Rock Climbing
tags: [about]
modified: 09-29-2026
comments: false
body_class: climbing-page
---

<style>
  .climbing-intro {
    margin-bottom: 1.5em;
  }

  .climbing-gallery {
    column-count: 3;
    column-gap: 2em;
  }

  .climbing-photo {
    break-inside: avoid;
    margin: 0 0 1.5em;
  }

  .climbing-photo img {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 2px;
  }

  .climbing-photo figcaption {
    margin-top: 0.65em;
    color: #777;
    font-size: 0.85em;
    line-height: 1.45;
  }

  @media only screen and (max-width: 900px) {
    .climbing-gallery {
      column-count: 2;
      column-gap: 1.5em;
    }
  }

  @media only screen and (max-width: 550px) {
    .climbing-gallery {
      column-count: 1;
    }
  }

  @media only screen and (min-width: 600px) {
    .climbing-page #main {
      width: 94%;
      max-width: 1600px;
    }

    .climbing-page #main .article-author-side {
      display: none;
    }

    .climbing-page #main article {
      display: block;
      float: none;
      width: 100%;
      margin: 0 0 2em;
    }
  }
</style>

<p class="climbing-intro">I like to think that whatever it is that draws me to cryptography is also what
draws me to pursue rock climbing as a sport. While I don't know what that might be, it is a big part of
my life. Here are a few photos of some of my recent climbs.</p>

<div class="climbing-gallery">
  {% for photo in site.data.climbing %}
    <figure class="climbing-photo">
      <img src="{{ '/images/climbingpics/' | append: photo.image | relative_url }}"
           alt="{{ photo.alt }}"
           loading="lazy"
           decoding="async">
      {% if photo.caption and photo.caption != "" %}
        <figcaption>{{ photo.caption }}</figcaption>
      {% endif %}
    </figure>
  {% endfor %}
</div>
