<template>
  <div class="home">
    <CustomButton title="Применить" type="yellow-outline"></CustomButton>
    <CustomButton title="Сбросить фильтр" type="yellow"></CustomButton>
    <CustomButton title="Забронировать" type="orange" icon="white-icon"></CustomButton>
    <CustomButton title="Забронировать" type="orange-outline" icon="orange-icon"></CustomButton>
  </div>
</template>

<script setup lang="ts">
import CustomButton from '@/components/ui/CustomButton.vue';
</script>


<style lang="scss" scoped>
.home {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  gap: 20px;
}
</style>