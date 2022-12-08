<template>
  <div class="team-area pt-100 pb-70">
    <div class="container">
      <div class="section-title text-center">
        <span class="sp-color2">Our Team</span>
        <h2>Our Team Members</h2>
      </div>
      <div class="row pt-45" v-if="team.teams.length >= 1">
        <div
          v-for="member in team.teams"
          :key="member.id"
          class="col-sm-6 col-md-4 projects-col"
        >
          <div class="card">
            <div class="thumb">
              <img :src="member.image" alt="" />
              <div class="rollover"></div>
            </div>
            <div class="content">
              <h4>{{ member.name }}</h4>
              <h5>{{ member.job }}</h5>
              <h6>{{ member.description }}</h6>
              <h5>{{ member.phone }}</h5>
              <h5>{{ member.email }}</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppTestimonialsTeam",
  props: ["team"],
};
</script>

<style>
.team-area .section-title {
  margin-bottom: 0;
}
.team-area .section-title span {
  color: rgb(0, 206, 200);
  font-size: 20px;
  font-weight: 400;
  line-height: 33.8px;
  margin-bottom: 10px;
}
.team-area .section-title h2 {
  color: #000;
  font-size: 40px;
  font-weight: 400;
  line-height: 50.6px;
  margin-bottom: 30px;
  text-align: center;
}
.team-area .section-title .seprator img {
  width: 70px;
  margin-top: 5px;
  margin-bottom: 20px;
}
.thumb img {
  height: 250px;
}
</style>
