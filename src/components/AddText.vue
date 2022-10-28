<template>
  <div>
    <input type="text" v-model="inputText" @change="addNewText" />
    <text-list :textList="filterText"></text-list>
  </div>
</template>

<script>
import TextList from "./TextList.vue";
import { ref, computed } from "vue";
export default {
  components: { TextList },
  setup() {
    const inputText = ref("");
    const arrText = ref([]);

    const filterText = computed(function () {
      return arrText.value.filter((txt) => txt != "React");
    });

    function addNewText() {
      arrText.value.push(inputText.value);
      inputText.value = "";
    }

    return {
      inputText: inputText,
      filterText: filterText,
      addNewText: addNewText,
    };
  },
};
</script>

<style>
</style>