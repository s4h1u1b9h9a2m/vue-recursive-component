<template>
  <div>
    <div>hello: {{val}}</div>
    <test :val="val + 1" v-if="toRender"/>
  </div>
</template>
<script>
import test from "./test.vue";
export default {
  name: "test",
  props: ['val'],
  components: {
    test
  },
  computed: {
    
    toRender() {
      return this.val < 4;
    }
  }
};
</script>

