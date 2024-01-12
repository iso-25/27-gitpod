<template>
  <div class="welcome">
    <div class="welcome__info">
      <TitleH1 msg="Always" class="welcome__info-title" />
      <TitleH1 msg="Ready to Code." class="welcome__info-title" />
      <DescGl
        msg="Spin up fresh, automated dev environments for each task, in the cloud, in seconds."
        class="welcome__info-desc"
      />
      <div class="welcome__workspace">
        <a href="/">
          <div class="welcome__workspace-btn">Try Now</div>
        </a>
        <div class="welcome__workspace-btn-info">
          <p>Open a workspace.</p>
          <p>Start from any Git context.</p>
        </div>
      </div>
      <div class="welcome__social">
        <a href="/" class="welcome__social-link">
          <img src="@/assets/welcome-gitlab.svg" alt="gitlab" />
        </a>
        <a href="/" class="welcome__social-link">
          <img src="@/assets/welcome-github.svg" alt="github" />
        </a>
        <a href="/" class="welcome__social-link">
          <img src="@/assets/welcome-bitbucket.svg" alt="bitbucket" />
        </a>
      </div>
    </div>
    <div class="welcome__img">
      <img src="@/assets/welcome.svg" alt="Welcome" />
    </div>
  </div>
</template>

<script>
import TitleH1 from "@/components/TitleH1.vue";
import DescGl from "@/components/DescGl.vue";

export default {
  name: "SectionWelcome",
  components: {
    TitleH1,
    DescGl,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/SectionWelcome/SectionWelcome.scss";
</style>
