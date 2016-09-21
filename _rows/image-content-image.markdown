---
title: Image Content Image
position: 4
main_text: |-
  ## Designed by professionals

  ### Each template delivers high quality, a professional finish<br/>and custom design for creating something truly unique.
top_image: "/uploads/templates-row1.png"
bottom_image: "/uploads/templates-row2.png"
id: image-content-image
style: |
  .image-content-image {
    text-align: center;
    background: #4281c9;
    padding: 2rem 0;
    &__main {
      overflow-x: hidden;
    }
    &__content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 3.2rem 6rem 4.6rem;
    }
    &__image {
      img {
        width: 100%;
      }
    }
    h2,
    h3,
    h4,
    h5,
    h6,
    p {
      color: #ffffff;
    }
    h3 {
      font-weight: 600;
    }
    &__image {
      overflow: hidden;
      white-space: nowrap;
      width: 200%;
      @include breakpoint(break-2) {
        width: 100%;
      }
    }
    &__image img {
      will-change: left;
      animation: marquee 24s linear infinite;
      position: relative;
    }
    @keyframes marquee {
      0% { left: 0; }
      100% { left: -100%; }
    }
  }
script: |
  // Image Content Image js
---

<section class="image-content-image">
  <div class="image-content-image__main">
    <div class="image-content-image__image">
      <img src="{{ page.top_image }}"/><img src="{{ page.top_image }}"/>
    </div>
    <div class="image-content-image__content  typeset">
      {{ page.main_text | markdownify }}
    </div>
    <div class="image-content-image__image">
      <img src="{{ page.bottom_image }}"/><img src="{{ page.bottom_image }}"/>
    </div>
  </div>
</section>
