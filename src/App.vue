<template>
  <div id="app">
    购物车：<br>
    <num :count="value" @numberchange="numchange"></num>
    {{value}}
    <hr>
    <com-a></com-a>
    <br>
    <com-b></com-b>
  </div>
</template>

<script>
import Num from '@/components/num';
import ComA from '@/components/sub/coma';
import ComB from '@/components/sub/comb';
export default {
  name: 'App',
  components: {
    Num,
    ComA,
    ComB
  },
  data() {
    return {
      value: 1
    };
  },
  methods: {
    numchange(num) {
      this.value = num;
    }
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
