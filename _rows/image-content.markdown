---
title: Image Content
position: 3
main_text: |-
  ## Built for busy people

  Just like social media, Sitebuilder is designed to get things done in minutes. Change colours, fonts, images and more, to create your own unique website.

  ## Instant sharing

  Take a photo on your phone and publish straight to your website.   Your visitors will love how quickly you share things.

  ## Move to the top

  Websites with fresh content rank higher in search engines. Sitebuilder’s speed and simplicity makes it even easier to keep your audience updated, at home or on-the-go.
image: "/uploads/mobile-devices.png"
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
---

<section class="image-content">
  <div class="image-content__main">
    <div class="image-content__image">
      <img src="{{ page.image }}"/>
    </div>
    <div class="image-content__content  typeset">
      {{ page.main_text | markdownify }}
    </div>
  </div>
</section>
