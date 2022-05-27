<template>
  <footer class="footer">
    <div class="container">
      <footer-top />
      <div class="footer__footer-bottom footer-bottom"></div>
    </div>
  </footer>
</template>
<script>
import FooterTop from "@/components/FooterTop.vue";
export default {
  components: {
    FooterTop,
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
  padding: 24px 0;
  background: #ffffff;
}
</style>