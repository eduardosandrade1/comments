<template>
    
   
</template>

<script>
    import ItemTextVue from './ItemText.vue';
    export default {
        data () {
            return {
                options: [
                    {
                        description: 'Colors',
                        class: [
                            'green',
                            'red',
                            'black',
                        ],    
                    },
                    {
                        description: '22',
                        class: [
                            ''
                        ],
                    }
                ]
            }
        },
        methods : {

        },
        components: {
            ItemTextVue,
        }
    }

</script>

<style scoped>

</style>