<template >
  <div class="app">
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
  },
  data() {
    return {
      cities: ["Алматы", "Нур-Султан", "Караганды", "Актау", "Атырау"],
      contacts: ["7 707 777 77 77", "8 808 000 00 00"],
    };
  },
};
</script>

<style lang='scss'>
.app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;

  $fontfamily: "Manrope";
  $minwidth: 320px;

  @import "@/assets/styles/fonts.scss";
  @import "@/assets/styles/nullstyle.scss";
  font-family: $fontfamily;
  font-weight: 400;
  font-size: 50px;
  transition: all 0.3s ease;
  .container {
    max-width: 1440px;
    padding: 0 48px;
    margin: 0 auto;
  }
}

.header {
  &__row {
    &_top {
      height: 52px;
    }
  }
}
</style>
