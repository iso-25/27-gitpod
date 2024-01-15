<template>
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
</template>

<script>
import TitleH3 from "@/components/TitleH3.vue";
import DescGl from "@/components/DescGl.vue";
import ButtonUn from "@/components/ButtonUn.vue";

export default {
  name: "SectionThink",
  components: {
    TitleH3,
    DescGl,
    ButtonUn,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/Section3Think/SectionThink.scss";
</style>
