<template>
  <section class="why">
    <div class="row m-0 align-items-center justify-content-center">
      <div class="col-lg-6" style="padding: 0 60px">
        <h3>
          {{ whyUs.find((one) => one.key === "why_choose_us_title").value }}
        </h3>
        <p>
          {{
            whyUs.find((one) => one.key === "why_choose_us_description").value
          }}
        </p>
        <ul>
          <li
            v-for="item in whyUs.find((one) => one.key === 'why_choose_us_list')
              .value"
            :key="item"
          >
            <i :class="item.icon"></i>
            {{ item.title }}
          </li>
        </ul>
      </div>
      <div class="col-lg-6 image">
        <img src="/assets/images/blob2.svg" alt="blob" class="blobImage1" />
        <img
          class="img-fluid mainImage"
          :src="whyUs.find((one) => one.key === 'why_choose_us_image').value"
          alt="image"
        />
        <img src="/assets/images/blob1.svg" alt="blob" class="blobImage2" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeWhy",
  props: ["whyUs"],
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>
<style>
.why {
  position: relative;
  padding: 0 0 90px;
}
.why h3 {
  color: rgb(0, 0, 0);
  font-size: 31px;
  font-weight: 400;
  line-height: 37.2px;
  margin-bottom: 30px;
}

.why p {
  color: rgb(94, 100, 107);
  font-size: 18px;
  font-weight: 400;
  line-height: 28.8px;
  margin-bottom: 40px;
}
.why ul {
  list-style: none;
  padding: 0;
}
.why li {
  color: rgb(0, 0, 0);
  font-size: 18px;
  margin: 7.5px 0 0;
  padding: 0 0 7.5px;
}
.why li i {
  color: rgb(0, 206, 200);
  font-size: 20px;
  margin-right: 5px;
}
.why .image {
  position: relative;
  display: flex;
  flex-direction: columns;
  justify-content: center;
}
.why .image img {
  /* -webkit-mask-image: url(https://the7.io/business-advisors/wp-content/uploads/sites/72/2021/09/sqr005.svg); */
  -webkit-mask-size: contain;
  -webkit-mask-position: center center;
  -webkit-mask-repeat: no-repeat;
  max-width: 580px;
  border-radius: 30% 70% 25% 75% / 52% 47% 53% 48%;
}
.why .image .image-icon {
  color: rgb(94, 100, 107);
  font-size: 18px;
  position: absolute;
  left: 390px;
  top: 345px;
  z-index: 3;
  width: 140px;
}
.why .form-control {
  background-color: rgb(255, 255, 255);
  border: 2px solid rgb(226, 233, 239);
  border-radius: 6px;
  color: rgb(0, 0, 0);
  font-size: 18px;
  height: 59px;
  line-height: 26px;
  max-width: 100%;
  min-height: 59px;
  padding-bottom: 7px;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 7px;
  margin-bottom: 20px;
}
</style>
