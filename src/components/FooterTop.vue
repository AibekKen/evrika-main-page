<template>
  <div class="footer__footer-top footer-top">
    <div class="container">
      <div class="footer-top__body">
        <subs-us class="subs-us" />
        <links-list class="links-list" :listBlock="companyLinks" />
        <links-list class="links-list links-list_2" :listBlock="clientLinks" />
        <links-list class="links-list links-list_3" :listBlock="serviceLinks" />
        <div class="footer-top__contacts contacts">
          <div class="subtitle contacts__title">Контакты</div>
          <a href="tel:+77719365454" class="contacts__number"
            >+7(771) 936-54-54</a
          >
          <div class="text contacts__time">С 09:00 до 21:00 (без выходных)</div>
          <a href="#" class="contacts__links">Написать на WhatsApp</a>
          <a href="mailto:support@evrika.com" class="contacts__links"
            >support@evrika.com</a
          >
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import SubsUs from "@/components/SubsUs.vue";
import LinksList from "@/components/UI/LinksList.vue";
export default {
  components: {
    SubsUs,
    LinksList,
  },
  data() {
    return {
      subsWay: "phone",
      email: "",
      phone: "",
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
.links-list {
  margin: 0 12px 0 0;
}

.links-list_2 {
  margin: 0 63px 0 0;
}

.links-list_3 {
  margin: 0 93px 0 0;
}
.footer-top {
  &__body {
    display: flex;
    &__column {
    }
  }
}

.footer-top {
  padding: 24px 0;
  background: #ffffff;
  &__contacts {
  }
}
.contacts {
  a {
    display: block;
  }
  a:hover {
    color: #fb791b;
  }
  &__title {
  }

  &__number {
    font-family: "Inter";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 17px;
    letter-spacing: 0.02em;
    color: #000000;
    margin: 0 0 8px 0;
  }

  &__time {
    font-family: "Inter";
    margin: 0 0 8px 0;
  }

  &__links {
    font-family: "Inter";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 17px;
    letter-spacing: 0.02em;
    color: #029aad;
    margin: 0 0 8px 0;
  }
}
.subtitle {
}
.text {
}
.subs-us {
  margin: 0 70px 0 0;
}
</style>