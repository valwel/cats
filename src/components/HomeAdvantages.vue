<template>
  <div class="container section advantages">
    <img class="advantages__background" src="@/assets/img/paw.svg" alt="" />
    <p class="advantages__title h3">Почему мы?</p>
    <ul class="advantages__cards">
      <li v-for="card in cards" :key="card.title" class="advantages__card">
        <img :src="card.icon" alt="" class="advantages__card-icon" />
        <p class="advantages__card-title h4">{{ card.title }}</p>
        <p class="advantages__card-subtitle">{{ card.subtitle }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
interface ICard {
  icon: string;
  title: string;
  subtitle: string;
}

const cards: ICard[] = [
  {
    icon: "/icons/icon-card/0.svg",
    title: "Комфортная температура",
    subtitle:
      "Во всех номерах поддерживается комфортная температура в пределах 23 - 25 градусов. В каждом номере можно дополнительно отрегулировать температуру. ",
  },
  {
    icon: "/icons/icon-card/1.svg",
    title: "Видеонаблюдение",
    subtitle:
      "Мы предоставляем доступ в нашу систему. Вы сможете следить за своим питомцем со своего смартфона или компьютера.",
  },
  {
    icon: "/icons/icon-card/2.svg",
    title: "Услуги Зоотакси",
    subtitle: "Мы приедем за вашим питомцем в любой район Санкт-Петербурга.",
  },
  {
    icon: "/icons/icon-card/3.svg",
    title: "Сбалансированное питание",
    subtitle:
      "Вы можете привезти свой корм или доверить рацион своего питомца нашим профессионалам.",
  },
  {
    icon: "/icons/icon-card/4.svg",
    title: "Ежедневные прогулки",
    subtitle:
      "По вашему желанию мы выгуливаем вашего питомца два раза в день на специализированной закрытой территории.",
  },
  {
    icon: "/icons/icon-card/5.svg",
    title: "Лучшие ветеринары",
    subtitle:
      "В гостинице 24 часа дежурит ветеринарный врач, который окажет любую помощь в случае необходимости.",
  },
];
</script>

<style lang="scss" scoped>
.advantages {
  position: relative;
  z-index: 10;

  &__background {
    position: absolute;
    top: -140px;
    right: -20px;
    z-index: 0;
  }

  &__title {
    display: flex;
    justify-content: center;
  }

  &__cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 25px;
    grid-auto-rows: minmax(100px, auto);
    margin-top: 70px;
    position: relative;
    z-index: 10;
  }

  &__card {
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.05);
    background-color: #ffffff;
    border-radius: 8px;
    padding: 30px;
  }

  &__card-icon {
  }

  &__card-title {
    margin-top: 35px;
  }

  &__card-subtitle {
    margin-top: 20px;
  }
}
</style>
