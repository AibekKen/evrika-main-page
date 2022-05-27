<template>
  <div class="header-bottom">
    <div class="container">
      <div class="header-bottom__body">
        <div class="header-bottom__column logo">
          <img src="@/assets/images/icons/evrika-logo.svg" alt="" />
        </div>
        <form @submit.prevent class="header-bottom__column search">
          <input
            v-model="searchValue"
            type="search"
            name=""
            id="search__input"
            class="search__input"
            placeholder="Ищите среди 10 000 товаров..."
          />
          <button type="submit" class="search__icon">
            <img src="@/assets/images/icons/search-icon.svg" alt="" />
          </button>
        </form>
        <div class="header-bottom__column indicators">
          <a href="#" class="indicators__icon user">
            <img src="@/assets/images/icons/user.svg" alt="" />
          </a>
          <a href="#" class="indicators__icon scale">
            <img src="@/assets/images/icons/scales-icon.svg" alt="" />
          </a>
          <a href="#" class="indicators__icon wish">
            <img src="@/assets/images/icons/wish-icon.svg" alt="" />
          </a>
          <a href="#" class="indicators__icon cart">
            <img src="@/assets/images/icons/cart-icon1.svg" alt="" />
          </a>
          <a href="#" class="indicators__icon cart-info">
            <div class="cart-info__name">Корзина</div>
            <div class="cart-info__summ">0</div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      searchValue: "",
    };
  },
};
</script>
<style lang="scss" scoped>
.header {
  &-bottom {
    padding: 15px 0 0 0;
    height: 77px;
    background: #029aad;
    &__body {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
}
.logo {
  align-self: start;
}
.search {
  flex: 0 1 calc((675 / 1344) * 100%);
  display: flex;
  align-items: center;
  height: 48px;
  background: #ffffff;
  border: 1px solid #ffffff;
  border-radius: 8px;
  padding: 0 13px 0 16px;
  &__input {
    width: 100%;
    font-size: 16px;
    line-height: 22px;
    letter-spacing: -0.0041em;
    &::placeholder {
      color: #aeaeb2;
    }
    &:focus::placeholder {
      opacity: 0;
    }
  }

  &__icon {
    background: transparent;
  }

  &__icon svg {
    fill: #fb791b;
  }
}
.indicators {
  flex: 0 1 calc((268 / 1344) * 100%);
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__icon img:hover {
    filter: brightness(0) saturate(100%) invert(62%) sepia(45%) saturate(5449%)
      hue-rotate(350deg) brightness(105%) contrast(97%);
  }
}
.user {
}
.scale {
}
.wish {
}
.cart {
}
.cart-info {
  &__name {
    font-weight: 800;
    font-size: 16px;
    line-height: 10px;
    display: flex;
    align-items: center;
    color: #ffffff;
    margin: 0 0 10px 0;
    &:hover {
      color: #fb791b;
    }
  }

  &__summ {
    font-size: 11px;
    line-height: 10px;
    display: flex;
    align-items: center;
    color: #e0e0e0;
  }
}
</style>