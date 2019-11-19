import vueObj from '../../utils/communication';
<template>
  <div>
    coma <br>
    <input type="text" v-model="numa" @keyup="handlechange">
  </div>
</template>

<script>
import vueObj from '@/utils/communication';
export default {
  data() {
    return {
      numa: 1
    };
  },
  methods: {
    handlechange() {
      vueObj.$emit('change', this.numa);
    }
  }
};
</script>

<style>

</style>
