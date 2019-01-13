<template>
  <div
    class="big"
    @mousemove="play"
    @click="stop"
  >
    Dumb Sound
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
      synth.triggerAttack("C4");
    },
    stop: () => {
      synth.triggerRelease();
    }
  }
};
</script>

<style scoped>
.big {
  background-color: red;
  min-height: 800px;
  min-width: 800px;
}
</style>
