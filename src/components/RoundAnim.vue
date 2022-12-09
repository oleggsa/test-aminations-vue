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
  position: absolute;
  z-index: 10;
  left: 60%;
  bottom: 15%;
  &:hover {
    animation: rotation 3s infinite linear;
  }
  .text {
    position: relative;
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