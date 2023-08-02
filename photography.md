---
title: Photography
layout: page
permalink: "/photography/"
order: 4
---
I like to take pictures from time to time.
<div data-nanogallery2 = '{
    "thumbnailWidth": "auto",
    "thumbnailBorderVertical": 1,
    "thumbnailBorderHorizontal": 1,    
    "thumbnailLabel": {
        "position": "overImageOnBottom"
    },
    "thumbnailAlignment": "center",
    "thumbnailOpenImage": true,
    "itemsBaseURL":     "/assets/images/photography/"
  }'>

  <!-- ### gallery content ### -->
  {% for image in site.static_files %}
    {% if image.path contains 'assets/images/photography' %}
      {% unless image.path contains 'thumbnails' %}
        <a href="{{ image.name }}" data-ngthumb="thumbnails/{{ image.basename }}_t.jpg" />
      {% endunless %}
    {% endif %}
  {% endfor %}
</div>