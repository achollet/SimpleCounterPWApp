<template>
  <div id ="app" class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
    <header class="mdl-layout__header">
      <div class="mdl-layout__header-row">
        <span class="mdl-layout-title">Series</span>
      </div>
    </header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
require('material-design-lite')

export default {
  name: 'app'
}
</script>

<style>
  @import url("https://fonts.googleapis.com/icon?family=Material+Icons");
  @import url("https://code.getmdl.io/1.2.1/material.blue-red.min.css");
</style>
