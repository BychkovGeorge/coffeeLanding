<template>
  <main>
    <div class="row">
      <div class="col-lg-3 pr-0 position-relative">
        <p class="text-center">
          <img class="mt-5" src="~/assets/img/revo_logo.svg"/>
        </p>
        <div class="position-absolute" style="bottom: 0; left: 40%; z-index: 4000">
          <p class="main-text">Your</p>
          <p class="main-text-contained">PERSONALIZED</p>
          <p class="main-text">coffee</p>
        </div>
      </div>
      <div class="col-lg-6 p-0 position-relative">
        <img class="w-100" src="~/assets/img/coffee.svg"/>
        <img class="position-absolute pointer" style="top: 45%; left: 45%" src="~/assets/img/btn_play.svg" />
      </div>
      <div class="col-lg-3 p-0" style="background: #415167;">
        <ul class="mt-5 ml-5" style="list-style: none">
          <li class="position-relative pointer">
            <img src="~/assets/img/Shape.svg" />
            <div class="circle">2</div>
          </li>
        </ul>
        <ul class="mt-5 ml-5" style="list-style: none">
          <li class="mt-4 list-header pointer">
            TRANG CHỦ
          </li>
          <li class="mt-4 list-item pointer">
            COFFEE
          </li>
          <li class="mt-4 list-item pointer">
            PHIN MẠ MÀU
          </li>
          <li class="mt-4 list-item pointer">
            COMBO PHIN PHÊ
          </li>
          <li class="mt-4 list-item pointer">
            GIFTSET
          </li>
          <li class="mt-4 list-item pointer">
            LIÊN HỆ
          </li>
        </ul>
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-lg-12">
        <div class="row justify-content-center">
          <p class="small-text">Your Personalized Coffee</p>
        </div>
        <div class="row justify-content-center">
          <p class="big-text">COFFEE BUILD YOUR BASE</p>
        </div>
        <div class="row mt-5">
          <div class="col-lg-3">
            <div class="row justify-content-center">
              <img src="~/assets/img/icon_one.svg" />
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-header-text">
                Nguồn gốc
              </p>
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-small-text" style="max-width: 226px">
                Những hạt cà phê Arabica, Robusta đạt chất lượng theo tiêu chuẩn quốc tế.
              </p>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="row justify-content-center">
              <img src="~/assets/img/icon_two.svg" />
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-header-text">
                Chất lượng
              </p>
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-small-text" style="max-width: 226px">
                Từng một hạt cà phê là cả một quá trình tập trung cao độ của nghệ nhân cà phê.
              </p>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="row justify-content-center">
              <img src="~/assets/img/icon_three.svg" />
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-header-text">
                Các loại hạt
              </p>
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-small-text" style="max-width: 226px">
                70% chất lượng tách cà phê đến từ nguồn gốc và chất lượng green bean.
              </p>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="row justify-content-center">
              <img src="~/assets/img/icon_four.svg" />
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-header-text">
                Pha chế
              </p>
            </div>
            <div class="row mt-3 justify-content-center">
              <p class="nunito-small-text" style="max-width: 226px">
                Những hạt cà phê được lột xác qua quá trình rang xay kỹ lưỡng và nghiêm ngặt.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row mt-5 justify-content-center" style="height: 894px">
      <div class="col-lg-3" style="background: #415167;">
      </div>
      <div class="col-lg-6 position-relative">
        <div class="row justify-content-center mt-5">
          <p class="nunito-small-text">Choose Your Favorite</p>
        </div>
        <div class="row justify-content-center">
          <p class="nunito-header-text">CHUẨN GU ĐÚNG VỊ</p>
        </div>
        <div class="row position-absolute" style="left: -300px">
          <Swiper :data-array="coffeeCardsData" />
        </div>
      </div>
      <div class="col-lg-3">

      </div>
    </div>
  </main>
</template>

<script>
import Swiper from '~/components/swiper'

export default {
  components: {
    Swiper
  },

  data () {
    return {
      coffeeCardsData: [
        {
          image: require('~/assets/img/coffee_orange.svg'),
          price: '99.000',
          header: 'REVO Morning',
          description: 'đắng, hậu ngọt, hương hoa '
        },
        {
          image: require('~/assets/img/coffee_red.svg'),
          price: '139.000',
          header: 'REVO Origin',
          description: 'hậu ngọt, ít đắng, vị chua dâu'
        },
        {
          image: require('~/assets/img/coffee_blue.svg'),
          price: '85.000',
          header: 'REVO Everyday',
          description: 'cân bằng, hậu đắng, vị chocolate '
        },
        {
          image: require('~/assets/img/coffee_brown.svg'),
          price: '75.000',
          header: 'REVO Đậm Đà',
          description: 'đậm đà, đắng, truyền thống'
        },
        {
          image: require('~/assets/img/coffee_orange.svg'),
          price: '125.000',
          header: 'REVO Đậm Đà',
          description: 'đậm đà, đắng, truyền thống'
        },
        {
          image: require('~/assets/img/coffee_red.svg'),
          price: '225.000',
          header: 'REVO Evening',
          description: 'hậu ngọt, ít đắng, vị chua dâu'
        }
      ]
    }
  }
}
</script>

<style>
.main-text-contained {
  font-family: Montserrat, sans-serif;
  background: #C7A17A;
  color: white;
  font-weight: 900;
  font-size: 54px;
  line-height: 70px;
}

.circle {
  position: absolute;
  top: -7px;
  left: 15px;
  background: #C7A17A;
  border-radius: 50%;
  height: 20px;
  width: 20px;
  text-align: center;
  color: white;
  horiz-align: center;
}

.list-header {
  font-family: Montserrat, sans-serif;
  font-weight: bold;
  font-size: 16px;
  line-height: 22px;
  color: #EDF0F5;
}

.list-item {
  font-family: Montserrat, sans-serif;
  font-weight: 300;
  font-size: 16px;
  line-height: 24px;
  color: #EDF0F5;
}
</style>
