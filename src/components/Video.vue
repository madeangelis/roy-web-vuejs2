<template>
  <!-- Start video grid -->
  <div class="row">
    <div
      id="video-list"
      v-for="video in videos"
      v-bind:key="video.id"
      class="col-md-4 col-sm-6"
    >
      <div class="portfolio-item" :data-video="video.dataVideo">
        <div class="thumb">
          <div class="image">
            <img :src="displayImage(video)" :alt="video.title" />
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
  methods: {
    displayImage(video) {
      return require(`@/assets/img/${video.image}`);
    },
  },
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

.portfolio-item img {
  width: 100%;
  overflow: hidden;
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

.full-screen-portfolio .portfolio-item h1 {
  position: relative;
  font-size: 22px;
  text-transform: uppercase;
  color: #fff;
  display: inline-block;
  padding-left: 20px;
  line-height: 15px;
  transform: translateY(25px);
  transition: 0.5s ease-in-out;
  letter-spacing: 0.5px;
}

.full-screen-portfolio .portfolio-item em {
  font-style: normal;
  font-weight: 200;
}

.full-screen-portfolio .portfolio-item:hover h1 {
  transform: translateY(0);
}

.full-screen-portfolio .portfolio-item p {
  padding-left: 20px;
  font-weight: 300 !important;
  letter-spacing: 0.5px;
  font-size: 14px;
  color: #fff;
  opacity: 0;
  transform: translateY(10px);
  transition: 0.5s ease-in-out;
  text-transform: uppercase;
}

.full-screen-portfolio .portfolio-item {
  text-align: center;
  line-height: 150%;
  text-transform: lowercase;
  cursor: pointer;
}

.full-screen-portfolio .portfolio-item:hover p {
  opacity: 1;
  transform: translateY(0);
}
</style>
