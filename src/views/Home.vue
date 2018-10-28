<template lang="pug">
  div
    router-link(:to="{ name: 'about' }") About
</template>

<script>
export default {
  name: 'home'
}
</script>
