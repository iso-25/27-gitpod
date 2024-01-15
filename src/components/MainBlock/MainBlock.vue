<template>
  <div class="main">
    <SectionWelcome />
    <SectionProject />
    <SectionThink />
    <SectionDesign />
    <SectionDevelopers />
    <SectionStart />
  </div>
</template>

<script>
import SectionWelcome from "@/components/MainBlock/Section1Welcome/SectionWelcome.vue";
import SectionProject from "@/components/MainBlock/Section2Project/SectionProject.vue"
import SectionThink from "@/components/MainBlock/Section3Think/SectionThink.vue";
import SectionDesign from "@/components/MainBlock/Section4Design/SectionDesign.vue";
import SectionDevelopers from "@/components/MainBlock/Section5Developers/SectionDevelopers.vue";
import SectionStart from "@/components/MainBlock/Section6Start/SectionStart.vue";

export default {
  name: "MainBlock",
  components: {
    SectionWelcome,
    SectionProject,
    SectionThink,
    SectionDesign,
    SectionDevelopers,
    SectionStart,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/MainBlock.scss";
</style>
