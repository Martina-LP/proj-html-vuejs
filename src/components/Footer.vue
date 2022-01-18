<template>
  <footer class="p-3">
    <div class="footer-container">
      <div class="container">

        <div class="row">
          <div class="news">

          </div>
        </div>

      </div>

    </div>
      <div class="container text-center">
        <div>
          <!-- Logo -->
          <ul class="row p-3">
            <li class="col-3 mb-2">
              <img src="../assets/img/logo-sidearea-1.png" alt="Logo">
            </li>
            <!-- End Logo -->
            <!-- Contacts -->
            <li class="col-3 mb-2">
              <a href="#">maree.qode@gmail.com</a>
            </li>
            <li class="col-3 mb-2">
              <h6>Avenue d'Auderghem 10</h6>
            </li>
            <li class="col-3">
              <h6>Let's Get Creative</h6>
            </li>
            <li class="col-3">
              <a href="#">+44645 321 789</a>
            </li>
            <li class="col-3">
              <h6>1040 Brussels, Belgium</h6>
            </li>
            <!-- End Contacts -->
            <!-- Social -->
            <li class="col-3 mb-2">
              <h6>Stay in touch with us</h6>
            </li>
            <li class="col-3">
              <a href="#"><i class="fab fa-twitter"></i></a>
              <a href="#"><i class="fab fa-pinterest-p"></i></a>
              <a href="#"><i class="fab fa-facebook-f"></i></a>
              <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </li>
            <!-- End Social -->
          </ul>
        </div>
      </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

footer {
  width: 100%;
  height: 100px;
  margin-top: 40px;
  padding: 40px 60px;
  background-color: $aqua_bg;

  .container {
    background-color: $aqua_bg;

    ul {
      justify-content: space-between;

      li {
        margin-left: 40px;
        font-size: 14px;
        list-style-type: none;

        a, h6 {
          display: inline-block;
          color: $dark;
          text-decoration: none;
          font-weight: bold;

          i {
            margin-left: 15px;
          }

        }
      }

      .social {
        align-items: center;

        img {
          margin: 0 10px;
        }

        a {
          text-decoration: none;
          color: $dark;
          font-weight: 600;
          margin-right: 20px;
          cursor: pointer;
        }
      }
    }
  }
}
</style>
