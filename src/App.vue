<template>
  <div id="app" :style="{backgroundColor}">
    <input type="text" v-model="text" @keydown.enter="backgroundColor = text">
    <suggestion-list :match="text" @click="color => backgroundColor = color" />
  </div>
</template>

<script>
import SuggestionList from '@/components/SuggestionList'

export default {
  name: 'App',
  components: {SuggestionList},
  data(){ return {
    text: "",
    backgroundColor: ""
  }},
}
</script>

<style lang="scss">
body, html, #app{ margin: 0; height: 100%;}
#app {

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 60px;
}
</style>
