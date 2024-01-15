<template>
  <div class="start">
    <TitleH2 msg="Get started now" class="start__title" />
    <div class="start__container">
      <div class="start__blocks">
        <TitleH3 msg="Connect Git repository" class="start__repository-title" />
        <DescriptionGl msg="Select a Git provider to start with an existing project from any Git context."
          class="start__repository-desc" />
        <div class="start__rep-btns-container">
          <ButtonUn :classNames="['repository-btns', 'start__rep-btn-gitlab']" url="/" imgName="rep-gitlab.svg"
            txtBtn="Continue with GitLab" />
          <ButtonUn :classNames="['repository-btns', 'start__rep-btn-github']" url="/" imgName="rep-github.svg"
            txtBtn="Continue with GitHub" />
          <ButtonUn :classNames="['repository-btns', 'start__rep-btn-bitbucket']" url="/" imgName="rep-bitbucket.svg"
            txtBtn="Continue with Bitbucket" />
        </div>
        <DescriptionGl msg="Or prefix any GitLab, GitHub or Bitbucket URL with" class="start__repository-desc-pref" />
        <DescriptionGl msg="gitpod.io/#" class="start__repository-pref" />
      </div>
      <div class="start__blocks">
        <TitleH3 msg="Launch an example workspace" class="start__examlpes-title" />
        <DescriptionGl msg="Dive into one of our example workspaces" class="start__examlpes-desc" />
        <div class="start__examlpes-container">
          <div class="start__examlpe-item" v-for="(item, index) in  examlpes" :key="index">
            <div class="start__examlpe-logo-container">
              <img v-if="item.pathLogo" :src="require(`@/assets/${item.pathLogo}`)" :alt="item.nameWorkspace"
                class="start__examlpe-img" />
              <p class="start__examlpe-txt">{{ item.nameWorkspace }}</p>
            </div>
            <ButtonUn :classNames="['start__examlpe-btn']" :imgName="item.pathImgBtn" :url="item.urlBtn"
              :txtBtn="item.txtBtn" />

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";
import TitleH3 from "@/components/TitleH3.vue";
import DescriptionGl from "@/components/DescGl.vue";
import ButtonUn from "@/components/ButtonUn.vue";

export default {
  name: "SectionStart",
  components: {
    TitleH2,
    TitleH3,
    DescriptionGl,
    ButtonUn,
  },
  data() {
    const examlpes = [
      {
        pathLogo: "examplesImg/typescript.svg",
        nameWorkspace: "Node or TypeScript",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
      {
        pathLogo: "examplesImg/python.svg",
        nameWorkspace: "Python",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
      {
        pathLogo: "examplesImg/go.svg",
        nameWorkspace: "Go",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
      {
        pathLogo: "examplesImg/rust.svg",
        nameWorkspace: "Rust",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
      {
        pathLogo: "examplesImg/java.svg",
        nameWorkspace: "Java",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
      {
        pathLogo: "examplesImg/svelte.svg",
        nameWorkspace: "Svelte",
        pathImgBtn: "",
        altImgBtn: "",
        txtBtn: "Launch workspace",
        urlBtn: "/",
      },
    ];
    return {
      examlpes,
    };
  },
};
</script>

<style lang="scss">
@import "@/components/MainBlock/Section6Start/SectionStart.scss";
</style>
