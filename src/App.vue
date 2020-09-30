<template>
  <div id="app">
    <top-header></top-header>
    <contenu></contenu>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Contenu from './components/Contenu.vue'

export default {
  name: 'App',
  components: {
    'top-header': Header,
    'contenu': Contenu
  }
}
</script>

<style>

</style>
