<template>
    <div>
        <button @click="go_go_snake()">Snake style</button>

        
        <p>{{now_snake}}</p>
    </div>
</template>

<script>


    export default {
        data() {
            return {
                current_snake: "",
                now_snake: ""
            }
        },
        methods: {
        update_snake(ii) {
            this.current_snake = ii
        },
        
        go_go_snake() {
            // converting spaces to underscore, then stored into variable now_nake
            for(let i = 0;i < this.current_snake.length;i++) {
                this.now_snake = this.current_snake.replaceAll(" ", "_")
            }

        }
       },
        mounted () {
            this.$root.$on(`new_joke`, this.update_snake)
        },

                
       
        
        name: 'snake-joke'
    }
</script>

<style scoped>

</style>