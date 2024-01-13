<template>
  <div class="title-h1">{{ msg }}</div>
</template>

<script>
export default {
  name: "TitleH1",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss">
.title-h1 {
  font: var(--font-title-h1);
}
</style>
