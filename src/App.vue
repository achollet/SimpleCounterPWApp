<template>
  <div id ="app">
    <HomeView></HomeView>
  </div>
</template>

<script>
import HomeView from './components/HomeView'
require('material-design-lite')

export default {
  name: 'app',
  components: { HomeView }
}
</script>

<style>
  @import url("https://fonts.googleapis.com/icon?family=Material+Icons");
  @import url("https://code.getmdl.io/1.2.1/material.blue-red.min.css");
</style>
