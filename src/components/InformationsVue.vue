<script setup>
import CircledImageVueVue from "./CircledImageVue.vue";
import TypographyVue from "./main/TypographyVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
import IconVue from "./main/IconVue.vue";
import SidebarSectionVue from "./main/SidebarSectionVue.vue";
import ProgressVue from "./main/ProgressVue.vue";
import ExtraSkills from "./ExtraSkills.vue";
import ButtonVue from "./main/ButtonVue.vue";
</script>

<template>
  <section>
    <CircledImageVueVue />
    <SpaceVue scope="block" size="16px" />
    <TypographyVue component="h4">Reza Zeraat</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <TypographyVue color="#767676" component="p">
      Full Stack Developer
    </TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <div class="row">
      <IconVue name="facebook" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="instagram" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="twitter" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="linkedin" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="youtube" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="dribbble" active="true"></IconVue>
    </div>
    <hr />
    <div>
      <div class="item" v-for="data in items" :key="data.id">
        <div class="key">
          <TypographyVue component="p">{{ data.key + ":" }}</TypographyVue>
        </div>
        <div class="value">
          <TypographyVue component="p" color="data.color">
            {{ data.value }}
          </TypographyVue>
        </div>
      </div>
    </div>
    <hr />
    <SidebarSectionVue title="Languages">
      <ProgressVue :list="languages" />
    </SidebarSectionVue>
    <hr />
    <SidebarSectionVue title="Skills">
      <ProgressVue :list="skills" />
    </SidebarSectionVue>
    <hr />
    <SidebarSectionVue title="Extra Skills">
      <ExtraSkills :extraSkills="extraSkills" />
    </SidebarSectionVue>
    <hr />
    <ButtonVue>
      <TypographyVue component="h4"> Download CV </TypographyVue>
      <IconVue name="Download" active="true" />
    </ButtonVue>
    <SpaceVue scope="block" size="12px" />
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      items: [
        { id: 1, key: "Age", value: 25 },
        { id: 2, key: "Residence", value: "Turkey" },
        { id: 3, key: "Freelance", value: "Available", color: "#7EB942" },
        { id: 4, key: "Address", value: "Duzce, Konuralp" },
      ],
      languages: [
        { id: 1, key: "Persion", value: 100 },
        { id: 2, key: "English", value: 80 },
        { id: 3, key: "Turkish", value: 70 },
        { id: 4, key: "Arabic", value: 50 },
      ],
      skills: [
        { id: 1, key: "React", value: 95 },
        { id: 2, key: "Node.js", value: 85 },
        { id: 3, key: "MongoDB", value: 76 },
        { id: 4, key: "Postgresql", value: 90 },
        { id: 5, key: "JavaScript", value: 90 },
        { id: 6, key: "Typescript", value: 90 },
        { id: 7, key: "AWS", value: 60 },
        { id: 8, key: "Python", value: 70 },
        { id: 9, key: "Java", value: 50 },
      ],
      extraSkills: [
        { id: 1, text: "Next.js, Redux" },
        { id: 2, text: "Nestjs, Laravel" },
        { id: 3, text: "React Native, Flutter" },
        { id: 4, text: "Git, Gitlab, Jira" },
      ],
    };
  },
};
</script>

<style scoped>
section {
  background-color: white;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 2rem;
}

.row {
  display: flex;
}
hr {
  width: 80%;
  height: 1px;
  background-color: #f0f0f6;
  border: none;
  margin: 1.5rem auto;
}
.key {
  background: #ffb400;
  padding: 3px;
}

.item {
  display: flex;
  justify-content: space-between;
  margin: 1rem 0;
}
</style>
