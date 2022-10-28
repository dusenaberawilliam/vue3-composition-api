<template>
  <p>{{ greetings }}</p>
  <p>___________________</p>
  <p v-for="(txt, index) in textList" :key="index">
    {{ txt }}
  </p>
</template>

<script>
import { ref, watch, toRefs } from "vue";
export default {
  props: {
    textList: Array,
  },
  setup(props) {
    const greetings = ref("Hello! Type and hit enter");
    const { textList } = toRefs(props);

    watch(textList, (newValue, oldValue) => {
      console.log("old", oldValue);
      console.log("New", newValue);
    });

    return {
      greetings: greetings,
    };
  },
};
</script>

<style>
</style>