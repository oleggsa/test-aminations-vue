<template>
    <div class="logo">
        <div class="logo-inner">
            <img src="../assets/mozgi.svg" alt="logo">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>
.logo {
  position: absolute;
  left: 50%;
  top: 20px;
  transform: translateX(-50%);
  z-index: 2;
  img {
    @media (max-width: 1024px) {
      width: 69px;
    }
    @media (max-width: 592px) {
      width: 46px;
    }
  }
}
</style>