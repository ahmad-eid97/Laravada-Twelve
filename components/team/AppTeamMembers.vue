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
              <h6>
                {{ member.description.substring(0, 200) }}
                {{ member.description.length > 200 ? "..." : "" }}
              </h6>
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
  name: "AppTeamMembers",
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
.projects-col {
  text-align: center;
  margin-bottom: 40px;
}
.projects-col .card {
  text-align: center;
  margin-bottom: 40px;
  border: 2px solid #e2e9ef;
  -webkit-box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
  border-radius: 12px;
  cursor: pointer;
  transform: translateY(0px);
}

.projects-col .card:hover {
  transform: translateY(-15px);
  box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
  -webkit-box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
  -moz-box-shadow: 1px 19px 28px -10px rgba(13, 13, 13, 0.51);
}
.projects-col .thumb {
  margin-bottom: 18px;
  text-align: center;
  display: inline-block;
}
.projects-col .thumb img {
  border-radius: 12px 12px 0 0;
  width: 100%;
}
.projects-col .content {
  padding: 0 30px 30px;
}
.projects-col .content h4 {
  color: #3847d2;
  font-size: 20px;
  margin-bottom: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
}
.projects-col .content h5 {
  font-size: 16px;
  margin-bottom: 5px;
  letter-spacing: 1px;
  color: #05cfc9;
}
.projects-col .content h6 {
  color: #989898;
  font-family: Open Sans, sans-serif;
  font-size: 14px;
  text-transform: uppercase;
  margin-bottom: 15px;
  line-height: 28px;
  letter-spacing: 0.3px;
}
</style>
