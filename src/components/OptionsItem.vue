<template>
    <div class="fab-wrapper">
        <input id="fabCheckbox" type="checkbox" class="fab-checkbox" />
        <label class="fab" for="fabCheckbox">
            <span class="fab-dots fab-dots-1"></span>
            <span class="fab-dots fab-dots-2"></span>
            <span class="fab-dots fab-dots-3"></span>
        </label>
        <div class="fab-wheel">
            <a class="fab-action fab-action-1" @click="additem('input')">
                Txt
            </a>
            <a class="fab-action fab-action-2" @click="additem('banner')">
                Bn
            </a>
            <a class="fab-action fab-action-3">
                <i class="fas fa-address-book"></i>
            </a>
            <a class="fab-action fab-action-4">
            <i class="fas fa-info"></i>
            </a>
        </div>
      </div>
</template>

<script>
    import ItemTextVue from './Item.vue';
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
            additem(type) {
                this.$parent.additem(type);
            }
        },
        components: {
            ItemTextVue,
        }
    }

</script>

<style scoped>

</style>