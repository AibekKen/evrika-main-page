<template>
  <div>
    <aside class="sidebar">
      <ul class="sidebar__category-list category-list">
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/smariphones-icon.svg" alt="" />
            <span> Смартфоны и гаджеты</span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/tv-icon.svg" alt="" />
            <span> Телевизоры, аудио и видео</span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/fridge-icon.svg" alt="" />
            <span> Бытовая техника </span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/vacuum-icon.svg" alt="" />
            <span> Мелкобытовая техника </span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/photo-icon.svg" alt="" />
            <span> Фотоаппараты, видеокамеры </span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/car-icon.svg" alt="" />
            <span> Автотовары и инструменты </span>
          </a>
        </li>
        <li>
          <a href="" class="category-list__point point">
            <img src="@/assets/images/icons/games-icon.svg" alt="" />
            <span> Игры и приставки </span>
          </a>
        </li>
      </ul>
    </aside>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.sidebar {
  height: 100%;
  &__category-list {
    padding: 18px 16px 16px 18px;
    gap: 10px;
    width: 275px;
    background: #ffffff;
    border-radius: 8px;
  }
}
.category-list {
  height: 100%;
  li {
    position: relative;
    margin: 0 0 19px 0;
    &:hover {
      background: #ebe7e7b1;
    }
    &:hover::after {
      background: url(@/assets/images/curve-right-20-hover.svg) 0 3px / contain;
    }
  }
  li::after {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    width: 20px;
    height: 20px;
    background: url(@/assets/images/curve-right-20.svg) 0 3px / contain
      no-repeat;
  }
  &__point img {
    display: inline-block;
    margin-right: 9px;
  }
}
.point {
  font-size: 13px;
  line-height: 17px;
  color: #000000;
}
.point:hover {
}
</style>