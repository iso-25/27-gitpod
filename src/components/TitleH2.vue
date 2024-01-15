<template>
  <div class="title-h2">{{ msg }}</div>
</template>

<script>
export default {
  name: "TitleH2",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss">
.title-h2 {
  font: var(--font-title-h2);
}
</style>
