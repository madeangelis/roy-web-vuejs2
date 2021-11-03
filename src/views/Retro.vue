<template>
  <div class="retro py-5">
    <div class="container">
      <div class="col-12">
        <div class="content">
          <h2 class="text-center">Retro</h2>
          <br />
          <div id="retro-videos-wrapper" class="text-center">
            <RetroVideo v-bind:retroVideos="retroVideos" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import RetroVideo from "../components/RetroVideo.vue";

export default {
  name: "Retro",
  components: { RetroVideo },
  data() {
    return {
      retroVideos: [
        {
          id: 1,
          src: "https://www.youtube.com/embed/f1ZAnyLWMbA?rel=0",
        },
        {
          id: 2,
          src: "https://www.youtube.com/embed/rMMq08eKSwM?rel=0",
        },
        {
          id: 3,
          src: "https://www.youtube.com/embed/BQAls1prd_4?rel=0",
        },
        {
          id: 4,
          src: "https://www.youtube.com/embed/r7BNhLTlBqE?rel=0",
        },
      ],
    };
  },
};
</script>

<style>
.retro {
  background-color: #f5f7fc;
  width: 100vw;
  text-align: center;
}
.retro .content .video-wrapper {
  width: 100%;
  height: 200px;
}
.retro .content .video-wrapper iframe {
  width: 100%;
  height: 100%;
}
@media (min-width: 530px) {
  .retro .content .video-wrapper {
    min-height: 300px;
  }
  .retro .content {
    padding: 80px 60px;
  }
}
@media (min-width: 1025px) {
  .service-item img {
    width: 80%;
  }
  .retro .content .video-wrapper {
    width: 80%;
    margin: 0 auto;
    min-height: 610px;
  }
}
</style>
