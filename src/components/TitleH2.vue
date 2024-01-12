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
  font: $font-title-h2;

  @include desktop-small {
    font-size: 50rem;
  }

  @include tablet {
    font-size: 45rem;
  }

  @include mobile {
    font-size: 40rem;
  }
}
</style>
