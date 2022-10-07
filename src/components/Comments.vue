<!-- <template>
    <div class="comments">
        <input type="text" v-model="author_name" /><br>
        <textarea v-model="description"></textarea><br>
        <button v-on:click="addComment">Adicionar</button><br><br>
        <div class="item__comment__group" v-for="comment in items">
            <div class="item__comment__item">
                <hr>
                <span class="name_author_div">
                    Autor: {{comment.name}}
                </span>
                <p>
                    <span>Commentario:</span><br>

                    {{comment.description}}
                </p>
                <hr>
            </div>
        </div>        
    </div>
</template>

<script>
    export default {
        name: "Comments",
        data() {
            return {
                items : [
                    {
                        name: "Eduardo dev",
                        description : "My first app in VueJs"
                    }
                ],
                author_name: '',
                description: '',
            }
        },
        methods : {

            addComment() {
                this.items.push(
                    {
                        name: this.author_name,
                        description: this.description,
                    }
                )
                this.author_name = '';
                this.description = '';
            }

        }
    }
</script>

<style scoped>

</style> -->