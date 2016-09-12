---
title: Content Grid
position: 5
content_items:
- content_icon_image: "/uploads/ic_share_black_24px.svg"
  content_title: Social
  content_text: Bring everything together with social integrations. Display your most
    up-to-date posts anywhere on your website
- content_icon_image: "/uploads/ic_format_paint_black_24px.svg"
  content_title: Customisation/template picker
  content_text: Keep your site refreshed and on-trend by changing templates at any
    time. You won’t lose any content and you can swap your template back at anytime
- content_icon_image: "/uploads/ic_devices_black_24px.svg"
  content_title: Built for any device
  content_text: It doesn’t matter what screen size your customers are viewing your
    website on, sitebuilder sites will always look beautiful on phones, tablets and
    computers
- content_icon_image: "/uploads/ic_edit_black_24px.svg"
  content_title: Blog
  content_text: Attract more customers by writing about the things you love. Using
    blog categories and tags will help your visitors find your content easily
- content_icon_image: "/uploads/ic_contact_mail_black_24px.svg"
  content_title: Contact forms
  content_text: Give your customers the option to contact you directly from your website
    and have those enquiries sent straight to your inbox
- content_icon_image: "/uploads/ic_monochrome_photos_black_24px.svg"
  content_title: Image editor
  content_text: Get your photos looking even better than they do on Instagram. Use
    our image editor to add filters, resize images and reduce red eye
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