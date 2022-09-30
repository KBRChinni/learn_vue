<template>
  <div><input type="text" :value="modelValue" /></div>
</template>

<script>
export default {
  name: "InputS",
  props: {
    modelValue: String,
  },
};
</script>

<style scoped>
input[type="text"] {
  background-color: #ffd969;
  border-color: #000;
}
</style>
