<template>
  <main class="container row" style="height: 256px; width: 560px; background: white">
    <div class="col-lg-5 p-0" style="background: #EDF0F5;">
      <p class="text-center mb-0">
        <img :src="image" />
      </p>
    </div>
    <div class="col-lg-7">
      <div class="row ml-4 mt-5">
        <p class="nunito-price">{{ price }}</p>
      </div>
      <div class="row ml-4">
        <p class="nunito-header-text">{{ header }}</p>
      </div>
      <div class="row ml-4">
        <p class="nunito-small-text">{{ description }}</p>
      </div>
      <div class="row ml-4 justify-content-between">
        <div class="col p-0">
          <button style="border: none; width: 134px; height: 32px" type="button">MUA NGAY</button>
        </div>
        <div class="col p-0 text-center">
          <p class="nunito-card-text mt-1">CHI TIẾT</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  props: {
    price: String,
    header: String,
    description: String,
    image: String
  },

  data () {
    return {

    }
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

button {
  background: #C7A17A;
  border-radius: 19px;
  color: #F9FBFF;
}
</style>
