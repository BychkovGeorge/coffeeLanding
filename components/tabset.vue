<template>
  <main class="container row" style="background: white">
    <div class="col-lg-4 position-relative">
      <img class="position-absolute mt-5" style="left: -70%;" :src="data.image">
    </div>
    <div class="col-lg-6">
      <div class="row mt-5 ml-4">
        <p class="nunito-price">
          {{ data.price }}
        </p>
      </div>
      <div class="row ml-4">
        <p class="nunito-header-text">
          {{ data.header }}
        </p>
      </div>
      <div class="row ml-4">
        <p class="nunito-card-text">
          {{ data.description }}
        </p>
      </div>
      <div class="row mb-5 mt-4 justify-content-between">
        <div class="col p-0">
          <div class="row">
            <div class="col">
              <p class="text-center">
                <img src="~/assets/img/java.svg">
              </p>
            </div>
            <div class="col">
              <div class="row nunito-card-text">
                Loại hạt
              </div>
              <div class="row nunito-card-text">
                Fine Robusta Blend
              </div>
            </div>
          </div>
        </div>
        <div class="col p-0">
          <div class="row">
            <div class="col">
              <p class="text-center">
                <img src="~/assets/img/mountains.svg">
              </p>
            </div>
            <div class="col">
              <div class="row nunito-card-text">
                Độ cao
              </div>
              <div class="row nunito-card-text">
                700 - 800m
              </div>
            </div>
          </div>
        </div>
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
    </div>
    <div class="col-lg-2">
      <ul class="" style="list-style: none; height: 100%">
        <li id="1" class="tab-numbers list-selector position-relative pointer" style="height: 153px; vertical-align: middle" @click="changeTab(1)">
          <p class="position-absolute center">
            1
          </p>
        </li>
        <li id="2" class="tab-numbers-inactive list-selector position-relative pointer" style="height: 153px; background: #EDF0F5 !important;" @click="changeTab(2)">
          <p class="position-absolute center">
            2
          </p>
        </li>
        <li id="3" class="tab-numbers-inactive list-selector position-relative pointer" style="height: 153px; background: #EDF0F5 !important;" @click="changeTab(3)">
          <p class="position-absolute center">
            3
          </p>
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
export default {
  props: {
    data: Object
  },

  data () {
    return {

    }
  },

  methods: {
    changeTab (id) {
      document.getElementsByClassName('list-selector').forEach((el) => {
        el.classList.add('tab-numbers-inactive')
        el.style.background = '#EDF0F5'
      })
      const tab = document.getElementById(id)
      tab.classList.remove('tab-numbers-inactive')
      tab.classList.add('tab-numbers')
      tab.style.background = ''
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

.tab-numbers {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 900;
  font-size: 30px;
  line-height: 34px;
  color: #415167;
}

.tab-numbers-inactive {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 900;
  font-size: 30px;
  line-height: 34px;
  color: rgba(65, 81, 103, 0.3);
}
</style>
