<template>
  <div class="dev">
    <rezume class="dev__info-container">
      <p class="dev__info" v-for="(txt, txtIndex) in txtInfo" :key="txtIndex">{{ txt }}</p>
    </rezume>
    <div class="dev__name-container">
      <avatar class="dev__img" v-if="imgName">
        <img v-if="imgName" :src="require(`@/assets/devImgs/${imgName}`)" :alt="nameDev" />
      </avatar>
      <div class="dev__name-info">
        <name class="dev__name">{{ nameDev }}</name>
        <p>
          <role class="dev__role">{{ roleDev }}</role>
          <a class="dev__tag" v-for="(tagDev, tagIndex) in tagsDev" :key="tagIndex" :href="tagDev.url">
            <span class="dev__tag-span" v-if="tagIndex > 0">{{ (tagIndex > 0) ? ' and ' : '' }}</span>
            {{  tagDev.tag }} </a>
          </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SlideDeveloper",
  props: {
    txtInfo: {
      type: Array,
      default: () => [],
      validator: (value) => {
        return value.every((item) => typeof item === 'string');
      },
    },
    nameDev: String,
    roleDev: String,
    tagsDev: {
      type: Array,
      default: () => [],
      validator: (tags) => {
        if (!Array.isArray(tags)) {
          return false;
        }
        return tags.every((tagDev) => {
          return (
            tagDev &&
            typeof tagDev.tag === "string" &&
            typeof tagDev.url === "string"
          );
        });
      },
    },
    imgName: String,
  },
};
</script>

<style lang="scss" scoped>
@import "@/components/MainBlock/Section5Developers/SlideDeveloper/SlideDeveloper.scss";
</style>
