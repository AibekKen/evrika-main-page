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
            <svg
              width="23"
              height="25"
              viewBox="0 0 23 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_512_1146)">
                <path
                  d="M21.4124 26.1905H18.9181V23.6962C18.9181 22.7038 18.5238 21.7521 17.8222 21.0505C17.1205 20.3488 16.1688 19.9546 15.1766 19.9546H7.6936C6.70133 19.9546 5.74967 20.3488 5.048 21.0505C4.34634 21.7521 3.95205 22.7038 3.95205 23.6962V26.1905H1.45776V23.6962C1.45776 22.0423 2.11475 20.4562 3.28419 19.2868C4.4536 18.1173 6.03979 17.4604 7.6936 17.4604H15.1766C16.8304 17.4604 18.4166 18.1173 19.586 19.2868C20.7554 20.4562 21.4124 22.0423 21.4124 23.6962V26.1905ZM11.4351 14.966C10.4524 14.966 9.47931 14.7724 8.57145 14.3964C7.6636 14.0204 6.83872 13.4692 6.14384 12.7743C5.44895 12.0794 4.89776 11.2545 4.52169 10.3467C4.14562 9.43869 3.95205 8.46571 3.95205 7.48298C3.95205 6.50036 4.14562 5.52725 4.52169 4.61938C4.89776 3.7115 5.44895 2.88658 6.14384 2.19171C6.83872 1.49686 7.6636 0.945666 8.57145 0.569607C9.47931 0.193547 10.4524 0 11.4351 0C13.4197 0 15.323 0.788381 16.7263 2.19171C18.1297 3.59505 18.9181 5.49838 18.9181 7.48298C18.9181 9.46762 18.1297 11.371 16.7263 12.7743C15.323 14.1776 13.4197 14.966 11.4351 14.966ZM11.4351 12.4717C12.7581 12.4717 14.0271 11.9461 14.9626 11.0105C15.8981 10.075 16.4237 8.80607 16.4237 7.48298C16.4237 6.15988 15.8981 4.89104 14.9626 3.95548C14.0271 3.01992 12.7581 2.49433 11.4351 2.49433C10.1121 2.49433 8.84312 3.01992 7.90753 3.95548C6.97205 4.89104 6.44645 6.15988 6.44645 7.48298C6.44645 8.80607 6.97205 10.075 7.90753 11.0105C8.84312 11.9461 10.1121 12.4717 11.4351 12.4717Z"
                  fill="white"
                />
              </g>
              <defs>
                <clipPath id="clip0_512_1146">
                  <rect
                    width="21.4286"
                    height="25"
                    fill="white"
                    transform="translate(0.725342)"
                  />
                </clipPath>
              </defs>
            </svg>
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
  &__icon img {
    fill: #fb791b;
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