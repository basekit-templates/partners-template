---
title: Footer
position: 7
col1_text: |-
  ### Registered at

  BaseKit Platform Ltd.<br/>One Castlepark<br/>Bristol<br/>BS2 0AJ
col2_text: |-
  ### Follow us

  <a href='#'><img src='/uploads/facebook.svg'/></a> <a href='#'><img src='/uploads/twitter.svg'/></a> <a href='#'><img src='/uploads/linkedin.svg'/></a> <a href='#'><img src='/uploads/googleplus.svg'/></a> <a href='#'><img src='/uploads/instagram.svg'/></a>
col3_text: |-
  ### BaseKit Platform © 2016

  VAT NO: 1234567890
id: footer
style: |
  .footer {
    background: #333;
    h3 {
      color: #ffffff;
      font-weight: 500;
    }
    p {
      color: #BDBDBD;
    }
    &__columns {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      text-align: left;
      max-width: 1200px;
      margin: 0 auto;
      padding: 2em;
    }
    .col {
      width: 100%;
      margin-bottom: 1em;
      img {
        width: auto;
      }
      @include breakpoint(break-1) {
        width: 33.33%;
      }
    }
    .typeset a {
      background-image: none;
    }
  }
script: |
  // Header js
---

<footer class="footer">
<div class="footer__columns">
<div class="footer__col1 col typeset">
{{ page.col1_text | markdownify }}
</div>
<div class="footer__col2 col typeset">
{{ page.col2_text | markdownify }}
</div>
<div class="footer__col3 col typeset">
{{ page.col3_text | markdownify }}
</div>
</div>
</footer>