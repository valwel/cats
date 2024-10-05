<template>
  <div class="bunner">
    <div class="bunner__info">
      <div class="h6">Санкт-Петербург</div>
      <div class="h1">Котейка</div>
      <div class="h5">Уютная гостиница для котов и кошек</div>
      <CustomButton class="bunner__button" title="Забронировать" type="orange-outline" icon="orange-icon"></CustomButton>
    </div>
    <div class="bunner__cat">
      <img class="bunner__cat-img" src="@/assets/img/bunner.webp" alt="">
    </div>
  </div>
</template>

<script setup lang="ts">
import CustomButton from '@/components/ui/CustomButton.vue';
</script>

<style lang="scss" scoped>
.bunner {
  background: linear-gradient(#FF9B53, #F8B653);
  height: 504px;
  width: 100%;
  position: relative;

  &__info{
    padding: 150px 200px;
  }

  &__button{
    margin-top: 40px;
  }

  &__cat{
    position: absolute;
    top: 0;
    right: 0;
  }
  
  &__cat-img {
    max-height: 500px;
  }
}
</style>