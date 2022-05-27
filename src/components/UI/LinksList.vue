<template>
  <div class="footer-bottom__column links-block">
    <div class="subtitle links-block__title">
      {{ listBlock.title }}
    </div>
    <ul class="links-block__list">
      <li v-for="link in listBlock.links" :key="link">
        <a href="#" class="text links-block__link">{{ link }}</a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    listBlock: {
      type: Object,
    },
  },
};
</script>
<style lang="scss">
.footer-bottom {
  &__column {
  }
}
.links-block {
  &__title {
  }

  &__list {
  }

  &__link:hover {
    color: #fb791b;
  }
}
.subtitle {
}
.text {
}
</style>