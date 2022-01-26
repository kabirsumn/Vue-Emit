<template>
  <h2>
    <span class="log-in" @click="getBlock">Click here</span> to get the box
  </h2>
  <block v-show="showBlock" @close="showBlock = false" />
</template>

<script>
import Block from './components/Block.vue';
export default {
  name: 'App',
  components: { Block },

  data() {
    return {
      showBlock: false,
    };
  },

  methods: {
    getBlock() {
      this.showBlock = true;
    },
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

#app .log-in {
  background-color: #e0cdcd;
  color: #42ddaf;
  cursor: pointer;
  font-style: italic;
  font-weight: 600;
}
</style>
