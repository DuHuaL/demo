<template>
  <div>
    <button>+</button>
    <input type="text" v-model="count" style="width: 50px">
    <button>-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
  props: ['count']
};
</script>

<style>

</style>
