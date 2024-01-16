<template>
  <HeaderBlock />
  <div class="container">
    <MainBlock />
  </div>
  <FooterBlock />
</template>

<script>
import HeaderBlock from "@/components/HeaderBlock/HeaderBlock.vue";
import MainBlock from "@/components/MainBlock/MainBlock.vue";
import FooterBlock from "@/components/FooterBlock/FooterBlock.vue";

export default {
  name: "HomePage",
  data() {
    return {
      isChecked: false,
    };
  },
  methods: {},
  components: { HeaderBlock, MainBlock, FooterBlock },
};
</script>

<style lang="scss">
.container {
  background: linear-gradient(
    180deg,
    rgba(249, 249, 249, 1) 0%,
    rgba(255, 239, 239, 0.8) 5%
    );
}
</style>
