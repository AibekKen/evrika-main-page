<template>
  <div class="footer__footer-bottom footer-bottom">
    <div class="container">
      <div class="footer-bottom__body">
        <div class="footer-bottom__column">
          <div class="footer-logo">
            <img src="@/assets/images/icons/evrika-logo.svg" alt="" />
          </div>
        </div>
        <div class="footer-bottom__column">
          <a class="footer-bottom__link" href="#"
            >Политика конфиденциальности</a
          >
          <a class="footer-bottom__link" href="#">Карта сайта</a>
        </div>
        <div class="footer-bottom__column">
          Copyright © 2013 - 2022 ТОО Компания Эврика
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.footer {
  &__footer-bottom {
  }
}
.footer-bottom {
  padding: 36px 0;
  background: #141a38;
  &__body {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__column {
    font-family: "Inter";
    font-weight: 400;
    font-size: 10px;
    line-height: 17px;
    letter-spacing: 0.05em;
    color: #ffffff;
  }

  &__link {
    font-family: "Inter";
    font-weight: 400;
    font-size: 10px;
    line-height: 17px;
    letter-spacing: 0.05em;
    color: #ffffff;
  }
  &__link:hover {
    color: #fb791b;
  }

  &__link::after {
    content: " • ";
  }
  &__link:last-child:after {
    content: "";
  }
}
.container {
}
.footer-logo {
  width: 100px;
  height: 18px;
  & img {
    width: 100%;
  }
}
</style>