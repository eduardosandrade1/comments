<template>
    <div class="options_item">
        <ul>
            <li v-for="option in options"> 
                {{option.description}}
                <ul>
                    <li v-for="classe in option.class">
                        <button v-on:click="returnClassSelected"> {{classe}} </button>
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

        }
    }

</script>

<style scoped>

</style>