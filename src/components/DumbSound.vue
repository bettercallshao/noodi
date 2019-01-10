<template>
  <div>
    <p>Dumb Sound</p>
    <button @click="play">
      Doo
    </button>
  </div>
</template>

<script>
import Tone from "tone";
const synth = new Tone.Synth({
  oscillator: {
    type: "sine4",
    modulationFrequency: 0.2
  },
  envelope: {
    attack: 0.05,
    decay: 0.1,
    sustain: 0.2,
    release: 0.9
  }
}).toMaster();

export default {
  name: "DumbSound",
  props: {},
  data: () => {
    return {};
  },
  methods: {
    play: () => {
      synth.triggerAttackRelease("C4", "2n");
      synth.triggerAttackRelease("E4", "2n");
    }
  }
};
</script>

<style scoped>
</style>
