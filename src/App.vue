<template lang="pug">
  div(id="app")
    Bar/
    .content
      .notification.is-success(v-if="isCv") OpenCV is loaded
      .notification.is-danger(v-else="isCv") OpenCV is not loaded
      router-view/
</template>

<script>
import Bar from '@/components/Bar'
// const cv =  require('opencv4nodejs')
// import * as path from 'path'
// import * as fs from 'fs'

export default {
  name: 'app',
  components: {
    Bar
  },
  data() {
    return {
      isCv: false
    }
  },
  mounted() {
    // if (!cv.xmodules.face) {
    //   throw new Error('exiting: opencv4nodejs compiled without face module');
    //   this.isCv = false;
    // }else{
    //   this.isCv = true;
    // }
    // const classifier = new cv.CascadeClassifier('public/HAAR_FRONTALFACE_ALT2.xml');
    // console.log(classifier);
  }
}
</script>

<style lang="sass">
@import @/assets/styles.sass
#app
  height: 100%
  width: 100%
  border: 0
  background-color: $body-background-color
  color: black
</style>
