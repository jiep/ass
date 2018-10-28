<template lang="pug">
  div(id="app")
    h1 Hello Electron!
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style lang="sass">
#app
  height: 100%
  width: 100%
  border: 0
  background-color: black
  color: white

  h1
    margin: 0
</style>
