---
layout: post
title:  "Rumah Nenek"
date:   2021-02-04 07:33:23 +0800
categories: Liburan
---
<style>
img {
  width: 100%;
  height: auto;
}
</style>

<script type="text/javascript">
  (() => {
  'use strict';
  // Page is loaded
  const objects = document.getElementsByClassName('asyncImage');  Array.from(objects).map((item) => {
    // Start loading image
    const img = new Image();
    img.src = item.dataset.src;
    // Once image is loaded replace the src of the HTML element
    img.onload = () => {
      item.classList.remove('asyncImage');
      return item.nodeName === 'IMG' ? 
        item.src = item.dataset.src :        
        item.style.backgroundImage = `url(${item.dataset.src})`;
    };
  });
})();
</script>

  <div class="wrapper">

    <div class="footer-col-wrapper">
    {% for image in site.static_files %}
	{% if image.path contains 'rumah-nenek/' %}
	
      <div class="footer-col footer-col-2">
        <a href="{{ site.baseurl }}{{ image.path }}"><img src="{{ site.baseurl }}{{ image.path }}" alt="image" width="100%" /></a>
      </div>

      {% endif %}
	{% endfor %}

      
    </div>

  </div>

