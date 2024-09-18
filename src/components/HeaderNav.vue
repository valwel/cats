<template>
  <header class="container" :class="{ bg: !burger }">
    <div class="header">
      <router-link to="/" class="header__logo">
        <img src="@/assets/img/logo.svg" alt="" />
      </router-link>
      <div class="header__menu">
        <HeaderNavMenu class="mobile"></HeaderNavMenu>
        <div @click="burger = !burger" class="desktop">
          <img v-show="burger" src="@/assets/img/open-burger.svg" alt="" />
          <img v-show="!burger" src="@/assets/img/close-burger.svg" alt="" />
        </div>
      </div>
    </div>
    <HeaderNavMenu v-show="!burger" class="desktop"></HeaderNavMenu>
  </header>
</template>

<script setup lang="ts">
import HeaderNavMenu from "@/components/HeaderNavMenu.vue";
import { ref } from "vue";

const burger = ref(true);
</script>

<style lang="scss" scoped>
@import "@/assets/styles/main.scss";

.bg {
  @media (max-width: 768px) {
    background-color: $yellow;
    height: 100vh;
  }
}

.mobile {
  @media (max-width: 768px) {
    display: none;
  }
}

.desktop {
  @media (min-width: 769px) {
    display: none;
  }
}

.header {
  display: flex;
  justify-content: space-between;
  padding-top: 12px;
  padding-bottom: 12px;

  @media (max-width: 768px) {
  }

  &__menu {
    display: flex;
    align-items: center;
  }
}
</style>
