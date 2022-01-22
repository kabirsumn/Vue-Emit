<template>
  <h2>You Must <span class="log-in">Log in</span></h2>
  <block />
</template>

<script>
import Block from './components/Block.vue';
export default {
  name: 'App',
  components: { Block },
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

#app .log-in {
  color: #42ddaf;
  cursor: pointer;
  font-style: italic;
  font-weight: 600;
}
</style>
