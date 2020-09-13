<template>
  <div id="app">
    <contenu></contenu>
    <header-top> </header-top>
  </div>
</template>

<script>


import Header from "./components/Header.vue"
import Contenu from "./components/Contenu.vue"

export default {
  name: 'App',
  components: {
   "contenu": Contenu,
   "header-top" : Header
  }
}
</script>

<style>

</style>
