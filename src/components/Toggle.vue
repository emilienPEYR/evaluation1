<template>
  <div>
    <div v-if="isShow"><Hello-world/></div>
    <button @click="isShow = !isShow">Cliquer ici</button>
  </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue';
export default {
  components: { HelloWorld },
  name: "ToggleDiv",
  data: function () {
    return {
      isShow: true,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>