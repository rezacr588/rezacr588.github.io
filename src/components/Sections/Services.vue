<script setup>
import Typography from "../main/TypographyVue.vue";
import SpaceVue from "../main/SpaceVue.vue";
import ServiceContainer from "./Services/ServiceContainer.vue";

const services = [
  {
    title: "Front End Development",
    description:
      "I can build a beautiful and scalable SPA using <b>HTML</b>, <b>CSS</b> and <b>Vue.js</b>.",
    icon: "mdi-monitor-dashboard",
  },
  {
    title: "Back End Development",
    description:
      "I can design a beautiful and modern website using <b>Figma</b> and <b>Adobe XD</b>.",
    icon: "mdi-palette",
  },
  {
    title: "Full Stack Development",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Content Creation",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Game Design",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Lead Developer",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
];
</script>
<template>
  <section id="services">
    <Typography component="h2" color="#2B2B2B"> Services </Typography>
    <SpaceVue />
    <Typography component="p" color="#767676">
      I have a lot of experience in building different kind of applications.
      <br />
      Thier scope were from small to large scale applications. <br />
      I have worked with different technologies and frameworks.
    </Typography>
    <SpaceVue size="2rem" />
    <ServiceContainer :services="services" />
  </section>
</template>
<style scoped>
section {
  margin: 70px auto;
  text-align: center;
}
</style>
