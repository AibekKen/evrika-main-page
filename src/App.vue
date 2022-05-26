<template >
  <div class="app">
    <header-body />
    <div class="container">
      <div class="block">
        <sidebar-category />
        <big-banner />
      </div>
      <news-block />
    </div>
  </div>
</template>

<script>
import HeaderBody from "./components/HeaderBody.vue";
import SidebarCategory from "./components/SidebarCategory.vue";
import BigBanner from "./components/BigBanner.vue";
import NewsBlock from "./components/NewsBlock.vue";

export default {
  name: "App",
  components: {
    HeaderBody,
    SidebarCategory,
    BigBanner,
    NewsBlock,
  },
};
</script>
<style lang='scss'>
.app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 100%;
  background: #f7f7f7;

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

.block {
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  margin: 0 0 32px 0;
}

.title {
  font-weight: 800;
  font-size: 28.5px;
  color: #000000;
}
</style>
