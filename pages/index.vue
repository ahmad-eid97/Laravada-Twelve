<template>
  <div class="home">
    <app-home-slider :slides="slides"></app-home-slider>
    <app-home-competence></app-home-competence>
    <app-home-contact></app-home-contact>
    <app-home-cases :services="services"></app-home-cases>
    <app-home-why :whyUs="whyUs"></app-home-why>
    <app-home-activities :activities="activities" />
    <app-home-steps :steps="steps" />
    <!-- <app-home-feature></app-home-feature>

        <app-home-services></app-home-services>
        <app-home-contact-divider></app-home-contact-divider>
        <app-home-principles></app-home-principles>
        <app-home-cases></app-home-cases>
        <app-home-achievements></app-home-achievements>
        <app-home-why></app-home-why>
        <app-home-blogs></app-home-blogs>
        <app-home-contact-divider-bottom></app-home-contact-divider-bottom> -->
    <app-home-testimonials :testimonials="testimonials"></app-home-testimonials>

    <!-- WHY WORK WITH US Start -->
    <!-- WHY WORK WITH US End -->

    <!-- testimonials Section Start -->
    <!-- testimonials Section End -->

    <!-- <app-home-news></app-home-news> -->

    <!-- Services Section Start -->
    <!-- <app-home-services-offers></app-home-services-offers> -->
  </div>
</template>

<script>
// import AppHomeAchievements from '../components/home/AppHomeAchievements.vue'
// import AppHomeBlogs from '../components/home/AppHomeBlogs.vue'
// import AppHomeCases from '../components/home/AppHomeCases.vue'
// import AppHomeContactDivider from '../components/home/AppHomeContactDivider.vue'
// import AppHomeContactDividerBottom from '../components/home/AppHomeContactDividerBottom.vue'
// import AppHomeFeature from '../components/home/AppHomeFeature.vue'
// import AppHomeNews from '../components/home/AppHomeNews.vue'
// import AppHomePrinciples from '../components/home/AppHomePrinciples.vue'
// import AppHomeServices from '../components/home/AppHomeServices.vue'
// import AppHomeServicesOffers from '../components/home/AppHomeServicesOffers.vue'
import AppHomeSlider from "../components/home/AppHomeSlider.vue";
import AppHomeCompetence from "../components/home/AppHomeCompetence.vue";
import AppHomeContact from "../components/home/AppHomeContact.vue";
import AppHomeCases from "../components/home/AppHomeCases.vue";
import AppHomeWhy from "../components/home/AppHomeWhy.vue";

import AppHomeTestimonials from "../components/home/AppHomeTestimonials.vue";
import AppHomeActivities from "../components/home/AppHomeActivities.vue";
import AppHomeSteps from "../components/home/AppHomeSteps.vue";
// import AppHomeWhy from '../components/home/AppHomeWhy.vue'
// @ is an alias to /src

export default {
  name: "Home",
  async asyncData({ $axios, app }) {
    const slides = await $axios.get("/sliders", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const testimonials = await $axios.get("/testimonials");

    const services = await $axios.get("/services");

    const whyUs = await $axios.get("/sections/why_choose_us", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    return {
      slides: slides.data.data.sliders,
      testimonials: testimonials.data.data.testimonials,
      services: services.data.data.services,
      whyUs: whyUs.data.data,
      activities: activities.data.data,
      steps: steps.data.data,
    };
  },
  components: {
    AppHomeSlider,
    AppHomeCompetence,
    AppHomeContact,
    AppHomeCases,
    AppHomeWhy,
    AppHomeTestimonials,
    AppHomeActivities,
    AppHomeSteps,
    // AppHomeFeature,
    // AppHomeBlogs,
    // AppHomeContactDivider,
    // AppHomeWhy,
    // AppHomeServices,
    // AppHomeNews,
    // AppHomeServicesOffers,
    // AppHomePrinciples,
    // AppHomeCases,
    // AppHomeAchievements,
    // AppHomeContactDividerBottom
  },
};
</script>
