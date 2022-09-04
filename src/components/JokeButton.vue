<template>
    <div>
        <button @click="get_joke">Get a new Joke</button>
    </div>
</template>

<script>
// stored the joke also in cookies also, was going to use that instead of emit. but running out of time.
import axios from "axios"
import Cookies from "vue-cookies"

    export default {
        methods: {
            get_joke() {
                
                axios.request({
                    url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`
                }).then((success)=>{

                        this.$root.$emit(`new_joke`, success.data[0]);
                        Cookies.set(`joke`, success.data[0])
                }).catch((error)=>{
                    error
                })
            }
        },
        name: 'joke-button'
    }
</script>

<style scoped>

</style>