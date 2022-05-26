<template>
  <div class="news-block">
    <div class="news-block__title title">Новинки</div>
    <div class="news-block__body">
      <product-card :newProducts="newProducts" />
    </div>
  </div>
</template>
<script>
import ProductCard from "@/components/UI/ProductCard.vue";
export default {
  components: {
    ProductCard,
  },
  data() {
    return {
      newProducts: [
        {
          id: 1,
          image: "tab.png",
          discript: "Планшет Samsung Galaxy Tab S8 11 128GB Silver (SM-X706)",
          exPrice: "599 890 ₸",
          currPrice: "499 890 ₸",
          hit: true,
          new: true,
          sale: "-20%",
          present: true,
          colors: true,
        },
        {
          id: 2,
          image: "kitchen-rob.png",
          discript: "Планшет Samsung Galaxy Tab S8 11 128GB Silver (SM-X706)",
          exPrice: "599 890 ₸",
          currPrice: "499 890 ₸",
          hit: false,
          new: false,
          sale: false,
          present: true,
          colors: false,
        },
        {
          id: 3,
          image: "iphone13.png",
          discript: "Смартфон Iphone 13 mini 128GB Slim Box Pink",
          exPrice: false,
          currPrice: "499 890 ₸",
          hit: true,
          new: false,
          sale: false,
          present: false,
          colors: true,
        },
        {
          id: 4,
          image: "lg-nano.png",
          discript: "Телевизор LG NANO 50NANO806PA",
          exPrice: false,
          currPrice: "549 890 ₸",
          hit: true,
          new: false,
          sale: "-20%",
          present: true,
          colors: true,
        },
        {
          id: 5,
          image: "tab.png",
          discript: "Планшет Samsung Galaxy Tab S8 11 128GB Silver (SM-X706)",
          exPrice: "599 890 ₸",
          currPrice: "499 890 ₸",
          hit: false,
          new: true,
          sale: false,
          present: false,
          colors: true,
        },
        {
          id: 6,
          image: "dyson.png",
          discript: "Фен Dyson HD07 Supersonic фуксия/никель",
          exPrice: false,
          currPrice: "357 990 ₸",
          hit: false,
          new: true,
          sale: false,
          present: false,
          colors: true,
        },
        {
          id: 7,
          image: "iphon13mini.png",
          discript: "Смартфон Iphone 13 mini 128GB Slim Box Pink",
          exPrice: "599 890 ₸",
          currPrice: "499 890 ₸",
          hit: false,
          new: false,
          sale: "-20%",
          present: true,
          colors: true,
        },
        {
          id: 8,
          image: "washing-machine.png",
          discript: "Стиральная машина Samsung WW90T986CSX",
          exPrice: false,
          currPrice: "659 990 ₸",
          hit: false,
          new: true,
          sale: "-20%",
          present: false,
          colors: true,
        },
        {
          id: 10,
          image: "tab.png",
          discript: "Планшет Samsung Galaxy Tab S8 11 128GB Silver (SM-X706)",
          exPrice: "599 890 ₸",
          currPrice: "499 890 ₸",
          hit: true,
          new: true,
          sale: "-20%",
          present: true,
          colors: true,
        },
        {
          id: 11,
          image: "kitchen-rob.png",
          discript: "Планшет Samsung Galaxy Tab S8 11 128GB Silver (SM-X706)",
          exPrice: false,
          currPrice: "359 990 ₸",
          hit: true,
          new: false,
          sale: false,
          present: false,
          colors: false,
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.news-block {
  &__body {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 0 -8px 0 0;
  }
  &__title {
    margin: 0 0 5px 3px;
  }
  &__item {
    margin: 0 8px 8px 0;
  }
}
</style>