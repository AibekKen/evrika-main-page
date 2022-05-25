<template >
  <div class="app">
    <header-body />
  </div>
</template>

<script>
import HeaderBody from "./components/HeaderBody.vue";

export default {
  name: "App",
  components: {
    HeaderBody,
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
  transition: all 0.3s ease;
}

.container {
  max-width: 1440px;
  padding: 0 48px;
  margin: 0 auto;
}
</style>
