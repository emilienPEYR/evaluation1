<template>
<div><label for="message">{{ msg }}</label></div>
<div><input type="date" v-model="message" /></div>
</template>

<script>
export default {
  name: "Inputday",
  props: {
    msg: String
  }, 
};
</script>

<style scoped>

</style>