<template>
  <div id="video" :class="[displayVideo ? '' : 'invisible', 'back']">
    <iframe
      id="videoImage"
      width="80%"
      height="80%"
      src=""
      frameborder="0"
      allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </div>
</template>

<script>
export default {
  name: "Video",
  data() {
    return {
      displayVideo: false,
    };
  },
};
</script>

<style scoped>
#video {
  position: fixed;
  background-color: rgba(0, 0, 0, 0.8);
  height: 100vh;
  width: 100vw;
  overflow: hidden;
  top: 0px;
  left: 0px;
  z-index: 1000;
}
#videoImage {
  position: fixed;
  top: 12vh;
  left: 15vw;
  z-index: 100;
}
</style>
