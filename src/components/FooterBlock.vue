<template>
  <footer class="footer">
    <footer-top />
    <footer-bottom />
  </footer>
</template>
<script>
import FooterTop from "@/components/FooterTop.vue";
import FooterBottom from "@/components/FooterBottom.vue";
export default {
  components: {
    FooterTop,
    FooterBottom,
  },
  data() {
    return {
      companyLinks: {
        title: "Компания Evrika",
        links: [
          "О компани",
          "Магазины и пункты выдачи заказов",
          "Корпоративные продажи",
          "Новости",
          "Вакансии",
          "Авторизованные сервисные центры",
          "Аренда торговых помещений",
          "Контакты",
        ],
      },
      clientLinks: {
        title: "Покупателям",
        links: [
          "Акции",
          "Каталог товаров",
          "Доставка и оплата",
          "Кредит и рассрочка",
          "Возврат и обмен",
          "Гарантия лучшей цены",
          "Публичная оферта",
          "FAQ",
          "Вопросы по работе техники",
        ],
      },
      serviceLinks: {
        title: "Услуги и сервисы",
        links: [
          "Smart Service",
          "Smart Bonus",
          "Smart market",
          "Smart Gift",
          "Установка техники",
        ],
      },
    };
  },
};
</script>
<style lang="scss" scoped>
.footer {

}
</style>