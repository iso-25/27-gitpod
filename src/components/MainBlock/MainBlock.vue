<template>
  <div class="main">
    <SectionWelcome />

    <!-- project -->
    <div class="project">
      <TitleH2 msg="Select project," class="project__title" />
      <TitleH2 msg="check dependencies, checkout branch, view readme.txt, install tools, run build, run test,"
        class="project__subtitle" />
      <TitleH2 msg="start coding." class="project__title" />
    </div>

    <!-- think -->
    <div class="think">
      <div class="think__info">
        <div class="think__info-container">

          <TitleH3 msg="Think CI/CD for dev environments" class="think__info-title" />
          <DescGl
            msg="We invented prebuilds so application code, configuration and infrastructure can all be stored as machine-executable code in your git repositories and applied to dev environments automatically and continuously."
            class="think__info-desc" />
          <div class="think__info-btns">
            <ButtonUn url="/" txtBtn="More on prebuilds" class="think__btns btn-l" />
            <ButtonUn url="/" txtBtn="Documentation" class="think__btns btn-r" />
          </div>
        </div>
      </div>
      <div class="think__img">
        <div class="think__img-container">
          <img src="@/assets/think.png" alt="Think">
        </div>
      </div>
    </div>

    <!-- design -->
    <div class="design">
      <TitleH2 msg="Remote-first. Secure by design." class="design__title" />

      <DescGl
        msg="You no longer need an over-powered laptop to code, Gitpod works just as smoothly on a Chromebook or iPad. All you need is a browser. Gitpod centralizes all source code and never stores it on insecure machines and networks."
        class="design__desc" />

      <div class="design__btns">
        <BtnExtension url="/" imgName="design-chrome-btn.svg" txtBtn="Chrome Extension" />
        <BtnExtension url="/" imgName="design-firefox-btn.svg" txtBtn="Firefox  Extension" />
      </div>
    </div>
  </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";
import TitleH3 from "@/components/TitleH3.vue";
import SectionWelcome from "@/components/MainBlock/SectionWelcome/SectionWelcome.vue";
import BtnExtension from "@/components/BtnExtension/BtnExtension.vue";
import DescGl from "@/components/DescGl.vue";
import ButtonUn from "@/components/ButtonUn.vue";

export default {
  name: "MainBlock",
  components: {
    TitleH2,
    TitleH3,
    SectionWelcome,
    BtnExtension,
    DescGl,
    ButtonUn,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/MainBlock.scss";
</style>
