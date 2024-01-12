<template>
  <div class="desc">{{ msg }}</div>
</template>

<script>
export default {
  name: "DescriptionGl",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
.desc {
  color: $color-txt-desc;
  font: $font-desc;

  @include desktop-small {
    font-size: 20rem;
  }
  @include tablet {
    font-size: 18rem;
  }
  @include mobile {
    font-size: 14rem;
  }
}
</style>
