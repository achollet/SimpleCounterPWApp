<template>
      <button v-on:click=onClick class="mdl-button mdl-js-button rounded-button">
        <i class="material-icons .round-button-icon">{{ icon }}</i>
      </button>
</template>

<style scoped>
.rounded-button
{
  width: 100%;
  height: 100%;
  padding-bottom: 10%;
  border-radius: 50%;
  border: 3px solid white;
  overflow: hidden;
}

.round-button-icon {
    display: block;
    width: auto;
    padding: 12%;
    height: auto;
}
</style>

<script>
  export default {
    name: 'round-button',
    props: ['icon', 'onClick']
  }
</script>
