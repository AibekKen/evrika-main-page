<template>
  <a
    v-for="product in newProducts"
    :key="product.id"
    class="news-block__item item"
  >
    <div class="item__labels labels">
      <div v-if="product.hit" class="labels__hit">
        <img src="@/assets/images/icons/Хитпродаж.svg" alt="" />
      </div>
      <div v-if="product.new" class="labels__new">
        <img src="@/assets/images/icons/Новинка.svg" alt="" />
      </div>
      <div v-if="product.sale" class="labels__sale">
        <span>{{ product.sale }}</span>
        <img src="@/assets/images/icons/Скидка.svg" alt="" />
      </div>
      <div v-if="product.present" class="labels__present">
        <img src="@/assets/images/icons/Подарок.svg" alt="" />
      </div>
    </div>
    <div class="item__body">
      <div class="item__image">
        <img :src="require(`@/assets/images/${product.image}`)" alt="" />
      </div>
      <div class="item__description">
        {{ product.discript }}
      </div>
      <div v-if="product.exPrice" class="item__count item__count_prev">
        {{ product.exPrice }}
      </div>
      <div class="item__count item__count_current">
        {{ product.currPrice }}
      </div>
    </div>
    <div v-show="product.colors" class="item__colors colors">
      <input
        :id="`pink${product.id}`"
        type="radio"
        :name="product.id"
        value="pink"
        checked
      />
      <label @click.stop class="colors_pink" :for="`pink${product.id}`">
      </label>
      <input
        :id="`white${product.id}`"
        type="radio"
        :name="product.id"
        value="white"
      />
      <label @click.stop class="colors_white" :for="`white${product.id}`">
      </label>
      <input
        :id="`black${product.id}`"
        type="radio"
        :name="product.id"
        value="black"
      />
      <label @click.stop class="colors_black" :for="`black${product.id}`">
      </label>
      <input
        :id="`green${product.id}`"
        type="radio"
        :name="product.id"
        value="green"
      />
      <label @click.stop class="colors_green" :for="`green${product.id}`">
      </label>
    </div>
    <div @click.stop class="item__cart">
      <img src="@/assets/images/icons/cart-icon.svg" alt="" />
    </div>
  </a>
</template>
<script>
export default {
  props: {
    newProducts: {
      type: Array,
    },
  },
};
</script>
<style lang="scss">
.item {
  position: relative;
  width: 262.4px;
  height: 338px;
  background: #ffffff;
  border: 1px solid #f7f7f7;
  border-radius: 8px;
  padding: 235px 0 0 0;
  &__labels {
    position: absolute;
    top: 15px;
    left: -5px;
    z-index: 3;
  }

  &__body {
  }

  &__image {
    position: absolute;
    top: 29px;
    left: 50%;
    transform: translate(-50%, 0);
    margin: 0 0 45px 0;
  }

  &__description {
    width: 220px;
    font-size: 13.6px;
    line-height: 18px;
    letter-spacing: 0.5px;
    color: #000000;
    margin: 0 0 13px 22px;
  }

  &__count {
    margin: 0 0 0 22px;
    &_prev {
      font-size: 19px;
      font-weight: 700;
      line-height: 18px;
      display: flex;
      align-items: center;
      letter-spacing: 0.5px;
      text-decoration-line: line-through;
      color: #999999;
    }

    &_current {
      font-weight: 700;
      font-size: 19px;
      line-height: 18px;
      display: flex;
      align-items: center;
      letter-spacing: 0.5px;
      color: #000000;
    }
  }

  &__colors {
    position: absolute;
    top: 118px;
    right: 15px;
  }

  &__cart {
    position: absolute;
    cursor: pointer;
    right: 20px;
    bottom: 18px;
    transition: all 0.6s ease;
    :hover {
      transform: scale(1.1);
    }
  }
}
.labels {
  &__hit {
  }

  &__new {
  }

  &__sale {
    position: relative;
    span {
      position: absolute;
      display: inline-block;
      top: 50%;
      left: 10%;
      font-size: 10px;
      line-height: 10px;
      font-weight: 800;
      align-items: center;
      text-align: center;
      color: #ffffff;
    }
  }

  &__present {
  }
}

.item {
  &__colors {
  }
}
.colors {
  input {
    display: none;
  }
  label {
    cursor: pointer;
    display: block;
    width: 14px;
    height: 14px;
    border-radius: 50%;
    margin: 0 0 6px 0;
    transition: all 0.5s ease;
  }
  &_pink {
    background: linear-gradient(180deg, #f857a6 0%, #ff5858 100%);
  }

  &_white {
    background: #ffffff;
    border: 0.6px solid rgba(31, 31, 31, 0.12);
  }

  &_black {
    background: linear-gradient(180deg, #232526 0%, #414345 100%);
    border: 0.1px solid rgba(31, 31, 31, 0.12);
  }

  &_green {
    background: linear-gradient(180deg, #34e89e 0%, #0f3443 100%);
  }

  input:checked + label {
    outline: #dee0e6 solid 1px;
    outline-offset: 4px;
    margin: 10px 0;
  }
}
</style>