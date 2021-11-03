<template>
  <div>
    <div
      v-for="retroVideo in retroVideos"
      v-bind:key="retroVideo.id"
      class="video-wrapper"
    >
      <iframe
        :src="retroVideo.src"
        frameborder="0"
        allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      >
      </iframe>
      <hr>
    </div>
  </div>
</template>

<script>
export default {
  name: "RetroVideo",
  props: ["retroVideos"],
};
</script>

<style scoped>
.video-wrapper {
  padding: 1.5rem 0;
}
</style>
