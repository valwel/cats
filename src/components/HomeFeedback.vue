<template>
  <div class="container section">
    <div>
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="50"
        navigation
        :pagination="{ clickable: true, }"
      >
        <swiper-slide v-for="feedback in feedbacks" :key="feedback.text">
          <div class="slide">
            <div class="slide__feedback">
              <div class="slide__icon">"</div>
              <div class="slide__text">{{ feedback.text }}</div>
            </div>
            <div class="slide__info">
              <div class="slide__info-name">
                {{ feedback.name }}
              </div>
              <div class="slide__info-date">
                {{ feedback.date }}
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script setup>
import { Navigation, Pagination, Scrollbar, A11y } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

const feedbacks = [{
  text: 'Первый раз пришлось оставить нашего котика в гостинице, очень переживали. Администратор Мария каждый день высылала нам фото нашего питомца, рассказывала, как он себя чувствует. И мы и котик остались очень довольны!',
  name: 'Валерия Гришаева',
  date: '15 ноября, 2019'
},
{
  text: 'Первый раз пришлось оставить нашего котика в гостинице, очень переживали. Администратор Мария каждый день высылала нам фото нашего питомца, рассказывала, как он себя чувствует. И мы и котик остались очень довольны!',
  name: 'Валерия Гришаева',
  date: '15 ноября, 2019'
},
{
  text: 'Первый раз пришлось оставить нашего котика в гостинице, очень переживали. Администратор Мария каждый день высылала нам фото нашего питомца, рассказывала, как он себя чувствует. И мы и котик остались очень довольны!',
  name: 'Валерия Гришаева',
  date: '15 ноября, 2019'
},]
const modules = [Navigation, Pagination, Scrollbar, A11y];
</script>

<style lang="scss" scoped>
.slide {
  position: relative;
  padding: 0 100px 55px 100px;
  margin-top: 70px;

  &__icon {
    font-size: 72px;
    color: $yellow;

  }

  &__text{}

  &__info{}

  &__info-name{}

  &__info-date{}
}
</style>