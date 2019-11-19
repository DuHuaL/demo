<template>
  <div id="app">
    购物车：<br>
    <num :count="value"></num>
  </div>
</template>

<script>
import Num from '@/components/num';
export default {
  name: 'App',
  components: {
    Num
  },
  data() {
    return {
      value: 1
    };
  }
};
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
