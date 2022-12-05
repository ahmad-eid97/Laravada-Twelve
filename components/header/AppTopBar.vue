<template>
  <div class="top-bar">
    <div class="row m-0">
      <div class="col-lg-12">
        <ul class="social-icon bordered-theme">
          <li>
            <span class="tel">
              <i class="fa-solid fa-phone"></i>
              +11111111111111
            </span>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-facebook"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-behance"></i></a>
          </li>
          <langSwitch></langSwitch>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import langSwitch from "../langSwitch/langSwitch.vue";
export default {
  name: "AppTopBar",
  components: {
    langSwitch,
  },
  data() {
    return {};
  },
  mounted() {},
  methods: {},
};
</script>
<style lang="scss">
.top-bar {
  padding: 20px 60px 0;
  height: 60px;
  transition: all 0.3s linear;
}
@include md {
  .top-bar {
    display: none;
  }
}
.top-bar .social-icon {
  list-style: none;
  padding: 0;
  display: flex;
  justify-content: end;
}
.top-bar .social-icon li {
  display: inline-block;
  margin-left: 6px;
}
.top-bar .social-icon li .tel {
  box-shadow: none;
  color: rgb(0, 0, 0);
  font-size: 18px;
  font-weight: 600;
  line-height: 18px;
  margin-right: 30px;
}
.top-bar .social-icon li .tel i {
  box-sizing: border-box;
  color: rgb(0, 206, 200);
  font-size: 18px;
  font-weight: 400;
  height: 18px;
  line-height: 18px;
  margin-right: 6px;
  position: relative;
  width: 18px;
}
.top-bar .social-icon li a {
  align-items: center;
  background-color: rgba(0, 206, 200, 0.14);
  border-radius: 50%;
  color: rgb(0, 206, 200);
  cursor: pointer;
  font-size: 14px;
  height: 28px;
  line-height: 14px;
  text-decoration-color: rgb(129, 138, 145);
  width: 28px;
  display: inline-flex;
  justify-content: center;
}
.top-bar .social-icon li a:hover {
  background-color: rgb(0, 206, 200);
  color: rgb(255, 255, 255);
}
</style>
