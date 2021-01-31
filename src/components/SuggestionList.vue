<template>
  <ul>
    <li 
      v-for="color in colors" 
      :key="color"
      @click="$emit('click', color)"
    >{{color}}</li>
  </ul>
</template>

<script>
export default {
  props: ['match'],
  data(){ return {
    color: ['red','green','blue'] // Change this to a vuex getter that filters based on this.match
  }},
}
</script>

<style scoped lang="scss">
ul{
  position: absolute;
}
</style>