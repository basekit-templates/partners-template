---
layout: default
title: Welcome
excerpt: Welcome to BaseKit
---

{% capture hero-content %}
<h1>The same great experience<br/> across every device</h1>
<p>Your business needs a fresh place to grow,<br/> make it happen today.</p>
<a href="#" class="button">Select Template</a>
{% endcapture %}

{% include blocks/default.html content=hero-content header=true logo=true text-align="center" text-shade="light" background="images/background-hero.jpg" %}


{% capture editor-content %}
<h2>The new way to stay in control</h2>
<p>The only sitebuilder to give you a consistent, experience across your phone, tablet or computer.<br/> No app and no updating required</p>
{% include image.html image="images/image-editor.png" %}
{% endcapture %}

{% include blocks/default.html content=editor-content text-align="center" id="editor" %}


{% capture phone-content %}
{% include image.html image="images/image-phone.png" %}
<div class="content">
  <h2>The same great experience<br/> across every device</h2>
  <p>The only sitebuilder to give you a consistent, experience across your phone, tablet or computer.<br/> No app and no updating required</p>
</div>
{% endcapture %}

{% include blocks/default.html content=phone-content text-align="right" text-shade="light" background="#151F26" content-arrange=true id="every-device" %}


{% capture google-content %}
<h2>Get found at the top</h2>
<p>The only sitebuilder to give you a consistent, experience across your phone, tablet or computer.<br/> No app and no updating required</p>
{% include image.html image="images/image-google.png" %}
{% endcapture %}

{% include blocks/default.html content=google-content text-align="center" %}


{% capture share-content %}
<div class="content">
  <h2>Share moments instantly</h2>
  <p>The only sitebuilder to give you a consistent, experience across your phone, tablet or computer.<br/> No app and no updating required</p>
</div>
{% endcapture %}

{% include blocks/default.html content=share-content text-align="left" background="images/background-sharing.jpg" id="share-moments" %}


{% capture devices-content %}
{% include image.html image="images/image-devices.png" %}
{% endcapture %}

{% include blocks/default.html content=devices-content background="#151F26" text-align="center" %}
