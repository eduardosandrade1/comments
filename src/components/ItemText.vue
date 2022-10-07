<template>
    <div class="item_commun_div">
        <div class="item_commun_item">
            <OptionsItem />
            <div class="input_item_div">
                <input name="" />
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

</style>