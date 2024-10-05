<template>
  <div class="container section rooms">
    <div class="rooms__title h2">Номера</div>
    <img src="@/assets/img/fish.svg" alt="" class="rooms__background">
    <swiper
      :modules="modules"
      :slides-per-view="1"
      :space-between="50"
      navigation
      :pagination="{ clickable: true, }"
    >
    <!-- <button @click="sw.useSwiperSlide()">Slide to the next slide</button> -->
      <swiper-slide v-for="room in rooms" :key="room.title">
        <div class="slide">
          <img :src="`img/rooms/room${room.img}.jpg`" alt="" />
          <div class="slide__card">
            <div class="slide__card-title h4">{{ room.title }}</div>
            <ul class="slide__card-list">
              <li class="slide__card-item">
                <div class="slide__card-item--marker"></div>
                <p>Площадь - {{ room.area }} м2</p>
              </li>
              <li class="slide__card-item">
                <div class="slide__card-item--marker"></div>
                <p>Размеры (ШхГхВ) — {{ room.size }} см</p>
              </li>
              <li class="slide__card-item">
                <div class="slide__card-item--marker"></div>
                <p>Цена за сутки: {{ room.price }} ₽</p>
              </li>
            </ul>
            <CustomButton
              class="slide__card-button"
              title="Забронировать"
              type="orange"
              icon="white-icon"
            />
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import CustomButton from "./ui/CustomButton.vue";
import { Navigation, Pagination, Scrollbar, A11y } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";


const rooms = [
  {
    img: 0,
    title: "Эконом плюс",
    area: "0,90",
    size: "90х100х180",
    price: "200",
  },
  {
    img: 1,
    title: "Комфорт",
    area: "1,13",
    size: "100х125х180",
    price: "250",
  },
  {
    img: 2,
    title: "Сьют",
    area: "1,56",
    size: "125х125х180",
    price: "350",
  },
];

// const onSwiper = (swiper) => {
//   console.log(swiper);
// };
// const onSlideChange = () => {
//   console.log("slide change");
// };

const modules = [Navigation, Pagination, Scrollbar, A11y];
</script>

<style lang="scss" scoped>
.rooms {
  position: relative;

  &__title {
    display: flex;
    justify-content: center;
  }

  &__background {
    position: absolute;
    top: 0;
    left: -20px;
    z-index: 0;
  }
}


.slide {
  position: relative;
  padding: 0 100px 55px 100px;
  margin-top: 70px;

  &__img {
  }

  &__card {
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.05);
    background-color: #ffffff;
    border-radius: 8px;
    padding: 30px;
    position: absolute;
    top: 10%;
    right: 150px;
    padding: 40px 110px;
  }

  &__card-title {
  }

  &__card-list {
    margin-top: 30px;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  &__card-item {
    display: flex;
    gap: 8px;
    align-items: center;
  }

  &__card-item--marker {
    width: 8px;
    height: 8px;
    background-color: $yellow;
    border-radius: 50%;
  }

  &__card-button {
    margin-top: 30px;
  }
}
</style>


