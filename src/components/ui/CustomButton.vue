<template>
  <button
    class="custom-button"
    :class="{
      'custom-button--yellow-outline': props.type === 'yellow-outline',
      'custom-button--yellow': props.type === 'yellow',
      'custom-button--orange': props.type === 'orange',
      'custom-button--orange-outline': props.type === 'orange-outline',
    }"
  >
    <span class="custom-button__title">{{ props.title }}</span>
    <img
      v-if="props.icon"
      class="custom-button__icon"
      :src="
        props.icon === 'white-icon'
          ? '/icons/button-logo.svg'
          : '' || props.icon === 'orange-icon'
          ? '/icons/button-logo-inversive.svg'
          : ''
      "
      alt=""
    />
  </button>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps({
  title: String,
  type: String,
  icon: String,
});
</script>

<style lang="scss" scoped>
.custom-button {
  border-radius: 25px;
  font-size: 14px;
  font-weight: 600;

  &--yellow {
    background-color: $yellow;
    padding: 16px 0;
  }

  &--yellow-outline {
    border: solid 1px $yellow;
    padding: 16px 0;
  }

  &--orange {
    background-color: $orange;
    color: $white;
    display: flex;
    align-items: center;
    padding: 6px;
    justify-content: space-between;
  }

  &__title {
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 0 30px;
  }

  &__icon {
    max-width: 34px;
    max-height: 34px;
  }

  &--orange-outline {
    outline: solid 1px $orange;
    background-color: $white;
    display: flex;
    align-items: center;
    padding: 6px;
  }
}
</style>
