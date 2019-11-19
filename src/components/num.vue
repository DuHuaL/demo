<template>
  <div>
    <button @click="numadd">+</button>
    <input type="text" v-model="num" style="width: 50px">
    <button @click="numsub">-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0
    };
  },
  props: ['count'],
  created() {
    this.num = this.count;
  },
  methods: {
    numadd() {
      this.num++;
      // 触发一个自定事件, vue提供了一套自定义事件机制
      // 给当前组件增加一个事件
      this.$emit('numberchange', this.num);// 多个数据传入一个对象
    },
    numsub() {
      this.num--;
      if (this.num <= 0) {
        this.num = 0;
      }
      this.$emit('numberchange', this.num);// 多个数据传入一个对象
    }
  }
};
</script>

<style>

</style>
