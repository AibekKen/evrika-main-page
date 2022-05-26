<template>
  <div class="header">
    <header-top />
    <header-bottom />
  </div>
</template>
<script>
import HeaderTop from "@/components/HeaderTop.vue";
import HeaderBottom from "@/components/HeaderBottom.vue";
export default {
  components: { HeaderTop, HeaderBottom },
};
</script>
<style lang="scss" scoped>
.header {
  margin-bottom: 24px;
}
</style>