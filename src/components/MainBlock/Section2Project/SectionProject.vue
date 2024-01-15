<template>
    <div class="project">
      <TitleH2 msg="Select project," class="project__title" />
      <TitleH2 msg="check dependencies, checkout branch, view readme.txt, install tools, run build, run test,"
        class="project__subtitle" />
      <TitleH2 msg="start coding." class="project__title" />
    </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";

export default {
  name: "SectionProject",
  components: {
    TitleH2,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/Section2Project/SectionProject.scss";
</style>
