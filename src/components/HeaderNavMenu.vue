<template>
  <nav class="nav h5">
    <router-link to="/">Почему мы?</router-link>
    <router-link to="/rooms">Номера</router-link>
    <a href="#">Отзывы</a>
    <a href="#">Как нас найти</a>
    <div class="nav__contacts">
      <a href="tel:+78003335599" class="nav__contacts-phone">8 (800) 333-55-99</a>
      <ul class="nav__contacts-links">
        <a href="#"><img src="@/assets/img/fb.svg" alt=""></a>
        <a href="#"><img src="@/assets/img/inst.svg" alt=""></a>
        <a href="#"><img src="@/assets/img/vk.svg" alt=""></a>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.nav {
  display: flex;
  gap: 20px;
  align-items: center;

  @media (max-width: 767px) {
    flex-direction: column;
    align-items: start;
    gap: 25px;
    padding: 50px 15px;
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
