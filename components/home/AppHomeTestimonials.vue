<template>
  <section class="testimonials">
    <div class="row">
      <h4>What clients say about our work</h4>
    </div>
    <div class="row m-0">
      <swiper :options="swiperOption" v-if="testimonials.length >= 1">
        <swiper-slide v-for="item in testimonials" :key="item.id">
          <div>
            <div class="item">
              <img :src="item.image" :alt="item.title" />
              <p>
                {{ item.description }}
              </p>
              <h5>
                {{ item.name }}
              </h5>
              <h6>
                {{ item.job }}
              </h6>
              <p>
                <a href="#" class="btn">View case</a>
              </p>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>
<script>
export default {
  name: "AppHomeTestimonials",
  props: ["testimonials"],
  data() {
    return {
      swiperOption: {
        loop: true,
        slidesPerView: 3,
        spaceBetween: 50,
        breakpoints: {
          // when window width is >= 320px
          100: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 480px
          480: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          // when window width is >= 640px
          640: {
            slidesPerView: 1,
            spaceBetween: 5,
          },
          992: {
            slidesPerView: 2,
            spaceBetween: 5,
          },
          1200: {
            slidesPerView: 3,
            spaceBetween: 5,
          },
        },
      },
    };
  },
  methods: {},
};
</script>
<style>
.testimonials {
  margin: 0 0 60px;
  padding: 30px 60px;
}
.testimonials h4 {
  color: rgb(0, 206, 200);
  font-size: 22px;
  font-weight: 400;
  line-height: 30.8px;
  margin-bottom: 60px;
  text-align: center;
}
.testimonials .item {
  margin: 0 30px;
  display: flex;
  flex-direction: column;
}
.testimonials .item img {
  width: 120px;
  border-radius: 50%;
  margin: 0 auto 30px;
}
.testimonials .item p {
  color: rgb(94, 100, 107);
  font-size: 20px;
  font-style: italic;
  line-height: 30px;
  margin-bottom: 20px;
  text-align: center;
}
.testimonials .item h5 {
  color: rgb(0, 0, 0);
  font-size: 18px;
  font-weight: 400;
  line-height: 25.2px;
  text-align: center;
}
.testimonials .item h6 {
  color: rgb(166, 175, 179);
  font-size: 16px;
  line-height: 24px;
  margin-bottom: 30px;
  text-align: center;
}
.testimonials .item .btn {
  align-items: center;
  background-color: rgb(63, 82, 254);
  border-radius: 6px;
  border: none;
  box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
  color: rgb(255, 255, 255);
  display: flex;
  font-size: 14px;
  font-weight: 400;
  line-height: 14px;
  margin: 0 auto 0;
  min-height: 36px;
  min-width: 50px;
  padding-bottom: 8px;
  padding-left: 14px;
  padding-right: 14px;
  padding-top: 8px;
  text-align: center;
  text-decoration-color: rgb(255, 255, 255);
  text-decoration-line: none;
  text-decoration-style: solid;
  text-decoration-thickness: auto;
  transition-delay: 0s;
  transition-duration: 0.3s;
  transition-property: all;
  transition-timing-function: ease;
  display: inline-block;
}
.testimonials .slick-prev {
  left: -25px;
}
.testimonials .slick-next {
  right: -25px;
}
.testimonials .slick-prev,
.testimonials .slick-next {
  width: 40px;
  height: 40px;
  z-index: 2;
}
.testimonials .slick-prev::before,
.testimonials .slick-next::before {
  font-family: "slick";
  font-size: 40px;
  line-height: 1;
  opacity: 0.75;
  color: #a7afb3;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
