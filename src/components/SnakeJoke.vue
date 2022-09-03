<template>
    <div>
        <button @click="go_go_snake()">Snake style</button>

        
        <p>{{now_loud}}</p>
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
            
            for(let i = 0;i < this.current_loud.length;i++) {
                if(((i+1) % 1=== 0) ) {
                    this.now_loud += this.current_loud[i].toUpperCase();
                }else{
                    this.now_loud += this.current_loud[i]
                }
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