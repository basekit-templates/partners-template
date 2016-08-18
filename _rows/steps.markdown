---
title: Steps
position: 0
id: steps
style: |
  .steps {
    text-align: center;
    &__list {
      list-style: none;
      max-width: 1200px;
      margin: 6rem auto;
      @include breakpoint(break-2) {
        display: flex;
        justify-content: space-around;
      }
    }
    h2 {
      font-weight: 500;
      color: #3A71B0;
    }
    p {
      padding-top: 0;
    }
    &__item {
      width: 100%;
      @include breakpoint(break-2) {
        width: 33.33%;
      }
      padding: 1em 3.5em;
      position: relative;
      &:before,
      &:after {
        content: "";
        position: absolute;
        background: #BDBDBD;
        right: 0;
        bottom: 0;
        margin-right: 40%;
        width: 10.4%;
        height: 1px;
        transform: rotate(-10deg);
        @include breakpoint(break-2) {
          margin-right: 0;
          top: 0;
          left: auto;
          right: .6rem;
          height: 50.4%;
          width: 1px;
        }
      }
      &:after {
        left: 0;
        right: auto;
        margin-right: 0;
        margin-left: 40%;
        transform: rotate(10deg);
        @include breakpoint(break-2) {
          margin-right: 0;
          right: .6rem;
          left: auto;
          bottom: 0;
          top: auto;
        }
      }
      &:last-of-type:before,
      &:last-of-type:after {
        display: none;
      }
    }
  }
script: |
  // Steps js
step_items:
- step_icon: "/uploads/ic_account_circle_black.svg"
  step_title: Choose a template
  step_content: Take a tour through our beautiful template library and choose the
    design you love.
- step_icon: "/uploads/ic_web_black.svg"
  step_title: Make it your own
  step_content: Instantly bring your site to life by customising images, text, colours
    and more.
- step_icon: "/uploads/ic_publish_black.svg"
  step_title: Launch your site
  step_content: Get your site online in just two clicks and welcome your new customers
    today.
---

<section class="steps">
  <ol class="steps__list">
    {% for item in page.step_items %}
      <li class="steps__item  typeset">
        <img src="{{ item.step_icon }}" />
        <h2>{{ item.step_title }}</h2>
        {{ item.step_content | markdownify }}
      </li>
    {% endfor %}
  </ol>
</section>
