<template>
  <main class="container col-lg-12" style="min-width: 360px; height: 640px; z-index: 10000; background: white">
    <div class="row" style="background: #EDF0F5;">
      <p class="text-center mb-5 mt-5">
        <img :src="data.image" />
      </p>
    </div>
    <div class="row justify-content-start ml-4 mt-4">
      <div class="col p-0"><p class="nunito-price">{{ data.price }}</p></div>
      <div class="col p-0"><p class="nunito-old-price">{{ data.oldPrice }}</p></div>
    </div>
    <div class="row ml-4">
      <p class="nunito-header-text">{{ data.header }}</p>
    </div>
    <div class="row ml-4">
      <p class="nunito-card-text">{{ data.description }}</p>
    </div>
    <div class="row ml-4 mb-5 justify-content-between">
      <div class="col p-0">
        <button style="border: none; width: 134px; height: 32px" type="button">
          MUA NGAY
        </button>
      </div>
      <div class="col p-0 text-center">
        <p class="nunito-card-text mt-1">
          CHI TIẾT
        </p>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  props: {
    data: Object
  }
}
</script>

<style>
.nunito-price {
  font-family: Nunito, sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 24px;
  color: #C7A17A;
}

.nunito-card-text {
  font-family: Nunito;
  font-style: normal;
  font-weight: bold;
  font-size: 16px;
  line-height: 22px;
  color: #415167;
}

.nunito-old-price {
  font-family: Nunito, sans-serif;
  font-style: italic;
  font-weight: 300;
  font-size: 14px;
  line-height: 19px;
  text-decoration-line: line-through;
  color: #415167;
}
</style>
