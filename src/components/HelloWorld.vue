<script setup lang="ts">
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

defineProps({
  msg: String,
});

const page = ref(1);
const pageHandler = (count: number) => {
  page.value = page.value + count > 0 ? page.value + count : 1;
};

const pageNames = [
  { page: 1, name: "1~5" },
  { page: 2, name: "5~10" },
  { page: 3, name: "10~15" },
  { page: 4, name: "15~19" },
  { page: 5, name: "20~26" },
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
  <!-- 1 - 9 10 - 18 19 - 26 -->
  <div v-for="pageName in pageNames" :key="pageName.page">
    <div v-if="pageName.page === page">{{ pageName.name }}</div>
  </div>
  <!-- <div v-if="page === 1">1 ~ 9</div> -->
  <button @click="pageHandler(-1)">前へ</button>
  <button @click="pageHandler(1)">次へ</button>
  <div v-if="page === 1" class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSeyBLQOOe_t6ZG6lX1KdZ4ueJglATv-VJ1avL8IuD1XDYpJbg/viewform?embedded=true"
      width="640"
      height="8868"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in 5" :key="i">
          <img v-if="i === 0" src="../assets/images/acs1.png" alt="roji1" />
          <img v-if="i === 1" src="../assets/images/asc2.png" alt="roji2" />
          <img v-if="i === 2" src="../assets/images/asc3.png" alt="roji3" />
          <img v-if="i === 3" src="../assets/images/asc4.png" alt="roji4" />
          <img v-if="i === 4" src="../assets/images/asc5.png" alt="roji5" />
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </div>
  <div v-if="page === 2" class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSdmX20Z8w8YhuOdcufupzqHZnvOx_PUQ1oWJYTgkiriAVCU-w/viewform?embedded=true"
      width="640"
      height="8868"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in 5" :key="i">
          <img v-if="i === 0" src="../assets/images/asc6.png" alt="roji1" />
          <img v-if="i === 1" src="../assets/images/asc7.png" alt="roji2" />
          <img v-if="i === 2" src="../assets/images/asc8.png" alt="roji3" />
          <img v-if="i === 3" src="../assets/images/asc9.png" alt="roji4" />
          <img v-if="i === 4" src="../assets/images/asc10.png" alt="roji5" />
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </div>
  <div v-if="page === 3" class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSeO_RZ0nlmpfOkuzqnK4taKBJMRwJTFzvTuzI1cvaIiByB6lg/viewform?embedded=true"
      width="640"
      height="8868"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in 5" :key="i">
          <img v-if="i === 0" src="../assets/images/asc11.png" alt="roji1" />
          <img v-if="i === 1" src="../assets/images/asc12.png" alt="roji2" />
          <img v-if="i === 2" src="../assets/images/asc13.png" alt="roji3" />
          <img v-if="i === 3" src="../assets/images/asc14.png" alt="roji4" />
          <img v-if="i === 4" src="../assets/images/asc15.png" alt="roji5" />
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </div>
  <div v-if="page === 4" class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSfwklGUjB3ecB246scVwYv375syxAlPZRCOPxsCEUMdVpJeBQ/viewform?embedded=true"
      width="640"
      height="8923"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in 5" :key="i">
          <img v-if="i === 0" src="../assets/images/asc16.png" alt="roji1" />
          <img v-if="i === 1" src="../assets/images/asc17.png" alt="roji2" />
          <img v-if="i === 2" src="../assets/images/asc18.png" alt="roji3" />
          <img v-if="i === 3" src="../assets/images/asc19.png" alt="roji4" />
          <img v-if="i === 4" src="../assets/images/asc20.png" alt="roji5" />
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
  </div>
  <div v-if="page === 5" class="form-container">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSe75ylEQgWmSoncRSTueLtYIiHEqPpErpVMbGmV6jEi5W2sMg/viewform?embedded=true"
      width="640"
      height="8923"
      frameborder="0"
      marginheight="0"
      marginwidth="0"
      >読み込んでいます…</iframe
    >
    <div class="right-container">
      <carousel :items-to-show="1">
        <slide v-for="(image, i) in 6" :key="i">
          <img v-if="i === 0" src="../assets/images/asc21.png" alt="roji1" />
          <img v-if="i === 1" src="../assets/images/asc22.png" alt="roji2" />
          <img v-if="i === 2" src="../assets/images/asc23.png" alt="roji3" />
          <img v-if="i === 3" src="../assets/images/asc24.png" alt="roji4" />
          <img v-if="i === 4" src="../assets/images/asc25.png" alt="roji5" />
          <img v-if="i === 5" src="../assets/images/asc26.png" alt="" />
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
