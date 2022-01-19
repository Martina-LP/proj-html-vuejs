<template>
  <footer>
    <div class="container text-center">
      <div class="row">
        <div class="link d-flex">
          <div class="col">
            <div class="list">
              <!-- Logo -->
              <ul>
                <li>
                  <img src="../assets/img/logo-sidearea-1.png" alt="Logo">
                </li>
              </ul>
            </div>
            <!-- End Logo -->
            <div class="list">
              <ul>
                <li>
                  <h6>Let's Get Creative</h6>
                </li>
              </ul>
            </div>
          </div>
          <!-- Contacts -->
          <div class="col">
            <div class="list">
              <ul>
                <li>
                  <a href="#">maree.qode@gmail.com</a>
                </li>
              </ul>
            </div>
            <div class="list">
              <ul>
                <li>
                  <a href="#">+44645 321 789</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="col">
            <div class="list">
              <ul>
                <li>
                  <h6>Avenue d'Auderghem 10</h6>
                </li>
              </ul>
            </div>
            <div class="list">
              <ul>
                <li>
                  <h6>1040 Brussels, Belgium</h6>
                </li>
              </ul>
            </div>
          </div>
          <!-- End Contacts -->  
          <!-- Social -->
          <div class="col">
            <div class="list">
              <ul>
                <li>
                  <h6>Stay in touch with us</h6>
                </li>
              </ul>
            </div>
            <div class="list">
              <ul>
                <li>
                  <a href="#"><i class="fab fa-twitter"></i></a>
                  <a href="#"><i class="fab fa-pinterest-p"></i></a>
                  <a href="#"><i class="fab fa-facebook-f"></i></a>
                  <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </li>
              </ul>
            </div>
          </div>
          <!-- End Social -->
        </div>
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
  height: 160px;
  margin-top: 60px;
  padding: 40px 40px;
  background-color: $aqua_bg;

  .container {
    padding: 30px 0;
    background-color: $aqua_bg;

    .list {
      ul {
        justify-content: space-between;

        li {
          margin-left: 20px;
          font-size: 14px;
          list-style-type: none;

          a {
            text-decoration: none;
            color: $dark;
            font-weight: 400;
            margin-right: 20px;
            cursor: pointer;
          }

          a, h6 {
            display: inline-block;
            color: $dark;
            text-decoration: none;
            font-weight: bold;

            i {
              margin-left: 12px;
            }

          }
        }
      }
    }
  }
}
</style>
