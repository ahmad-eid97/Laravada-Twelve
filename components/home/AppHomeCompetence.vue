<template>
  <section class="competence">
    <div class="row m-0">
      <h2>Our fields of competence</h2>
    </div>
    <div class="row m-0 justify-content-center">
      <div class="col-sm-6 col-lg-4">
        <div class="item">
          <font-awesome-icon icon="fa-solid fa-cloud-arrow-down" />
          <h4 class="">Software & automatisation</h4>
          <p>starting from <span>$999</span></p>
          <div class="row">
            <a href="#" class="btn col-auto"> Learn more </a>
          </div>
        </div>
      </div>
      <div class="col-sm-6 col-lg-4">
        <div class="item">
          <font-awesome-icon icon="fa-solid fa-box-archive" />
          <h4 class="">Business audit & analytics</h4>
          <p>starting from <span>$1509</span></p>
          <div class="row">
            <a href="#" class="btn col-auto"> Learn more </a>
          </div>
        </div>
      </div>
      <div class="col-sm-6 col-lg-4">
        <div class="item">
          <font-awesome-icon icon="fa-solid fa-user-check" />
          <h4 class="">Quality control management</h4>
          <p>starting from <span>$750</span></p>
          <div class="row">
            <a href="#" class="btn col-auto"> Learn more </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHomeCompetence",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.competence {
  margin: 0 0 60px;
  padding: 30px 60px;
}
@include xs {
  .competence {
    padding: 30px 20px;
  }
}
.competence h2 {
  color: rgb(0, 0, 0);
  font-size: 38px;
  font-weight: 400;
  line-height: 45.6px;
  margin-bottom: 60px;
  text-align: center;
}
.competence .item {
  align-content: center;
  align-items: center;
  border-radius: 8px;
  border: 2px solid #e2e9ef;
  display: block;
  flex-direction: row;
  flex-wrap: nowrap;
  font-size: 18px;
  height: 400px;
  margin-bottom: 30px;
  min-height: 400px;
  padding-bottom: 45px;
  padding-left: 30px;
  padding-right: 30px;
  padding-top: 45px;
  justify-content: center;
}
.competence .item svg {
  color: rgb(0, 206, 200);
  display: block;
  font-size: 48px;
  height: 48px;
  line-height: 48px;
  margin: 0 auto 40px;
  position: relative;
  text-align: center;
  width: 48px;
}
.competence .item h4 {
  color: rgb(0, 0, 0);
  font-size: 31px;
  font-weight: 400;
  line-height: 37.2px;
  text-align: center;
}
.competence .item p {
  color: rgb(94, 100, 107);
  font-size: 18px;
  font-weight: 400;
  line-height: 28.8px;
  margin-top: 20px;
  text-align: center;
}
.competence .item span {
  color: rgb(0, 206, 200);
  font-size: 18px;
  font-weight: 400;
  line-height: 28.8px;
  text-align: center;
}
.competence .item .btn {
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
  margin: 30px auto 0;
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
</style>
