<template>
  <div class="home">
    <HomeBunner />
    <HomeAdvantages />
    <HomeRooms />
    <HomeFeedback />
  </div>
</template>

<script setup lang="ts">
// import CustomButton from '@/components/ui/CustomButton.vue';
import HomeBunner from '@/components/HomeBunner.vue';
import HomeAdvantages from '@/components/HomeAdvantages.vue';
import HomeRooms from '@/components/HomeRooms.vue';
import HomeFeedback from '@/components/HomeFeedback.vue';
</script>


<style lang="scss" scoped>
.home {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  gap: 20px;
}
</style>