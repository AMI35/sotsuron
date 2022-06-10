<script setup lang="ts">
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

defineProps({
  msg: String,
});

const images = [
  { src: "src/assets/images/acs1.png", name: "roji1" },
  { src: "src/assets/images/asc2.png", name: "roji2" },
  { src: "src/assets/images/asc3.png", name: "roji2" },
  { src: "src/assets/images/asc4.png", name: "roji2" },
  { src: "src/assets/images/asc5.png", name: "roji2" },
  { src: "src/assets/images/asc6.png", name: "roji2" },
  { src: "src/assets/images/asc7.png", name: "roji2" },
  { src: "src/assets/images/asc8.png", name: "roji2" },
  { src: "src/assets/images/asc9.png", name: "roji2" },
  { src: "src/assets/images/asc10.png", name: "roji2" },
  { src: "src/assets/images/asc11.png", name: "roji2" },
  { src: "src/assets/images/asc12.png", name: "roji2" },
  { src: "src/assets/images/asc13.png", name: "roji2" },
  { src: "src/assets/images/asc14.png", name: "roji2" },
  { src: "src/assets/images/asc15.png", name: "roji2" },
  { src: "src/assets/images/asc16.png", name: "roji2" },
  { src: "src/assets/images/asc17.png", name: "roji2" },
  { src: "src/assets/images/asc18.png", name: "roji2" },
  { src: "src/assets/images/asc19.png", name: "roji2" },
  { src: "src/assets/images/asc20.png", name: "roji2" },
  { src: "src/assets/images/asc21.png", name: "roji2" },
  { src: "src/assets/images/asc22.png", name: "roji2" },
  { src: "src/assets/images/asc23.png", name: "roji2" },
  { src: "src/assets/images/asc24.png", name: "roji2" },
  { src: "src/assets/images/asc25.png", name: "roji2" },
  { src: "src/assets/images/asc26.png", name: "roji2" },
];
</script>

<template>
  <div class="title">
    <h1>路地写真の印象評価</h1>
    <h3>次の路地写真を見て、最も適切な項目を選んでください。</h3>
    <a
      >※注意※Googleアカウントにログインすると他のページに飛んでしまうため、ログインせずに回答をお願いします。</a
    >
  </div>
  <div class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSeyBLQOOe_t6ZG6lX1KdZ4ueJglATv-VJ1avL8IuD1XDYpJbg/viewform?embedded=true"
      width="640"
      height="11540"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in images" :key="i">
          <!-- <img :src="image.src" :alt="image.name" /> -->
          <img src="../assets/images/acs1.png" alt="" />
        </slide>
        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </div>
</template>

<style>
.carousel {
  height: 600px;
  /* width: 300px; */
  /* border: 1px solid red; */
}
.carousel__viewport {
  height: 600px;
  /* width: 300px; */
  /* border: 1px solid blue; */
}
.carousel__track {
}
.carousel__slide {
  /* justify-content: flex-start; */
  /* width: fit-content; */
}
iframe {
  height: 700px;
  overflow-y: scroll;
  scrollbar-color: rebeccapurple green;
  scrollbar-width: thin;
}

img {
  width: 55%;
}

.title {
  border: 1px solid black;
  width: 100%;
  padding: 0px 10px;
}

.form-container {
  display: flex;
  width: 100vw;
  overflow: hidden;
}

.right-container {
  width: 50vw;
}

@media screen and (max-width: 500px) {
  /*　画面サイズが480px以下の場合ここの記述が適用される　*/

  iframe {
    height: 400px;
    width: 100%;
    overflow-y: scroll;
    scrollbar-color: rebeccapurple green;
    scrollbar-width: thin;
  }

  img {
    width: 100%;
  }

  .form-container {
    display: flex;
    flex-direction: column-reverse;
    width: 100%;
  }

  .right-container {
    padding-right: 0px;
    height: 100%;
    margin-left: 100px;
  }

  .carousel {
    height: 100%;
    /* width: 300px; */
    /* border: 1px solid red; */
  }

  .carousel__viewport {
    height: 385px;
    /* width: 300px; */
    /* border: 1px solid blue; */
  }
}
</style>
