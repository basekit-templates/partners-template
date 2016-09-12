---
title: Content Grid
position: 5
content_items:
- content_icon_image: "/uploads/ic_share_black_24px.svg"
  content_title: Choose a template?
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
- content_icon_image: "/uploads/ic_format_paint_black_24px.svg"
  content_title: Choose a template
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
- content_icon_image: "/uploads/ic_devices_black_24px.svg"
  content_title: Choose a template
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
- content_icon_image: "/uploads/ic_edit_black_24px.svg"
  content_title: Choose a template
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
- content_icon_image: "/uploads/ic_contact_mail_black_24px.svg"
  content_title: Choose a template
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
- content_icon_image: "/uploads/ic_monochrome_photos_black_24px.svg"
  content_title: Choose a template
  content_text: Take a tour through our beautiful template library and choose the
    design you love.
id: content-grid
style: |
  .content-grid {
    padding: 2rem 0;
    &__list {
      list-style: none;
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      max-width: 1200px;
      margin: 2rem auto;
    }
    &__item {
      width: 100%;
      @include breakpoint(break-1) {
        width: 50%;
      }
      @include breakpoint(break-2) {
        width: 33.33%;
      }
      padding: 0 2.5em;
      margin: 1.5em 0;
      position: relative;
      h3 {
        color: #3A71B0;
        font-weight: 500;
      }
    }
    &__icon {
      text-align: center;
      width: 60px;
      height: 60px;
      float: right;
      padding: 10px;
      margin: .5rem 0 .5rem .5rem;
      background: rgba(0,0,0,0.07);
      border-radius: 100%;
      display: flex;
      justify-content: center;
      img {
        width: auto;
      }
    }
  }
script: |
  // Content Grid js
---

<section class="content-grid">
<div class="content-grid__list">
{% for item in page.content_items %}
<div class="content-grid__item  typeset">
<div class="content-grid__icon  icon"><img src="{{ item.content_icon_image }}" /></div>
<h3>{{ item.content_title }}</h3>
{{ item.content_text | markdownify }}
</div>
{% endfor %}
</div>
</section>