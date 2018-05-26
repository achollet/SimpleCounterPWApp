<template>
  <div class="container">
    <div class="serie-label label">
      SERIES
    </div>
    <div class="repetition-label label">
      REPETITIONS
    </div>

    <div class="serie-value label">
      X {{series}}
    </div>
    <div class="value-separator label">/</div>
    <div class="repetition-value label">
      {{repetitions}}
    </div>

    <round-button icon='add' :onClick=addOneSerie class="add-button"></round-button>
    <round-button icon='repeat' :onClick=addOneSerie class="repeat-button"></round-button>
    <round-button icon='clear' :onClick=reset class="reset-button"></round-button>
  </div>
</template>

<script>
import RoundButton from './RoundButton.vue'
export default {
  name: 'HomeView',
  components: {RoundButton},
  data () {
    return {
      series: 1,
      repetitions: 1
    }
  },
  methods: {
    addOneRep: function () {
      this.repetitions++
    },
    addOneSerie: function () {
      this.series++
      this.repetitions = 1
    },
    reset: function () {
      this.repetitions = 1
      this.series = 1
    }
  }
}
</script>

<style>
.container {
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-columns: 10% 37.5% 5% 37.5% 10%;
  grid-template-rows: 20px repeat(2, 40px) 40px 60px 10% 20px;
  background-color: cornflowerblue;
}

.label {
  color: white;
  font-family: monospace;
  font-size: 2.5em;
  font-weight: 900;
}

.serie-label {
  grid-row-start: 2;
  grid-row-end: 3;
  grid-column-start: 2;
  grid-column-end: 3;
  justify-self: center;
  align-self: center;
}

.repetition-label {
  grid-row-start: 2;
  grid-row-end: 3;
  grid-column-start: 4;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

.serie-value {
  grid-row-start: 3;
  grid-row-end: 4;
  grid-column-start: 2;
  grid-column-end: 3;
  justify-self: center;
  align-self: center;
}

.value-separator {
  grid-row-start: 3;
  grid-row-end: 4;
  grid-column-start: 3;
  grid-column-end: 4;
  justify-self: center;
  align-self: center;
}

.repetition-value {
  grid-row-start: 3;
  grid-row-end: 4;
  grid-column-start: 4;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

.add-button {
  grid-row-start: 5;
  grid-row-end: 6;
  grid-column-start: 2;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

.repeat-button {
  grid-row-start: 6;
  grid-row-end: 7;
  grid-column-start: 2;
  grid-column-end: 3;
  justify-self: center;
  align-self: center;
}

.reset-button {
  grid-row-start: 6;
  grid-row-end: 7;
  grid-column-start: 4;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

</style>


