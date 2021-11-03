<template>
  <div class="full-screen-portfolio" id="portfolio">
    <div class="container-fluid">
      <Video v-bind:videos="videos" />
    </div>
  </div>
</template>

<script>
import Video from "../components/Video.vue";
export default {
  name: "VideoGrid",
  components: {
    Video,
  },
  data() {
    return {
      videos: [
        {
          id: 1,
          title: "Embajada Zona 18",
          image: "embajada.jpg",
          dataVideo: "dlbrQpf-DNU",
        },
        {
          id: 2,
          title: "I am Nada",
          image: "iam_nada.jpg",
          dataVideo: "MD118-syTQM",
        },
        {
          id: 3,
          title: "IRTRA",
          image: "irtra.jpg",
          dataVideo: "MD118-syTQM",
        },
      ],
    };
  },
};
</script>

<style>
#portfolio {
  margin-top: 8rem;
}

.full-screen-portfolio .container-fluid,
.full-screen-portfolio .col-md-4,
.col-md-8 {
  padding-left: 0px;
  padding-right: 0px;
}
</style>
