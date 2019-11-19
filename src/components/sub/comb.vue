import vueObj from '../../utils/communication';
<template>
  <div>
    comb <br>
    {{numb}}
  </div>
</template>

<script>
import vueObj from '@/utils/communication';
export default {
  data() {
    return {
      numb: 0
    };
  },
  created() {
    vueObj.$on('change', (num) => {
      this.numb = num;
    });
  }
};
</script>

<style>

</style>
