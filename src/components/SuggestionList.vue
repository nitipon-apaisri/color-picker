<template>
  <ul>
    <li v-for="color in colors" :key="color" @click="$emit('click', color)">
      {{ color }}
    </li>
  </ul>
</template>

<script>
export default {
  props: ["match"],
  computed: {
    colors() {
      return this.$store.getters.filterColors(this.match);
    },
  },
  methods: {},
};
</script>

<style scoped lang="scss">
ul {
  position: absolute;
}
</style>