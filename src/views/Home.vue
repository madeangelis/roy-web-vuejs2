<template>
  <div>
    <VideoGrid />
    <Video />
  </div>
</template>

<script>
import VideoGrid from "../components/VideoGrid.vue";
import Video from "../components/Video.vue";

export default {
  name: "Home",
  components: { VideoGrid, Video },
};
</script>

<style scoped></style>
