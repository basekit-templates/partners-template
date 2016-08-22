---
maincontent: "### Affordable prices and packages to suit your needs"
pricing_lists:
- title: Sitebuilder
  content: |
    *   **Unlimited pages**
    *   **Unlimited templates**
    *   **Social integrations**
    *   **10 free stock images**
    *   **Developer tools**
    *   ~~Sell unlimited products~~
    *   ~~Accept major credit cards~~
    *   ~~Safe & secure shopping cart~~
  price: "€12 <sup>per month</sup>"
  button_text: Select package
  button_link: "#"
- title: Storebuilder
  content: |
    *   **Unlimited pages**
    *   **Unlimited templates**
    *   **Social integrations**
    *   **10 free stock images**
    *   **Developer tools**
    *   **Sell unlimited products**
    *   **Accept major credit cards**
    *   **Safe & secure shopping cart**
  price: "€20 <sup>per month</sup>"
  button_text: Select package
  button_link: "#"
button_text: Start your free trial today
button_link: "#"
title: Pricing
position: 6
id: pricing
style: |
  .pricing {
    padding: 2rem 0;
    text-align: center;
    background: #4281c9;
    &__lists {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      max-width: 680px;
      margin: 2rem auto;
      padding: 0 2em;
      text-align: left;
    }
    &__item {
      width: 100%;
      display: flex;
      flex-direction: column;
      @include breakpoint(break-1) {
        width: 48%;
      }
      padding: .5em 1.5em 2em;
      margin-bottom: 1em;
      position: relative;
      background: #ffffff;
      border-radius: 4px;
      box-shadow: 0px 2px 1px 0px rgba(0,0,0,0.20);
      h2 {
        color: #3A71B0;
        text-align: center;
      }
      &-footer {
        text-align: center;
      }
      ul {
        flex: 1;
      }
      ul > li {
        position: relative;
        padding-right: 1rem;
        strong:after {
          content: "";
          position: absolute;
          top: 0;
          right: 0;
          height: 1rem;
          width: .5rem;
          border-bottom: 2px solid green;
          border-right: 2px solid green;
          transform: rotate(45deg);
        }
      }
      del {
        color: #999999;
        background: #ffffff;
      }
      img {
        width: 3.5rem;
        height: auto;
        float: right;
        padding: .5rem;
        margin: 0 0 .5rem .5rem;
        background: rgba(0,0,0,0.07);
        border-radius: 100%;
      }
      li {
        list-style: none;
      }
    }
    > h2,
    > h3,
    > h4,
    > h5,
    > h6,
    > p,
    > li,
    small {
      color: #ffffff;
    }
    &__price {
      @include sassline($fontsize: 34, $font: $bodytype, $lineheight: 3, $below: 0, $breakpoint: all);
      color: #4281c9;
      sup {
        font-size: .4em;
        line-height: 3.8em;
        vertical-align: top;
        color: #4281c9;
        font-weight: 500;
      }
    }
    &__divider-comment {
      background: #4281c9;
      padding: .5em 1em;
    }
    &__divider {
      margin: -3.95rem auto 0 !important;
      max-width: 640px;
    }
    &__button {
      color: #ffffff;
      display: inline-block;
      background: #4CAF50;
      padding: .6rem 1.6rem;
      border-radius: 2px;
    }
  }
script: |
  // Pricing js
---

<section class="pricing  typeset" id="pricing">
  <h2>{{ page.title }}</h2>
  {{ page.maincontent | markdownify }}
  <div class="pricing__lists">
    {% for list in page.pricing_lists %}
      <div class="pricing__item  typeset">
        <h2>{{ list.title }}</h2>
        {{ list.content | markdownify }}
        <div class="pricing__item-footer">
          <span class="pricing__price">{{ list.price }}</span><br/>
          <a class="pricing__button  button" href="{{ list.button_link }}">{{ list.button_text }}</a>
        </div>
      </div>
    {% endfor %}
  </div>
  <div class="pricing__footer">
    <small class="pricing__divider-comment"><em>OR</em></small>
    <hr class="pricing__divider"/>
    <a class="pricing__button  button" href="{{ page.button_link }}">{{ page.button_text }}</a>
  </div>
</section>
