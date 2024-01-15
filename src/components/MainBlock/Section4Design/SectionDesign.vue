<template>
  <div class="design">
    <TitleH2 msg="Remote-first. Secure by design." class="design__title" />
    <div class="design__img">
      <img src="@/assets/design.png" alt="Design">
    </div>
    <DescGl
      msg="You no longer need an over-powered laptop to code, Gitpod works just as smoothly on a Chromebook or iPad. All you need is a browser. Gitpod centralizes all source code and never stores it on insecure machines and networks."
      class="design__desc" />
    <div class="design__btns">
      <BtnExtension url="/" imgName="design-chrome-btn.svg" txtBtn="Chrome Extension" />
      <BtnExtension url="/" imgName="design-firefox-btn.svg" txtBtn="Firefox  Extension" />
    </div>
  </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";
import DescGl from "@/components/DescGl.vue";
import BtnExtension from "@/components/BtnExtension/BtnExtension.vue";

export default {
  name: "SectionDesign",
  components: {
    TitleH2,
    BtnExtension,
    DescGl,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/Section4Design/SectionDesign.scss";
</style>
