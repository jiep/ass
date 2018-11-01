<template lang="pug">
  div
    .notification.is-danger(v-if="error") Could not connect stream
    button.button(@click="onClick", :class="{ 'is-danger': recording, 'is-info': !recording }") {{text}}
    video(v-if="recording", id="camera")
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      recording: false,
      text: 'Record',
      error: false,
      track: null
    }
  },
  methods: {
    onClick() {
      this.recording = !this.recording
      this.text = this.recording ? 'Stop' : 'Record'
      if(this.recording) {
        this.track.stop()
      }
    }
  },
  mounted() {
    if (this.recording)
      this.text = 'Recording'
    navigator.mediaDevices.getUserMedia({video: true})
  .then((stream) => {
    document.getElementById('camera').srcObject = stream;
    this.track = stream.getTracks()[0];
  }).catch(() => {
    this.error = true;
    this.recording = false;
  });
  }
}
</script>

<style lang="sass">
  video
    object-fit: fill
    width: 100%
    height: inherit
</style>
