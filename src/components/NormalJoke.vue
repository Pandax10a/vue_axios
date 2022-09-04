<template>
    <div>
        <button @click="go_go_normal()">Normal and Simple</button>

        
        <p>{{now_normal}}</p>
    </div>
</template>

<script>


    export default {
        data() {
            return {
                current_normal: "",
                now_normal: ""
            }
        },
        methods: {
        update_normal(ii) {
            this.current_normal = ii
        },
        
        go_go_normal() {
           this.now_normal = this.current_normal

        }
       },
        mounted () {
            this.$root.$on(`new_joke`, this.update_normal)
        },

                
       
        
        name: 'normal-joke'
    }
</script>

<style scoped>

</style>