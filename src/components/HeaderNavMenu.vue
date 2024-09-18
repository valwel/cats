<template>
  <nav class="nav h5">
    <router-link to="/">Почему мы?</router-link>
    <router-link to="/rooms">Номера</router-link>
    <a href="#">Отзывы</a>
    <a href="#">Как нас найти</a>
    <div class="nav__contacts">
      <a href="tel:+78003335599" class="nav__contacts-phone">8 (800) 333-55-99</a>
      <ul class="nav__contacts-links">
        <li><img src="@/assets/img/fb.svg" alt=""></li>
        <li><img src="@/assets/img/inst.svg" alt=""></li>
        <li><img src="@/assets/img/vk.svg" alt=""></li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/main.scss';
.nav {
  display: flex;
  gap: 20px;
  align-items: center;

  @media (max-width: 768px) {
    margin-top: 50px;
    flex-direction: column;
    align-items: start;
    gap: 25px;
  }

  &__contacts {
    margin-top: 40px;
    display: flex;
    flex-direction: column;
    gap: 25px;

    @media (min-width: 768px) {
      display: none;
    }
  }

  &__contacts-phone {
    font-weight: 400;
  }

  &__contacts-links {
    display: flex;
    gap: 20px;
  }
}
</style>
