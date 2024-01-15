<template>
  <div class="developers">
    <TitleH2 msg="Used by 400,000+ developers." class="developers__title" />

    <div class="swiper-container">
      <swiper class="swiper" :direction="'vertical'" :spaceBetween="14" :slidesPerView="1" :breakpoints="{
        768: {
          direction: 'horizontal',
          spaceBetween: 24,
          slidesPerView: 1, //If slidesPerView: 4, then all 4 slides fit on the entire screen
          width: 384        //Because slidesPerView: 1
        }
      }" @swiper="onSwiper" @slideChange="onSlideChange">
        <swiper-slide class="swiper-slide" v-for="(item, index) in  developers" :key="index">
          <SlideDeveloper :txtInfo="item.txtInfo" :nameDev="item.nameDev" :roleDev="item.roleDev" :tagsDev="item.tagsDev"
            :imgName="item.imgName" />
        </swiper-slide>
      </swiper>
    </div>

    <div class="developers__logos">
      <div class="developers__logo-item" v-for="(item, index) in  logos" :key="index">
        <img src="" alt="">
        <img v-if="item.imgName" :src="require(`@/assets/devLogosImgs/${item.imgName}`)" :alt="item.name" />
      </div>
    </div>
  </div>
</template>

<script>
import TitleH2 from "@/components/TitleH2.vue";
import SlideDeveloper from "@/components/MainBlock/Section5Developers/SlideDeveloper/SlideDeveloper.vue";
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

