<template>
  <div class="desc-gl">{{ msg }}</div>
</template>

<script>
export default {
  name: "DescriptionGl",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss">
.desc-gl {
  color: $color-txt-desc;
  font: var(--font-desc);
}
</style>
