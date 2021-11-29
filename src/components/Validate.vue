<template>
<div><button v-on:click="$emit('validation')">Confirmer et continuer</button></div>
</template>

<script>
export default {
  name: "Competences",
  props: {
    msg: String
  }, 
};
</script>

<style scoped>

</style>