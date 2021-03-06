---
title: Grow your business with a beautiful website
position: 0
logo_image: "/uploads/logo.svg"
subtitle: Create a site, blog or online store today
background_color: "#000"
background_video_file: "/uploads/background-video.mp4"
background_image: "/uploads/background-video.png"
button_text: Start your free trial
button_link: "#pricing"
banner_text: Learn more in 60 seconds
banner_link: https://www.youtube.com/watch?v=OLU3-5xbzEU
id: header
style: |
  .header {
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    position: relative;
    height: 100vh;
    overflow: hidden;
    background: #333;
    background-size: cover;
    background-position: center;
    &__video {
      position: absolute;
      min-width: 100vw;
      min-height: 100vh;
      opacity: 0.75;
      ~ * {
        z-index: 1;
      }
    }
    &__top {
      text-align: left;
    }
    &__logo {
      padding: 2rem;
      img {
        width: 140px;
        height: auto;
      }
    }
    h1,
    h2,
    p,
    .banner {
      color: #fff;
    }
    &__banner {
      display: block;
      padding: 1rem 0;
      background: rgba(74,143,226,0.60);
    }
    .banner {
      -webkit-backdrop-filter: blur(10px);
      backdrop-filter: blur(10px);
      &__icon {
        vertical-align: middle;
      }
    }
  }
script: |
  // Header js
---

<header class="header" style="background: {{ page.background_color }}">
  <video class="header__video" autoplay loop muted playsinline poster="{{ page.background_image }}" >
    <source src="{{ page.background_video_file }}" type="video/mp4">
  </video>
  <div class="header__top">
    <div class="header__logo">
      <img src="{{ page.logo_image }}"/>
    </div>
  </div>
  <div class="header__main  typeset">
    <h1 class="header__title">{{ page.title }}</h1>
    <h2 class="header__subtitle">{{ page.subtitle }}</h2>
    <br/>
    <a class="header__button  button" href="{{ page.button_link }}">{{ page.button_text }}</a>
  </div>
  <div class="header__bottom  typeset">
    <a class="header__banner  banner" href="{{ page.banner_link }}">
      <svg class="banner__icon" width="24px" height="24px" viewBox="0 1 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
          <g id="ic_play_circle_outline_black_24px" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" transform="translate(0.000000, 1.000000)">
              <g id="Group">
                  <polygon id="Shape" points="0 0 24 0 24 24 0 24"></polygon>
                  <path d="M10,16.5 L16,12 L10,7.5 L10,16.5 L10,16.5 Z M12,2 C6.48,2 2,6.48 2,12 C2,17.52 6.48,22 12,22 C17.52,22 22,17.52 22,12 C22,6.48 17.52,2 12,2 L12,2 Z M12,20 C7.59,20 4,16.41 4,12 C4,7.59 7.59,4 12,4 C16.41,4 20,7.59 20,12 C20,16.41 16.41,20 12,20 L12,20 Z" id="Shape" fill="#FFFFFF"></path>
              </g>
          </g>
      </svg>
      <small class="banner__text">{{ page.banner_text }}</small>
    </a>
  </div>
</header>
