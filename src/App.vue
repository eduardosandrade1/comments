<template>
  <div class="principal">
    <div class="edit-div">
      <button class="btn">
        <div class="edit-color" v-on:click="editColorBackground">
          edit
        </div>
      </button>
    </div>
    <img alt="Vue logo" src="./assets/logo.png">
    <ItemText v-for="item in listItems" :itemsCommun="listItems"/>
    <button @click="additemsText" class="btn-primary">
      Novo
    </button>
    <Modal v-bind:show="showModal" :inputs-props="inputsProps" :buttons-props="buttonsProps" />
  </div>

</template>

<script>
import ItemText from './components/ItemText.vue';
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  data(){
    return {
      listItems: [],
      inputsProps: [
        {
          type: 'color',
          class_name: '',
          name_input: 'value'
        },
        {
          type: 'number',
          class_name: 'strong',
          name_input: 'meu_primeiro_teste'
        },
      ],
      buttonsProps: [
        {
          text: 'aplicar',
          type: 'button'
        }
      ],
      showModal : false,
    }
  },
  components: {
    ItemText,
    Modal,
  },
  methods: {
    additemsText() {
      this.listItems.push({
        class_name: 'green',
        input_value: 'teste'
      });
    },
    editColorBackground() {
      if (this.showModal) {
        this.showModal = false;
      } else {
        this.showModal = true;
      }
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

.principal {
  width: 80vw;
  /* height: 80vh; */
  background-color: #2c3e50;
  margin: auto;
  border-radius: 5px;
}
</style>
