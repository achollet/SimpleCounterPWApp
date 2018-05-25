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

    <div class="add-button rounded-button">
      <button v-on:click="addOneRep()" class="mdl-button mdl-js-button">
        <i class="material-icons">add</i>
      </button>
    </div>
    <div class="repeat-button rounded-button">
      <button v-on:click="addOneSerie()" class="mdl-button mdl-js-button">
        <i class="material-icons">repeat</i>
      </button>
    </div>
    <RoundButton v-on:click="clear()" class="reset-button"></RoundButton>
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
    addOneRep () {
      this.repetitions++
    },
    addOneSerie () {
      this.series++
      this.repetitions = 1
    },
    clear () {
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


