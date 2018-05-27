<template>
  <div class="container">
    <div class="label-container label">
      <!-- Labels Row -->
      <div class="serie-label"> SERIES </div>
      <div class="repetition-label"> REPETITIONS </div>
      <!-- Values Display-->
      <div class="serie-value">{{series}}</div>
      <div class="value-separator">/</div>
      <div class="repetition-value">{{repetitions}}</div>
    </div>

    <div class="buttons-container">
      <round-button icon='add' :onClick=addOneRep class="add-button label"></round-button>
      <round-button icon='repeat' :onClick=addOneSerie class="repeat-button label"></round-button>
      <round-button icon='clear' :onClick=reset class="reset-button label"></round-button>
    </div>
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
  height: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 2fr;
  grid-template-areas: 'label-container' 'buttons-container';
  background-color:#9c43bc;
}

.label-container {
  display: grid;
  grid-template-columns: 20px 1fr 10% 1fr 20px;
  grid-template-rows: 20px 1fr 40px 1fr 20px;
  grid-row-gap: 10px;
}

.buttons-container {
  display: grid;
  grid-template-columns: 20px 1fr 10% 1fr 20px;
  grid-template-rows: 20px 1fr 40px 1fr 20px;
  grid-row-gap: 10px;
}

.label {
  color: white;
  font-family: monospace;
  font-size: 1.7em;
  font-weight: 600;
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
  grid-row-start: 2;
  grid-row-end: 3;
  grid-column-start: 2;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

.repeat-button {
  grid-row-start: 4;
  grid-row-end: 5;
  grid-column-start: 2;
  grid-column-end: 3;
  justify-self: center;
  align-self: center;
}

.reset-button {
  grid-row-start: 4;
  grid-row-end: 5;
  grid-column-start: 4;
  grid-column-end: 5;
  justify-self: center;
  align-self: center;
}

</style>


