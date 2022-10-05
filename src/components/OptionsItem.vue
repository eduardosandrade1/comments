<template>
    <div class="options_item">
        <ul>
            <li v-for="option in options"> {{option.description}}
                <ul>
                    <li v-for="class in option.class">
                        <button v-on:click="returnClassSelected"> {{class}} </button>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<script>

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
                        description: '',
                        class: [
                            ''
                        ],
                    }
                ]
            }
        },
        methods : {
            returnClassSelected (event) {
                // return prop from element and add in potions
            }
        }
    }

</script>

<style scoped>

</style>