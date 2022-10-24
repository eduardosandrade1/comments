<template>
    <div class="item_commun_div">
        <div class="item_commun_item">
            <div class="input_item_div" v-if="type.trim() == 'input'">
                <input :value="value"  placeholder="Type here" />
            </div>
            <div class="input_item_div" v-if="type.trim() == 'banner'">
                {{ type.trim() == 'banner' }}
                <img alt="{{alt}}">
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        name: "ItemText",
        props: ['itemsCommun', 'type', 'path', 'alt', 'value'],
        type: '',
        data() {
            return {
                
            }
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