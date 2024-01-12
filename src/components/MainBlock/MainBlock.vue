<template>
  <div class="main">
    <SectionWelcome />

    <!-- project -->
    <div class="project">
      <TitleH2 msg="Select project," class="project__title" />
      <TitleH2
        msg="check dependencies, checkout branch, view readme.txt, install tools, run build, run test,"
        class="project__subtitle"
      />
      <TitleH2 msg="start coding." class="project__title" />
    </div>

    <!-- design -->
    <div class="design">
      <TitleH2 msg="Remote-first. Secure by design." class="design__title" />
        
      <DescGl
        msg="You no longer need an over-powered laptop to code, Gitpod works just as smoothly on a Chromebook or iPad. All you need is a browser. Gitpod centralizes all source code and never stores it on insecure machines and networks."
        class="design__desc"
      />

      <div class="design__btns">
        <BtnExtension
          url="/"
          imgName="design-chrome-btn.svg"
          txtBtn="Chrome Extension"
        />
        <BtnExtension
          url="/"
          imgName="design-firefox-btn.svg"
          txtBtn="Firefox  Extension"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";
import SectionWelcome from "@/components/MainBlock/SectionWelcome/SectionWelcome.vue";
import BtnExtension from "@/components/BtnExtension/BtnExtension.vue";
import DescGl from "@/components/DescGl.vue";


export default {
  name: "MainBlock",
  components: {
    TitleH2,
    SectionWelcome,
    BtnExtension,
    DescGl,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/MainBlock.scss";
</style>
