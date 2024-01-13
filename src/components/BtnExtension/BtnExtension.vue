<template>
  <div class="btn-ext">
    <a :href="url" class="btn-ext__link">
      <div class="btn-ext__btn-container">
        <div class="btn-ext__btn-border">
        </div>  
        <div class="btn-ext__btn">
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
