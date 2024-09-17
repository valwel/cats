<template>
  <HeaderNav></HeaderNav>
</template>
<script setup lang="ts">
import HeaderNav from '@/components/HeaderNav.vue';
</script>
<style lang="scss">
@import '@/assets/styles/main.scss';
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');
// #app {
//   font-family: "Lato", sans-serif;
//   font-optical-sizing: auto;
//   font-weight: weight;
//   font-style: normal;
//   color: $text;
// }

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
