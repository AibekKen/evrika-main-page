<template>
  <div class="header-top">
    <div class="container">
      <div class="header-top__body">
        <select-city :cities="cities" />
        <consult-help :contacts="contacts" />
      </div>
    </div>
  </div>
</template>
<script>
import SelectCity from "@/components/UI/SelectCity.vue";
import ConsultHelp from "@/components/UI/ConsultHelp.vue";

export default {
  components: {
    SelectCity,
    ConsultHelp,
  },
  data() {
    return {
      cities: ["Алматы", "Нур-Султан", "Караганды", "Актау", "Атырау"],
      contacts: ["7 707 777 77 77", "8 808 000 00 00"],
    };
  },
};
</script>
<style lang="scss" scoped>
.header {
  &-top {
    &__body {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 52px;
      background: #f7f7f7;
    }
  }
}
</style>