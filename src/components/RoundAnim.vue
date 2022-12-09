<template>
  <div class="round">
    <div class="text">
      <img src="../assets/showreel.svg" alt="showreel">
      <div class="dot"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RoundAnim"
}
</script>

<style lang="scss" scoped>
.round {
  position: fixed;
  z-index: 10;
  bottom: 0;
  right: 20px;
  @media (max-width: 650px) {
    bottom: -20px;
    right: 60px;
  }
  @media (max-width: 592px) {
    bottom: -20px;
    right: 20px;
  }
  &:hover {
    animation: rotation 3s infinite linear;
  }
  .text {
    position: relative;
    img {
      @media (max-width: 1024px) {
        width: 109px;
      }
      @media (max-width: 592px) {
        width: 87px;
      }
    }
    .dot {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 8px;
      height: 8px;
      background: black;
      border-radius: 50%;
    }
  }
}
</style>