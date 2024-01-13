<template>
  <div class="title-h3">{{ msg }}</div>
</template>

<script>
export default {
  name: "TitleH3",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss">
.title-h3 {
  font: var(--font-title-h2);
}
</style>
