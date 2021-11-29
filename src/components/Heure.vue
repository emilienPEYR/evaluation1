<template>
  <div id="heure">
    <input type="radio" name="heure" value="heure" v-on:click="$emit('validation')"/>
    <label for="dewey">{{ heure }}</label>
  </div>
</template>

<script>
export default {
  name: "Heure",
  props: {
    heure: String,
  },
};
</script>

<style scoped>
</style>