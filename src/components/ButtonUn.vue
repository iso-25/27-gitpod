<template>
    <a :href="url" class="btn-un__link">
      <div :class="[ 'btn-un__btn', Array.isArray(classNames) ? classNames.join(' ') : '' ]">
        <img v-if="imgName" :src="require(`@/assets/${imgName}`)" :alt="txtBtn" />
        <div>{{ txtBtn }}</div>
      </div>
    </a>
</template>

<script>
export default {
  name: "ButtonUn",
  props: {
    classNames: {
      type: Array,
      default: () => [],
      validator: (value) => {
        return value.every((item) => typeof item === 'string');
      },
    },
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
