<template>
  <div class="full-screen-portfolio" id="portfolio">
    <div class="container-fluid">
      <Video v-bind:videos="videos" />
    </div>
  </div>
</template>

<script>
import Video from "./VideoContainer.vue";
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
        {
          id: 4,
          title: "Toyota",
          image: "toyota.jpg",
          dataVideo: "c8SedrGtWtk",
        },
        {
          id: 5,
          title: "Burger King",
          image: "burger_king.jpg",
          dataVideo: "zix3XgDvb6U",
        },
        {
          id: 6,
          title: "Super 24 Buzos/Astronauta",
          image: "buzos.png",
          dataVideo: "6RImAVN0_1g",
        },
        {
          id: 7,
          title: "Bonie",
          image: "bonie.jpg",
          dataVideo: "rBilOt9iRdQ",
        },
        {
          id: 8,
          title: "Bomberos Voluntarios",
          image: "bomberos.jpg",
          dataVideo: "sESeBymKXgw",
        },
        {
          id: 9,
          title: "Shinny Lessons",
          image: "shinny_lessons.jpg",
          dataVideo: "xLD9lVytOJ0",
        },
      ],
    };
  },
};
</script>

<style>
#portfolio {
  margin-top: 5rem;
}

.full-screen-portfolio .container-fluid,
.full-screen-portfolio .col-md-4,
.col-md-8 {
  padding-left: 0px;
  padding-right: 0px;
}
</style>
