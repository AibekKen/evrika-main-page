<template>
  <div>
    
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang='scss'>
#app {
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

  .container {
    max-width: 1440px;
    padding: 0 48px;
    margin: 0 auto;
  }
}
</style>
