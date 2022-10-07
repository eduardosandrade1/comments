<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <ItemText v-for="item in listItems" :itemsCommun="listItems"/>
  <button @click="additemsText" class="btn-primary">
    Novo
  </button>
</template>

<script>
import ItemText from './components/ItemText.vue';

export default {
  name: 'App',
  data(){
    return {
      listItems: []
    }
  },
  components: {
    ItemText,
  },
  methods: {
    additemsText() {
      this.listItems.push({
        class_name: 'green',
        input_value: 'teste'
      });
    }
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
.btn-primary {
    margin: 10px;
    font-size: 28px;
    width: 100px;
    height: 50px;
    padding: 5px;
    background: #0055ff;
    color: #fff;
    outline: none;
    border-radius: 4px;
    border: 1px solid transparent;
    transition: 0.5s;
}
.btn-primary:hover {
    background: #0055dd;
    box-shadow: 0 0 0 5px rgba(0, 85, 255, 0.5);
    color: #fff;
    transition: 0.5s;
}

</style>
