<template>
  <header class="header" :class="{ 'header__menu-open': !isMenuOpened }">
    <div class="container header__container">
      <router-link to="/" class="header__logo">
        <img src="@/assets/img/logo.svg" alt="" />
      </router-link>
      <div class="header__menu">
        <HeaderNavMenu class="header__mobile"></HeaderNavMenu>
        <div @click="isMenuOpened = !isMenuOpened" class="header__burger">
          <img
            v-show="isMenuOpened"
            src="@/assets/img/open-burger.svg"
            alt=""
          />
          <img
            v-show="!isMenuOpened"
            src="@/assets/img/close-burger.svg"
            alt=""
          />
        </div>
      </div>
    </div>
    <HeaderNavMenu
      class="header__desktop"
      :class="{active: !isMenuOpened}"
    ></HeaderNavMenu>
  </header>
  <router-view/>
</template>

<script setup lang="ts">
import HeaderNavMenu from "@/components/HeaderNavMenu.vue";
import { ref } from "vue";

const isMenuOpened = ref(true);
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  display: flex;
  justify-content: space-between;
  padding-top: 12px;
  padding-bottom: 12px;

  &__container {
    display: flex;
    justify-content: space-between;
  }

  &__menu {
    display: flex;
    align-items: center;
    max-height: 52px;
  }

  &__menu-open {
    height: 100vh;
    overflow: hidden;
    background-color: $yellow;
  }

  &__mobile {
    @media (max-width: 767px) {
      display: none;
    }
  }

  &__burger {
    @media (min-width: 768px) {
      display: none;
    }
  }

  &__desktop {
    width: 100%;
    height: 100vh;
    position: fixed;
    top: -100%;
    transition: top .3s ease-in-out;

    &.active {
      top: 76px;
    }
  }
}
</style>
