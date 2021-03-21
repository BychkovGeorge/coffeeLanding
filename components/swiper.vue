<template>
  <div>
    <swiper v-if="variant === 'simple'" class="swiper" :options="swiperOptions">
      <swiper-slide>
        <Card
          class="mb-5"
          :image="dataArray[0].image"
          :price="dataArray[0].price"
          :header="dataArray[0].header"
          :description="dataArray[0].description"
        />
        <Card
          :image="dataArray[1].image"
          :price="dataArray[1].price"
          :header="dataArray[1].header"
          :description="dataArray[1].description"
        />
      </swiper-slide>
      <swiper-slide>
        <Card
          class="mb-5"
          :image="dataArray[2].image"
          :price="dataArray[2].price"
          :header="dataArray[2].header"
          :description="dataArray[2].description"
        />
        <Card
          :image="dataArray[3].image"
          :price="dataArray[3].price"
          :header="dataArray[3].header"
          :description="dataArray[3].description"
        />
      </swiper-slide>
      <swiper-slide>
        <Card
          class="mb-5"
          :image="dataArray[4].image"
          :price="dataArray[4].price"
          :header="dataArray[4].header"
          :description="dataArray[4].description"
        />
        <Card
          :image="dataArray[5].image"
          :price="dataArray[5].price"
          :header="dataArray[5].header"
          :description="dataArray[5].description"
        />
      </swiper-slide>
      <div slot="button-next" class="btn-next position-absolute" style="top: 45.5%; right: 30%; z-index: 10000">
        <img src="~/assets/img/next.svg" />
      </div>
    </swiper>

    <swiper v-if="variant === 'combo'" class="swiper" :options="swiperOptionsCombo">
      <swiper-slide>
        <ComboCard :data="dataArray[0]" />
      </swiper-slide>
      <swiper-slide>
        <ComboCard :data="dataArray[1]" />
      </swiper-slide>
      <swiper-slide>
        <ComboCard :data="dataArray[2]" />
      </swiper-slide>
      <swiper-slide>
        <ComboCard :data="dataArray[3]" />
      </swiper-slide>
      <swiper-slide>
        <ComboCard :data="dataArray[4]" />
      </swiper-slide>
      <div slot="button-next" class="btn-next position-absolute" style="top: 296px; right: 10%; z-index: 10000">
        <img src="~/assets/img/next.svg" />
      </div>
    </swiper>
  </div>
</template>

<script>
import Card from '~/components/coffee-card'
import ComboCard from '~/components/combo-card'
import 'swiper/swiper-bundle.css'

export default {
  components: {
    Card,
    ComboCard
  },

  props: {
    dataArray: Array,
    variant: String
  },

  data () {
    return {
      swiperOptions: {
        slidesPerView: 2.5,
        navigation: {
          nextEl: '.btn-next',
          prevEl: '.btn-prev'
        }
      },
      swiperOptionsCombo: {
        slidesPerView: 3.5,
        spaceBetween: 100,
        navigation: {
          nextEl: '.btn-next',
          prevEl: '.btn-prev'
        }
      }
    }
  }
}
</script>

<style>
.btn-next {
  height: 48px;
  width: 48px;
  background: #C7A17A;
  border-radius: 50%;
  text-align: center;
  padding-top: 8px;
}
</style>
