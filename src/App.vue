<template>
  <Inputday msg="Selectioner un jour" />
  <br />
  <Inputheure msg="Selectioner une heure" />
  <div id="heures">
    <Heure heure="12:00" v-on:validation="step = 'step1'" /><Heure
      heure="12:30"
      v-on:validation="step = 'step1'"
    /><Heure heure="13:00" v-on:validation="step = 'step4'" /><Heure
      heure="13:30"
      v-on:validation="step = 'step4'"
    /><Heure
      heure="14:00"
      class="prime"
      v-on:validation="step = 'step4'"
    /><Heure
      heure="14:30"
      class="prime"
      v-on:validation="step = 'step4'"
    /><Heure
      heure="15:00"
      class="prime"
      v-on:validation="step = 'step4'"
    /><Heure heure="15:30" v-on:validation="step = 'step4'" /><Heure
      heure="16:00"
      v-on:validation="step = 'step1'"
    /><Heure heure="16:30" v-on:validation="step = 'step1'" />
    <Heure heure="17:00" v-on:validation="step = 'step1'" /><Heure
      heure="17:30"
      v-on:validation="step = 'step4'"
    /><Heure
      heure="18:00"
      class="premium"
      v-on:validation="step = 'step4'"
    /><Heure
      heure="18:30"
      class="premium"
      v-on:validation="step = 'step1'"
    /><Heure
      heure="19:00"
      class="premium"
      v-on:validation="step = 'step4'"
    /><Heure heure="19:30" class="premium" v-on:validation="step = 'step1'" />
  </div>
  <Info />
  <div v-if="step === 'step1'">
    <h1 id="green">L'horaire est disponible !</h1>
    <Validate v-on:validation="step = 'step2'" />
  </div>
  <div v-if="step === 'step2'">
    <h1>Votre demande est accepté bravo !</h1>
    <style></style>
  </div>
  <div v-if="step === 'step0'">
    <h2 id="error">Veuillez choisir une horaire</h2>
  </div>
  <div v-if="step === 'step4'">
    <h2 id="notdisponible">Cette horaire n'est pas disponible</h2>
  </div>
</template>

<script>
import Inputday from "./components/Inputday.vue";
import Inputheure from "./components/Inputheure.vue";
import Heure from "./components/Heure.vue";
import Info from "./components/Info.vue";
import Validate from "./components/Validate.vue";

export default {
  name: "App",
  components: {
    Inputday,
    Inputheure,
    Heure,
    Info,
    Validate,
  },
  data() {
    return {
      step: "step0",
      horaire: "step",
    };
  },
};
</script>

<style>
body {
  margin-left: 20%;
  margin-right: 20%;
  display: block;
  margin-top: 10%;
}
#heures {
  display: flex;
}
button {
  margin-right: 10px;
}
.prime {
  color: red;
}
.premium {
  color: rgb(255, 0, 255);
}
#error {
  color: red;
}
#notdisponible {
  color: purple;
}
#green {
  color: rgb(0, 207, 0);
}
</style>
