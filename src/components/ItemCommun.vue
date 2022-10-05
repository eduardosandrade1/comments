<template>
    <div class="item_commun_div">
        <div class="item_commun_item" v-for="item in items">
            <div class="add_new_item" v-on:click="addNewItem">
                
            </div>
            <OptionsItem  v-on:click=""/>
            <div class="input_item_div">
                <input name="" v-model="input_value" v-bind:class="className" />
            </div>
        </div>
    </div>
</template>

<script>
    import OptionsItem from './components/OptionsItem.vue';

    export default {
        name: "ItemCommun",
        props: ["className", "inputValue"],
        data() {
            return {
                items : [
                    {
                        className: "",
                        input_value: ""
                    }
                ]
            },
            input_value : '',
            className: ''
        },
        components: {
            OptionsItem,
        }
    },
    methods: {
        addNewItem () {
            this.items.push({
                className: '', // get a class dynamic when he click
                input_value: this.input_value
            })
        }
    }
</script>

<style scoped>

</style>