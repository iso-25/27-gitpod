<template>
  <!-- <div class="btn-un"> -->
    <a :href="url" class="btn-un__link">
      <div class="btn-un__btn">
        <img v-if="imgName" :src="require(`@/assets/${imgName}`)" :alt="txtBtn" />
        <div>{{ txtBtn }}</div>
      </div>
    </a>
  <!-- </div> -->
</template>

<script>
export default {
  name: "ButtonUn",
  props: {
    url: String,
    imgName: String,
    txtBtn: String,
  },
};
</script>

<style lang="scss" scoped>
.btn-un__link {
  font: var(--font-btns);
  cursor: pointer;
  transition: var(--transition-btn);

  &:hover{
    transform: var(--transform-btn);
    box-shadow: 0rem 2rem 10rem $color-text-primary;    
  }
}
</style>
