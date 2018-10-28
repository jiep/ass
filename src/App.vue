<template lang="pug">
  div(id="app")
    h1 Hello Electron!
    router-view/
</template>

<script>
export default {
  name: 'app'
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
