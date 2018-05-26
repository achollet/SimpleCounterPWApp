<template>
      <button v-on:click=onClick class="mdl-button mdl-js-button rounded-button">
        <i class="material-icons">{{ icon }}</i>
      </button>
</template>

<style scoped>
.rounded-button
{
  border-color: white;
  border-width: 2px;
}
</style>

<
<script>
  export default {
    name: 'round-button',
    props: ['icon', 'onClick']
  }
</script>
