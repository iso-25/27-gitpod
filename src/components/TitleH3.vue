<template>
  <div class="title">{{ msg }}</div>
</template>

<script>
export default {
  name: "TitleH3",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
.title {
  font: $font-title-h2;

  @include tablet {
    font-size: 30rem;
  }

  @include mobile {
    font-size: 26rem;
  }
}
</style>
