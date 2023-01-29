<template>
  <footer>
    <subscribe />
    <!-- <div class="overlay"></div> -->
    <div class="container">
      <div class="section-content">
        <div class="row m-0">
          <div class="col-sm-6 col-md-4">
            <div class="footer-item footer-widget">
              <img
                :src="
                  $store.state.websiteSettings.find((one) => one.key === 'logo')
                    .plain_value
                "
                alt="logoImage"
                style="width: 240px"
              />
            </div>
            <p class="mt-5">
              {{
                $store.state.websiteSettings.find(
                  (one) => one.key === "description"
                ).plain_value
              }}
            </p>
          </div>

          <div class="col-sm-6 col-md-4">
            <div class="footer-item">
              <div class="footer-title">
                <h5>Services</h5>
              </div>
              <ul class="footer-list">
                <!-- <li><a href="#">About Us</a></li> -->
                <li v-for="page in $store.state.footerPages" :key="page.id">
                  <b-nav-item
                    :to="localePath(generatePagePath(page.id))"
                    v-if="page.status"
                    >{{ page.name }}</b-nav-item
                  >
                </li>
              </ul>
            </div>
          </div>

          <div class="col-sm-6 col-md-4">
            <div class="footer-item">
              <div class="footer-title">
                <h5>Contact</h5>
              </div>
              <p>
                <i class="fa-solid fa-envelope"></i>
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "email"
                  ).plain_value
                }}
              </p>
              <p>
                <i class="fa-solid fa-phone"></i>

                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "contact_phone"
                  ).plain_value
                }}
              </p>
              <p>
                <i class="fa-solid fa-location-dot"></i>

                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "contact_address"
                  ).plain_value
                }}
              </p>
            </div>
          </div>
        </div>
        <div class="row m-0">
          <div class="col-12 copyrights">
            <p>© Powered By: Rail Coder – 2021. All rights reserved.</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Subscribe from "../subscribe/subscribe.vue";
export default {
  name: "AppFooter",
  components: { Subscribe },
  data() {
    return {};
  },
  beforeMount() {},
  methods: {
    generatePagePath(id) {
      switch (id) {
        case 1:
          return "/about";
        case 2:
          return "/contact";
        case 3:
          return "/terms";
        case 4:
          return "/policy";
      }
    },
  },
};
</script>
<style>
footer {
  padding: 20px 30px 0;
  background-color: rgb(32, 43, 143);
  position: relative;
}
footer .overlay {
  background-image: url("https://the7.io/business-advisors/wp-content/uploads/sites/72/2020/04/blob-scene-haikei-8.i");
  background-position-x: 50%;
  background-position-y: 50%;
  background-size: cover;
  box-sizing: border-box;
  color: rgb(94, 100, 107);
  filter: brightness(1) contrast(1) saturate(1) blur(0px) hue-rotate(0deg);
  left: 0px;
  right: 0;
  opacity: 0.16;
  position: absolute;
  top: 0px;
  bottom: 0;
  mix-blend-mode: multiply;
}
footer p {
  color: rgb(255, 255, 255);
  font-size: 16px;
  line-height: 24px;
}
footer h5 {
  color: rgba(255, 255, 255, 0.5);
  font-size: 19px;
  font-weight: 600;
  line-height: 26.6px;
  margin-bottom: 30px;
}
footer .footer-item a {
  color: rgb(255, 255, 255);
  display: block;
  font-size: 15px;
  font-weight: 400;
  line-height: 22.5px;
  text-align: left;
  text-decoration: none;
  margin-bottom: 15px;
}
footer .footer-item a:hover {
  color: #30a46c;
}
footer .footer-item a i {
  color: #30a46c;
  margin-right: 10px;
}
footer .copyrights p {
  color: rgba(255, 255, 255, 0.5);
  font-size: 13px;
  font-weight: 400;
  line-height: 18.2px;
  text-align: left;
  padding: 90px 0 30px;
}
.footer-list {
  padding: 0;
  list-style: none;
}
</style>
