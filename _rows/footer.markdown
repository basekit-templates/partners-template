---
title: Footer
position: 7
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
col1_content: "<h3>Registered at</h3><p>BaseKit Platform Ltd.<br/>One Castlepark<br/>Bristol<br/>BS2
  0AJ</p>"
col2_content: "<h3>Follow us</h3><a href='#'><img src='/uploads/facebook.svg'/></a>
  <a href='#'><img src='/uploads/twitter.svg'/></a> <a href='#'><img src='/uploads/linkedin.svg'/></a>
  <a href='#'><img src='/uploads/googleplus.svg'/></a> <a href='#'><img src='/uploads/instagram.svg'/></a>"
col3_content: "<h3>BaseKit Platform &copy; 2016</h3><p>VAT NO: 1234567890</p>"
---

<footer class="footer">
  <div class="footer__columns">
    <div class="footer__col1 col typeset">
      {{ page.col1_content }}
    </div>
    <div class="footer__col2 col typeset">
      {{ page.col2_content }}
    </div>
    <div class="footer__col3 col typeset">
      {{ page.col3_content }}
    </div>
  </div>
</footer>
