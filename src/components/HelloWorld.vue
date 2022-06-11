<script setup lang="ts">
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

defineProps({
  msg: String,
});

const page = ref(Number(window.localStorage.getItem("page")) || 1);

const pageHandler = (count: number) => {
  page.value = page.value + count > 0 ? page.value + count : 1;
  const value = page.value.toString();
  window.localStorage.setItem("page", value);
};
</script>

<template>
  <div class="title">
    <h1>路地写真の印象評価</h1>
    <h3>次の路地写真を見て、最も適切な項目を選んでください。</h3>
    ※注意※<br />
    ・Googleアカウントにログインすると他のページに飛んでしまうため、ログインせずに回答をお願いします。<br />
    ・「送信」ボタンを押してから、「次へ」のボタンを押してください。
  </div>

  <div class="left-container">
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
        <img src="../assets/images/acs1.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 2" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSe1tw1IwDdTHzR5OycpTRQqm3tl5ffAqvRoRWuvbKud-yl64w/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc2.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 3" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdLpfQma2qgBWoq2GOLXqvWseJ7HhBZUDOk3M58OqHQzZ_cVQ/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc3.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 4" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSf7eQ6juF1cwpI4tpLsF9m_IN3QcYfz9cqocnpIaIDQc6rb7Q/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc4.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 5" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSceZmkf4VLVz7Ujq53gf1GRiEV2dDSpXYnJXRytrMWyKg2WDQ/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc5.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 6" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdJN7G4JezkSZsXTv1ZmZaVXAF6WuNTg-1O6ZGFny2VlTNlbg/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc6.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 7" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSediOQ4-LOB2cYjwmZccy7yfWYlDivc1Vuh3iPc3LZIGRSLRQ/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc7.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 8" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeC7-V5BEWMGATDZh1xnw9xDWpKjBiYJUSWPBZkwo2NCL_v_Q/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc8.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 9" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeQWZgJiTW98a7oa_FcNjUU2RdnKoT7MVVtrH8OxEgzlOSKJQ/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc9.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 10" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeMEpdVxyPdjJc8Pl89eyX_JDS4RGUukKe-cRztptVd3XaEQA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc10.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 11" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfppVuYcpzrxaqfw1C9zLXLkOHl7lfns6nlZV6RlRI7rbPBbA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc11.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 12" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfyNkRbbBbp-LpgEOjocIuqVE7Oy7l4ZqllSiludk9VfxBt1A/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc12.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 13" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfwo4LhEqBn0HtYeDUqCpwBEgdCQ1iCGtexbnlnY1omv_5BgA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc13.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 14" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScaDHtXMEbNtv7BhDiSE_0DBiISqQWtDSHDGJS8FSn5K3w8Wg/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc14.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 15" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSf46o95C93FYkOrleN2dbkriLeF4rWc1RjhMTb4VbcQ7Odxug/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc15.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 16" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfejVRkjgSBLC4-FWLsThbu977o6enm94LV_CeKoC57Xx3X7Q/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc16.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 17" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfnatlwpGzT2x2NTL0Ntj-PsWl0isoXEU-0x_dU0gxWdPno4w/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc17.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 18" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfpwDgEldiyIskzLNpnLPHuMB-rZfo_fv7i3ZxSBoebOpF5Dw/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc18.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 19" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSf-25R0HjANb8ZPkgFicdECzIRO1wLvfQq06Fvuqeawq0UZDA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc19.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 20" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSc1ablvgKUv__Zn4XK_hUU5ufFQ4bBqoyroinA3RSCWalpO5A/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc20.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 21" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdzMa7SgRWE0hNGdKUrKcyeG6yGZh-QicFxJBE4wwULYcj87w/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc21.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 22" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeW2a_zSyEfbGnSHjYA1xtmpEKCAQrClTIRoVN2-H70RRStAA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc22.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 23" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdkYWZ87fDMzgVFeJXtsFh6wn_GHSuLeOItgBTdPx7NcrTpzA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc23.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 24" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScOvnP3GkbiPfTq3R25Ox4JpI4fNwW2NuL8QGAllOt7N15zWw/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc24.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 25" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdI6pTJU7tR8zH6VB0kEqDrk-X6MPTNI9yvm5_K_1P1oA-WQA/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc25.png" alt="roji1" />
      </div>
    </div>
    <div v-else class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSc2B2hMRLeX3xLD-DkolUsBfQYPz7THr2VsJPVjWrL8jHaX7Q/viewform?embedded=true"
        width="640"
        height="8993"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <img src="../assets/images/asc26.png" alt="roji1" />
      </div>
    </div>
    <div class="button-container">
      <button @click="pageHandler(-1)">前へ</button>{{ page }}枚目
      <button @click="pageHandler(1)">次へ</button>
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

.button-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 40%;
  padding: 20px;
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

  button {
    margin: 10px;
  }

  .form-container {
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    width: 100%;
  }

  .right-container {
    display: flex;
    /* padding-right: 0px; */
    height: 100%;
    /* margin-left: 100px; */
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

  .button-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
  }
}
</style>
