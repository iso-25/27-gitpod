<template>
  <div class="title">{{ msg }}</div>
</template>

<script>
export default {
  name: "TitleH1",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
.title {
  font: $font-title-h1;

  @include desktop-small {
    font-size: 60rem;
  }

  @include tablet {
    font-size: 40rem;
  }

  @include mobile {
    font-size: 45rem;
  }
}
</style>
