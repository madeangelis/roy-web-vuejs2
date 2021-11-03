<template>
  <!-- Start video grid -->
  <div>
    <div
      id="video-list"
      v-for="video in videos"
      v-bind:key="video.id"
      class="col-md-4 col-sm-6"
    >
      <div class="portfolio-item" :data-video="video.dataVideo">
        <div class="thumb">
          <div class="image">
            <img :src="`../assets/img/${video.image}`" :alt="video.title" />
            <div class="overlay">
              <img src="../assets/img/play_button.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Video",
  props: ["videos"],
};
</script>

<style scoped>
.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #31313100;
  overflow: hidden;
  width: 100%;
  height: 100%;
  -webkit-transform: scale(0);
  -ms-transform: scale(0);
  transform: scale(0);
  -webkit-transition: 0.8s ease;
  transition: 0.8s ease;
}
.image:hover .overlay {
  -webkit-transform: scale(1);
  -ms-transform: scale(1);
  transform: scale(1);
}

.overlay img {
  width: 15%;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
}

.portfolio-item .thumb {
  position: relative;
}

.portfolio-item .thumb:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.portfolio-item .hover-effect .hover-content {
  position: absolute;
  text-align: left;
  width: 100%;
  bottom: 0;
  left: 0;
}
</style>
