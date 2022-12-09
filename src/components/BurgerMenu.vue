<template>
  <div class="burger-menu"></div>
</template>

<script>
export default {
  name: "BurgerMenu"
}
</script>

<style lang="scss" scoped>

.burger-menu {
  display: none;
  @media (max-width: 592px) {
    display: block;
  }
  &:before {
    content: url(../assets/line.svg);
    position: fixed;
    top: 20px;
    right: 20px;
  }
  &:after {
    content: url(../assets/line.svg);
    position: fixed;
    top: 10px;
    right: 20px;
  }
}
</style>