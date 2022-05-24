<template>
  <div>
    <div class="help">
      <div class="help__icon">
        <img src="@/assets/images/icons/phone-icon.svg" alt="" />
      </div>
      <select v-model="selectedCity" id="select-help" class="help__select">
        <option value="help" selected disabled>Помощь и консультация</option>
        <option v-for="contact in contacts" :key="contact" :value="contact">
          {{ contact }}
        </option>
      </select>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selectedCity: "help",
    };
  },
  props: {
    contacts: {
      type: Array,
    },
  },
};
</script>
<style lang="scss" scoped>
.help {
  display: inline-flex;
  height: 32px;
  padding: 4px 10px;
  border: 1px solid #e0e0e0;
  border-radius: 30px;
  &__icon {
    display: inline-block;
  }
  &__select {
    display: inline-block;
    font-size: 16px;
    letter-spacing: -0.04em;
    color: #999999;
  }
  &:hover {
    background: rgb(23, 169, 231);
    .help__select {
      background: rgb(23, 169, 231);
      color: rgb(255, 255, 255);
    }
  }
}
</style>