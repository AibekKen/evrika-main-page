<template >
  <div class="footer-bottom__column social">
    <div class="subtitle social__title">Подписаться на нас</div>
    <div class="social__links">
      <a href="#" class="social__item">
        <img src="@/assets/images/icons/facebook.svg" alt="" />
      </a>
      <a href="#" class="social__item">
        <img src="@/assets/images/icons/odnoklassniki.svg" alt="" />
      </a>
      <a href="#" class="social__item">
        <img src="@/assets/images/icons/twitter.svg" alt="" />
      </a>
      <a href="#" class="social__item">
        <img src="@/assets/images/icons/vkontakte.svg" alt="" />
      </a>
      <a href="#" class="social__item">
        <img src="@/assets/images/icons/whatsapp.svg" alt="" />
      </a>
    </div>
    <div class="text social__about-subs">
      Получайте новые акции и скидки одним из первых
    </div>
    <form class="social__subs-form subs-form" action="#">
      <div class="subs-form__radio-block">
        <input
          v-model="subsWay"
          id="phone"
          type="radio"
          name="subs"
          value="phone"
          class="subs-form__radio-input"
          checked
        />
        <label for="phone">Номер телефона</label>
      </div>
      <div class="subs-form__radio-block">
        <input
          v-model="subsWay"
          id="mail"
          type="radio"
          name="subs"
          class="subs-form__radio-input"
          value="email"
        />
        <label for="mail">Email</label>
      </div>
      <div class="subs-form__input-block">
        <input
          v-if="subsWay === 'email'"
          v-model="email"
          type="email"
          placeholder="Email"
        />
        <input v-else v-model="phone" type="tel" placeholder="Номер телефона" />
      </div>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      subsWay: "phone",
      email: "",
      phone: "",
    };
  },
};
</script>
<style lang="scss" scoped>
.social {
  &__links {
    display: flex;
    margin: 0 0 24px 0;
  }

  &__item {
    margin: 0 16px 0 0;
    &:hover {
      transform: scale(1.1);
    }
  }

  &__about-subs {
    width: 217px;
    margin: 0 0 13px 0;
  }

  &__subs-form {
  }
}
.subs-form {
  &__radio-block {
    display: inline-block;
    margin: 0 23px 13px 0;
    label {
      position: relative;
      font-weight: 700;
      font-size: 15px;
      line-height: 16px;
      text-align: center;
      color: #000000;
      padding: 0 0 0 25px;
    }
    label::before {
      position: absolute;
      left: 0;
      top: 2px;
      content: "";
      width: 15px;
      height: 15px;
      background: #ffffff;
      border: 2px solid #f7f7f7;
      border-radius: 50%;
      transition: all 0.5s ease;
    }
    input:checked + label::before {
      width: 15px;
      height: 15px;
      background: #ffffff;
      border: 5px solid #fb791b;
    }
  }

  &__radio-input {
    display: none;
  }

  &__input-block input {
    width: 282px;
    height: 50px;
    padding: 13px;
    border: 1px solid #e0e0e0;
    border-radius: 4px;
  }
}
</style>