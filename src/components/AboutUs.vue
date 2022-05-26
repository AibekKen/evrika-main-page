<template>
  <div class="about-us">
    <div class="title about-us__title">
      EVRIKA | надежная электроника и бытовая техника
    </div>
    <div class="about-us__body">
      <div class="about-us__column">
        EVRIKA является ведущей сетью на рынке потребительской электроники
        южного региона, осуществляющая свою деятельность с 2000 года. Сегодня
        сеть гипермаркетов электроники и бытовой техники EVRIKA включает 30
        магазинов, в 22 населенных пунктах Казахстана: Нур-Султан, Алматы,
        Шымкент, Аксукент, Аральск, Арысь, Жаркент, Жетысай, Карабулак,
        Караганда, Каскелен, Кызылорда, Ленгер, с.Казыгурт, с.Турара Рыскулова,
        с. Сарыкемер, с. Торетам, с. Узынагаш, Сарыагаш, Тараз, Туркестан, Шу.
      </div>
      <div class="about-us__column">
        География присутствия компании постоянно расширяется. Благодаря
        качественным товарам от ведущих мировых брендов, конкурентной ценовой
        политике, высококлассному формату магазинов, соответствующих
        международным стандартам и клиенто-ориентированному сервису EVRIKA
        отвечает всем требованиям своих любимых клиентов.
      </div>

      <a class="about-us__more" href="#">
        <span>ПОДРОБНЕЕ</span>
        <img src="@/assets/images/icons/arrow-more.svg" alt="" />
      </a>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.about-us {
  &__title {
    margin: 0 0 32px 0;
  }

  &__body {
    display: flex;
    justify-content: space-between;
    background: #ffffff;
    border-radius: 8px;
    padding: 24px 24px 64px;
  }

  &__column {
    flex: 0 1 48.4%;
    font-size: 14px;
    line-height: 16px;
    color: #999999;
  }

  &__more {
    position: absolute;
    left: 50%;
    bottom: 24px;
    display: flex;
    transform: translate(-50%, 0);
    font-weight: 700;
    font-size: 10px;
    color: #019aac;
    align-items: center;
    span {
      margin: 0 10px 0 0;
    }
  }
}
</style>