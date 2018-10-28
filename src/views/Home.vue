<template lang="pug">
  .home
    h1 This is a home page
    router-link(:to="{ name: 'about' }") About
</template>

<script>
export default {
  name: 'home'
}
</script>
