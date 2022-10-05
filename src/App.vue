<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Comments name-author="eduardo" />
  <ItemCommun  v-for="item in items" />
</template>

<script>
import Comments from './components/Comments.vue';
import ItemCommun from './components/ItemCommun.vue';

export default {
  name: 'App',
  components: {
    Comments,
    ItemCommun,
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
