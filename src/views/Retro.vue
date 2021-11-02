<template>
  <div class="retro">
    <div class="retro">
      <div class="container">
        <div class="col-12">
          <div class="content">
            <h2 class="text-center">Retro</h2>
            <br />
            <div class="text-center">
              <div class="video-wrapper">
                <iframe
                  src="https://www.youtube.com/embed/f1ZAnyLWMbA?rel=0"
                  frameborder="0"
                  allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                >
                </iframe>
              </div>
              <hr />
              <div class="video-wrapper">
                <iframe
                  src="https://www.youtube.com/embed/rMMq08eKSwM?rel=0"
                  frameborder="0"
                  allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                >
                </iframe>
              </div>
              <hr />
              <div class="video-wrapper">
                <iframe
                  src="https://www.youtube.com/embed/BQAls1prd_4?rel=0"
                  frameborder="0"
                  allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                >
                </iframe>
              </div>
              <hr />
              <div class="video-wrapper">
                <iframe
                  src="https://www.youtube.com/embed/r7BNhLTlBqE?rel=0"
                  frameborder="0"
                  allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                >
                </iframe>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Retro",
};
</script>

<style scoped>
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
    width: 100%;
    min-height: 510px;
  }
}
</style>
