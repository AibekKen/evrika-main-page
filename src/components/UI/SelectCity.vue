<template>
  <div class="city">
    <div class="city__geotag-icon">
      <img src="@/assets/images/icons/geotag-icon.svg" alt="" />
    </div>
    <select id="select-city" class="city__select">
      <option v-for="city in cities" :key="city" :value="city">
        {{ city }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  name: "SelectCity",
  props: {
    cities: {
      type: Array,
    },
  },
};
</script>
<style lang="scss" scoped>
  .city {
  display: inline-flex;
  height: 32px;
  padding: 7px 10px;
  border: 1px solid #e0e0e0;
  border-radius: 30px;
  &__geotag-icon {
    display: inline-block;
  }
  &__select {
    display: inline-block;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    font-size: 16px;
    letter-spacing: -0.04em;
    color: #999999;
  }
}
</style>