<template>
    <div class="item_commun_div">
        <div class="item_commun_item">
            <!-- <OptionsItem /> -->
            <div class="input_item_div">
                <input name="" placeholder="Type here" />
            </div>
        </div>
    </div>
</template>

<script>
    import OptionsItem from './OptionsItem.vue';

    export default {
        name: "ItemText",
        props: ['itemsCommun'],
        data() {
            return {
               
            }
        },
        components: {
            OptionsItem,
        },
        // methods: {
        //     addNewItem () {
        //         this.items.push({
        //             className: '', // get a class dynamic when he click
        //             inputValue: this.input_value
        //         })
        //     }
        // }
    }
</script>

<style scoped>
    .input_item_div input{
        font-size:  20pt;
        width: 80%;
        margin: 5px 2px;
        outline:none;
        box-shadow: none;
        border: none;
    }
    
</style>