---
title: Image Content
position: 2
id: image-content
style: |
  .image-content {
    text-align: left;
    &__main {
      max-width: 1200px;
      margin: 0 auto;
      @include breakpoint(break-2) {
        display: flex;
        align-items: center;
      }
    }
    @include breakpoint(break-2) {
      &__image,
      &__content {
        width: 50%;
      }
    }
    &__content,
    &__image {
      padding: 3.2rem 2rem;
    }
    h2 {
      font-weight: 500;
      color: #3A71B0;
    }
  }
script: |
  // Image Content js
maincontent: "<h2>Built for busy people</h2><p>Just like social media, Sitebuilder
  is designed to get things done in minutes. Change colours, fonts, images and more,
  to create your own unique website.</p><h2>Instant sharing</h2><p>Take a photo on
  your phone and publish straight to your website.\LYour visitors will love how quickly
  you share things.</p><h2>Move to the top</h2><p>Websites with fresh content rank
  higher in search engines. Sitebuilder’s speed and simplicity makes it even easier
  to keep your audience updated, at home or on-the-go.</p>"
image: "/uploads/mobile-devices.png"
---

<section class="image-content">
  <div class="image-content__main">
    <div class="image-content__image">
      <img src="{{ page.image }}"/>
    </div>
    <div class="image-content__content  typeset">
      {{ page.maincontent }}
    </div>
  </div>
</section>
