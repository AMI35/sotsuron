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
  <div class="title" style="border: solid 2px rebeccapurple">
    <h1>昼と夜の路地写真における魅力度の研究</h1>
    <h3>次の路地写真を見て、最も適切な項目を選んでください。</h3>
    ※注意※<br />

    ・Googleアカウントにログインすると他のページに飛んでしまうため、ログインせずに回答をお願いします。<br />
    ・「送信」ボタンを押してから、「次へ」のボタンを押してください。
  </div>

  <div class="left-container">
    <div v-if="page === 1" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeCkS4I7gmPvdo3OUpRABhg_pDN0WjXZHoB6w8pyWu22sjAcw/viewform?embedded=true"
        width="640"
        height="2724"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
    </div>
    <div v-else-if="page === 2" class="form-container">
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
        <div>1枚目</div>
        <img src="../assets/images/asc1.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 3" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfDWSgpgXJGJCtKx2z3zhEul7vkgJDrrLIH2x09xuIu265mdA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>2枚目</div>
        <img src="../assets/images/asc2.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 4" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSffeFeJ3dx6R-RysFa6MHD9MkGWDGJiS_09OVUuF3FWoZufbg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>3枚目</div>
        <img src="../assets/images/asc3.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 5" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSf75x8T3CjI4Zd5lPRv4bupYTBdUsR4_z2pEus8U5NDMOXpYg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>4枚目</div>
        <img src="../assets/images/asc4.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 6" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSezXVE5CICpyMsgHXnpowdGb2KLC2zfEwmjYRYuPCgHsShw7g/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>5枚目</div>
        <img src="../assets/images/asc5.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 7" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScUR25WGe3H_UAXCA5lkiUpbI8Xv37-2xvnxLgmvYyTsBtkNg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>6枚目</div>
        <img src="../assets/images/asc6.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 8" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdlqkThx8PxMecVB5utjSnElatK79JQrbm-x2nkccjcVS93Pg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>7枚目</div>
        <img src="../assets/images/asc7.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 9" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeGqmBmLTTbZ2SpJhz8JIUCgH1UObqmJ6jZ78b0CvjzsGVCGw/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>8枚目</div>
        <img src="../assets/images/asc8.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 10" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdlLSA7Z2jexnzAEOdW4gEzmG1vwF5rr-wkNXDf7f1HJrpyIQ/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>9枚目</div>
        <img src="../assets/images/asc9.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 11" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeayK2sJDFs4ORib8GKAGlGylTYypeEyzSsIYL3YTbVe7IaaA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>10枚目</div>
        <img src="../assets/images/asc10.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 12" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSeTIjjdzGCukggMpabLJjuJBFTt2fzAxSy3wMfXxUUT9U_b4A/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>11枚目</div>
        <img src="../assets/images/asc11.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 13" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScuMpJx0YXAtPlYB3waPKD6N4cOpEFlgr4KRs9j8T6GQG4wnw/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>12枚目</div>
        <img src="../assets/images/asc12.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 14" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfc9pOI9ZS8QNBWDSc_dLqBUFgPEDib8nwHC0EoCS5zCKQwkQ/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>13枚目</div>
        <img src="../assets/images/asc13.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 15" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSetHa9nfOQOX_-6sQ_lmWvxGbRgSpXh_xxbVFHdlVV1f0CU7Q/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>14枚目</div>
        <img src="../assets/images/asc14.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 16" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfVd3glPk5mRAcF6-8_Ljl66qH9_shCvj1W89fNs27-m0YHmA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>15枚目</div>
        <img src="../assets/images/asc15.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 17" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScyRO7VTuxuujfLjRsKtpuc7CRSHx5w8rzukf8_RVFYlkw3AA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>16枚目</div>
        <img src="../assets/images/asc16.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 18" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScrabDFs1NJZAuEdKt1DKonDS8R5sXe9jDZFxqjv1pn5zLaqA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>17枚目</div>
        <img src="../assets/images/asc17.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 19" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfD-A3F7DO-2XKeOS4mQe6GVSJR_zvHgR7CtIlVKjzfqTyxdA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>18枚目</div>
        <img src="../assets/images/asc18.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 20" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfNKOv-1LoO_0t0nPEs2M3ob2UHybnNRFl6z_-KsrKJhsrBTg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>19枚目</div>
        <img src="../assets/images/asc19.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 21" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSePaNr6xUj56gbAfE76XzNeK0s-yCSmqirH9nBMSNueWZDyjw/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>20枚目</div>
        <img src="../assets/images/asc20.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 22" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSd447WiszUNvLlAvjeLprpwTdyNWe1k1yMnGLQPcUjvIJQO5w/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>21枚目</div>
        <img src="../assets/images/asc21.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 23" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfodHBdE1zD1weCTXR7EtWBfFVfVpdWOmKk_ffUqpjflQQbKQ/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>22枚目</div>
        <img src="../assets/images/asc22.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 24" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfafsgMEjsA61KZvS_bdF6puYRqVT4ezsrnpoEVZq8rL4n86w/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>23枚目</div>
        <img src="../assets/images/asc23.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 25" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfpQl4vsOuhRMJ_QEokeRKme9sd4xgNfQP4FTBMXbb3-kue_w/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>24枚目</div>
        <img src="../assets/images/asc24.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 26" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSf8ehpO_lVgl7sP25ICgE0op9_ZJ47d5_lVTHJhmAWTiuWmNA/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>25枚目</div>
        <img src="../assets/images/asc25.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 27" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSfE5Re3Ls5sff0ltleEAd9Hhrc6F62kohjwyoNUAh3mB8TpuQ/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>26枚目</div>
        <img src="../assets/images/asc26.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 28" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSe1x_dgZQlMIFBNNZaG4bmoQNHuEdHFLNDLxJqjbCx-XPAkAw/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>27枚目</div>
        <img src="../assets/images/asc27.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 29" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLScvU3i_T6liiehhUjWzoRdzoOH9tkkrNXBfO5ouNPkH8yg_2g/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>28枚目</div>
        <img src="../assets/images/asc28.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 30" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSdh3MXZ592Tw52Mlhm3CfhIYhA-m2Kwlgj6WvZ_VqYEO4HP5A/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>29枚目</div>
        <img src="../assets/images/asc29.png" alt="roji1" />
      </div>
    </div>
    <div v-else-if="page === 31" class="form-container">
      <iframe
        src="https://docs.google.com/forms/d/e/1FAIpQLSc7NCoxQACNwn6TU3IIiBLSFckj5LH0Pq47ph5prk-WUfPWwg/viewform?embedded=true"
        width="640"
        height="5290"
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        >読み込んでいます…</iframe
      >
      <div class="right-container">
        <div>30枚目</div>
        <img src="../assets/images/asc30.png" alt="roji1" />
      </div>
    </div>
    <div v-else class="form-container">
      <div class="right-container">
        <div>
          アンケートは以上になります。<br />
          ご回答ありがとうございました。
        </div>
      </div>
    </div>
    <div class="button-container">
      <button @click="pageHandler(-1)">前へ</button>
      <div style="text-align: center">
        <div>「送信」してから「次へ]</div>
        <div>
          {{ page === 1 ? null : `${page - 1}枚目` }}
        </div>
      </div>
      <button
        style="
          background-color: rgb(198, 50, 50);
          border: none;
          color: white;
          border-radius: 15%;
        "
        @click="pageHandler(1)"
      >
        次へ
      </button>
    </div>
  </div>
</template>

<style>
.carousel {
  height: 600px;
  /* color: rgb(198, 50, 50); */
  /* width: 300px; */
  /* border: 1px solid red; */
}
.carousel__viewport {
  height: 600px;
  /* width: 300px; */
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

button {
  padding: 10px 20px;
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
  background-color: rgb(213, 205, 221);
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
  }

  .button-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
  }
}
</style>
