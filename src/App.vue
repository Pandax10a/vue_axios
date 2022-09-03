<template>
  <div id="app">
    <joke-button></joke-button>
    <br>
    <loud-joke></loud-joke>
    
    <snake-joke></snake-joke>
  </div>
</template>

<script>
import JokeButton from '@/components/JokeButton.vue';
import LoudJoke from '@/components/LoudJoke.vue';
import SnakeJoke from '@/components/SnakeJoke.vue';

export default {
  components: {
    JokeButton,
    LoudJoke,
    SnakeJoke
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
