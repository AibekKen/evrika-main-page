<template>
  <div class="brands">
    <div class="brands__body">
      <div v-for="brand in brands" :key="brand" class="brands__company company">
        <img :src="require(`@/assets/images/icons/${brand}`)" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      brands: [
        "bosch-logo.svg",
        "oppo-logo.svg",
        "huawei-logo.svg",
        "xiomi-logo.svg",
        "samsung-logo.svg",
        "lg-logo.svg",
        "philips-logo.svg",
        "lenovo-logo.svg",
        "tefal-logo.svg",
        "asus-logo.svg",
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.brands {
  &__body {
    display: flex;
    justify-content: space-between;
  }

  &__company {
    display: flex;
    align-items: center;
  }
}

.company {
  height: 70px;
  padding: 0 16px;
  background: #ffffff;
  box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.1),
    0px 1px 2px -1px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  img {
    display: inline-block;
  }
}
</style>