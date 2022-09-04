<template>
    <div>
        <button @click="go_go_loud()">Make it Loud!!!</button>

        
        <p>{{now_loud}}</p>
    </div>
</template>

<script>


    export default {
        data() {
            return {
                current_loud: "",
                now_loud: ""
            }
        },
        methods: {
        update_loud(ii) {
            this.current_loud = ii
        },
        // changing the value after modulo will change which character will be caps
        
        go_go_loud() {
            this.now_loud = this.current_loud.toUpperCase() + ' !!!!!!!!'

            // wanted to have more control which letter was applied caps but it repeated itself on each button click
            // for(let i = 0;i < this.current_loud.length;i++) {

                
            //     // if(((i+1) % 1=== 0) ) {
            //     //     this.now_loud += this.current_loud[i].toUpperCase();
            //     // }else{
            //     //     this.now_loud += this.current_loud[i]
            //     // }
            // }

        }
       },
        mounted () {
            this.$root.$on(`new_joke`, this.update_loud)
        },

                
       
        
        name: 'loud-joke'
    }
</script>

<style scoped>

</style>