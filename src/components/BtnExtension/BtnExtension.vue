<template>
  <div class="btn">
    <a :href="url" class="btn__link">
      <div class="btn__btn-container">
        <div class="btn__btn-border">
        </div>  
        <div class="btn__btn">
          <img v-if="imgName" :src="require(`@/assets/${imgName}`)" :alt="txtBtn" />
          <div>{{ txtBtn }}</div>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "BtnExtension",
  props: {
    url: String,
    imgName: String,
    txtBtn: String,
  },
  };
</script>

<style lang="scss" scoped>
@import "@/components/BtnExtension/BtnExtension.scss";
</style>