export default {
  name: "MainBlock",
  components: {
    TitleH2,
    SlideDeveloper,
    Swiper,
    SwiperSlide,
  },
  data() {
    const logos = [
      {
        imgName: "001.svg",
        name: "GitLab"
      },
      {
        imgName: "002.svg",
        name: "freeCodeCamp"
      },
      {
        imgName: "003.svg",
        name: "D-WAVE"
      },
      {
        imgName: "004.svg",
        name: "Google"
      },
      {
        imgName: "005.svg",
        name: "amazom"
      },
      {
        imgName: "006.svg",
        name: "facebook"
      },
      {
        imgName: "007.svg",
        name: "Uber"
      },
      {
        imgName: "008.svg",
        name: "OpenAI"
      },
      {
        imgName: "009.svg",
        name: "intel"
      },
      {
        imgName: "010.svg",
        name: "THEAI"
      },
      {
        imgName: "011.svg",
        name: "code"
      },
      {
        imgName: "012.svg",
        name: "4Geeks"
      },
    ];
    const developers = [
      {
        imgName: "001.jpg",
        txtInfo: ["GitPod is incredibly cool.",
          "In my opinion, this is a big step in open source software contribution. I'm excited to see where we go from here."],
        nameDev: "Ben Halpern",
        roleDev: "Creator and Co-founder",
        tagsDev: [
          { tag: "@forem", url: "/" },
          { tag: "@ThePracticalDev", url: "/" }
        ],
      },
      {
        imgName: "002.jpg",
        txtInfo: ["Let's say we were overwhelmed how smooth @gitpod workspaces creation & own Docker image for workspaces worked.",
          "Plus, installing @code extensions from the store and integrating @gitlab CI. That blew my mind entirely, and that is hard ;)"],
        nameDev: "Michael Friedrich",
        roleDev: "Developer Evangelist",
        tagsDev: [{ tag: "@GitLab", url: "/" }],
      },
      {
        imgName: "003.jpg",
        txtInfo: ["Look at any PR (pull request) in a full coding environment where you can edit, build, and test the PR code, by just prepending \"gitpod.io#\" to the PR URL. Super useful for reviewing/testing stuff without having to check it out locally!"],
        nameDev: "Julius Volz",
        roleDev: "Creator",
        tagsDev: [{ tag: "@PrometheusIO", url: "/" }],
      },
      {
        imgName: "004.jpg",
        txtInfo: ["I think I’m in love with @gitpod. It’s such a powerful tool. I’ve learned so much in the past week just from stumbling across Github repos that interest me and appending “http://gitpod.io/#” to the URL. A+ tool all around."],
        nameDev: "David Ressler",
        roleDev: "Engineering Manager",
        tagsDev: [{ tag: "@instagram", url: "/" }],
      },
      {
        imgName: "005.jpg",
        txtInfo: ["Wow - @gitpod is a brilliant way of evaluating a framework without installing anything.",
          "Launch gitpod for @vaadin at https://vaadin.com/start/v14 (\"Online workspace\" tab). You'll have app running and will be editing code in 3min from clicking \"Launch\" button."],
        nameDev: "Joonas Lehtinen",
        roleDev: "Co-founder",
        tagsDev: [{ tag: "@vaadin", url: "/" }],
      },
      {
        imgName: "006.jpg",
        txtInfo: ["Today is a great day, we added the @gitpod support to the @golo_lang repository. So now you can start hacking @golo_lang in almost only one click. Enjoy 🎉",
          "gitpod.io/#https://githu..."],
        nameDev: "Senior Enterprise Geek",
        roleDev: "Senior Technical Account Manager",
        tagsDev: [{ tag: "@GitLab", url: "/" }],
      },
      {
        imgName: "007.jpg",
        txtInfo: ["This @gitpod thing is magic! Pretty cool, without any extra configuration. Good work!",
          "https://gitpod.io/#https://github.com/thanos-io/thanos"],
        nameDev: "Bartłomiej Płotka",
        roleDev: "Principal Software Engineer",
        tagsDev: [],
      },
      {
        imgName: "008.jpg",
        txtInfo: ["Ya'all @gitpod is freaking amazing! We integrated it into our workflow for working on @freeCodeCamp's codebase and I am honestly loving it. 🔥🔥!",
          "Go check it out on our repo https://github.com/freeCodeCamp/f... now!"],
        nameDev: "Mrugesh Mohapatra",
        roleDev: "Technology & Community",
        tagsDev: [{ tag: "@freeCodeCamp", url: "/" }],
      },
      {
        imgName: "009.jpg",
        txtInfo: ["I'm really enjoying @gitpod - for me, it's made full-stack development in the browser (yes,including mobile) a reality"],
        nameDev: "Jonathan Lister Parsons",
        roleDev: "CTO",
        tagsDev: [{ tag: "@PensionBee", url: "/" }],
      },
      {
        imgName: "010.jpg",
        txtInfo: ["Have to say that @gitpod is just super nice to use. Very impressed by the performance!"],
        nameDev: "ROKU",
        roleDev: "Engineering Manager",
        tagsDev: [{ tag: "@GitLab", url: "/" }],
      },
      {
        imgName: "011.jpg",
        txtInfo: ["Can only agree, opening a GitLab repository in gitpod is a magical experience, thanks for the integration @gitpod!"],
        nameDev: "Marcel van Remmerden",
        roleDev: "Product Design Manager",
        tagsDev: [{ tag: "@GitLab", url: "/" }],
      },
      {
        imgName: "012.jpg",
        txtInfo: ["Now contributing to @gitlab is a cakewalk with @gitpod 🎉!",
          "Already started my game! #100DaysOfCode"],
        nameDev: "Yo",
        roleDev: "Creator",
        tagsDev: [{ tag: "@Taskord", url: "/" }],
      },
      {
        imgName: "013.jpg",
        txtInfo: ["My setup is on @gitpod, just like Christopher McCandless, where I go my code goes with me, no setup whatsoever Smiling face with sunglasses 😎 #IntoTheWild"],
        nameDev: "Alejandro",
        roleDev: "Co-Founder",
        tagsDev: [{ tag: "@4GeeksAcademy", url: "/" }],
      },
      {
        imgName: "014.jpg",
        txtInfo: ["I just discovered the @gitlab @gitpod integration is alive on http://GitLab.com (released in 13.4 behind a feature flag). And it's AMAZING https://docs.gitlab.com/ee/integration.... .",
          "Now I can code from *anywhere*"],
        nameDev: "Brendan O’Leary",
        roleDev: "Dev. Evangelist",
        tagsDev: [{ tag: "@GitLab", url: "/" }],
      },
      {
        imgName: "015.jpg",
        txtInfo: ["Huge time saver, less frustrations for devs: Automated ready-to-code dev environments with pre-build workspaces. #gitpod #cloudide"],
        nameDev: "Sven Peters",
        roleDev: "Dev Advocate",
        tagsDev: [{ tag: "@MongoDB", url: "/" }],
      },
      {
        imgName: "016.jpg",
        txtInfo: ["I've been playing around with the \"next generation\" of Cloud IDEs lately, and @gitpodio is quickly emerging as one of the best 👨‍💻",
          "Awesome @github integration, slick Chrome extension, and super fast 🚀 https://gitpod.io/index.html"],
        nameDev: "Hugh Durkin",
        roleDev: "Platform Ecosystem",
        tagsDev: [{ tag: "@HubSpot", url: "/" }],
      },
    ];
    return {
      developers,
      logos,
    };
  },

  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      onSwiper,
      onSlideChange,
    };
  },
};
</script>

<style lang="scss" scoped>@import "@/components/MainBlock/Section5Developers/SectionDevelopers.scss";</style>
