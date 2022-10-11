<template>
    <div id="{{idModal}}" class="modal">
        <!-- Modal content -->
        <div class="modal-content">
            <span class="close">&times;</span>
            <p>
                <input v-for="input in inputsProps" :type="input.type" :class="input.class_name" v-model="name_input" :placeholder="input.placeholder" />
                <button v-for="button in buttonsProps" :type="button.type">{{button.text}}</button>
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Modal",
        props: ['contentModal', 'idModal', 'show', 'inputsProps', 'buttonsProps'],
        data() {
            return {

            }
        },
        watch: {
            show: function (val) {
                let modal = document.getElementsByClassName('modal')[0]

                if (val) {
                    modal.style.display = 'block';
                } else {
                    modal.style.display = 'none';
                }
            },

        }
    }
</script>

<style scoped>
    /* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

/* Modal Content/Box */
.modal-content {
  background-color: #fefefe;
  margin: 15% auto; /* 15% from the top and centered */
  padding: 20px;
  border: 1px solid #888;
  width: 80%; /* Could be more or less, depending on screen size */
}

/* The Close Button */
.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}
</style>