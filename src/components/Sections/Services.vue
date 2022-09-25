<script setup>
import Typography from "../main/TypographyVue.vue";
import SpaceVue from "../main/SpaceVue.vue";
import ServiceContainer from "./Services/ServiceContainer.vue";

const services = [
  {
    title: "Front End Development",
    keywords: "HTML, CSS, JavaScript, React, Vue, Angular, Bootstrap, Tailwind",
    description:
      "I can build a beautiful and scalable SPA using HTML CSS and Javascript",
    icon: "mdi-monitor-dashboard",
  },
  {
    title: "Back End Development",
    keywords: "Node, Django, Redis, MongoDB, PostgreSQL",
    description:
      "I can design a beautiful and modern website using <b>Figma</b> and <b>Adobe XD</b>.",
    icon: "mdi-palette",
  },
  {
    title: "Full Stack Development",
    keywords: "Next.js, Nuxt.js, Laravel",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Content Creation",
    keywords: "Word, Excel, PowerPoint, Photoshop, Illustrator, Figma, XD",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Game Design",
    keywords: "Unity, C#, Blender, Maya, Photoshop, Illustrator, Figma, XD",
    description: "I can host your website on <b>Netlify</b> or <b>Heroku</b>.",
    icon: "mdi-server",
  },
  {
    title: "Lead Developer",
    keywords: "Agile, Scrum, Kanban, Jira, Trello, Git, GitHub, GitLab",
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
