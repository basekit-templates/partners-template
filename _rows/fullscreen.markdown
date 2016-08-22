---
title: Refresh your site on the go
position: 2
maincontent: "### Use your mobile phone to stay in control of your website and your
  business"
background_image: "/uploads/background-phone.jpg"
id: fullscreen
style: |
  .fullscreen {
    text-align: left;
    background: #333;
    background-size: cover;
    background-position: center;
    &__main {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      max-width: 1200px;
      min-height: 45vh;
      margin: 0 auto;
    }
    &__content {
      max-width: 75%;
      @include breakpoint(break-2) {
        max-width: 50%;
      }
      padding: 0 3.2rem;
      text-shadow: 0px 0px 9px rgba(0,0,0,0.50);
    }
    .typeset * {
      color: #fff;
      font-weight: 600;
    }
    .typeset h2 {
      font-weight: 300;
    }
  }
script: |
  // Fullscreen js
---

<section class="fullscreen" style="background-image: url({{ page.background_image }})">
  <div class="fullscreen__main">
    <div class="fullscreen__content  typeset">
      <h2>{{ page.title }}</h2>
      {{ page.maincontent | markdownify }}
    </div>
  </div>
</section>
