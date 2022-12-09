<template>
  <div class="circle-main">
    <div class="circle-wrapper">
      <div class="circle"></div>
      <RoundAnim />
    </div>
  </div>
</template>

<script>
import RoundAnim from "./RoundAnim.vue";
export default {
  name: "BkgCircle",
  components: {RoundAnim}
}
</script>

<style lang="scss" scoped>
.circle-main {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.circle-wrapper {
  position: relative;
  width: 578px;
  height: 578px;
  @media (max-width: 1024px) {
    width: 482px;
    height: 482px;
  }
  @media (max-width: 592px) {
    width: 294px;
    height: 294px;
  }
}
.circle {
  border-radius: 50%;
  background: #FFCB46;
  filter: blur(38px);
  font-size: 30px;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  @media (max-width: 592px) {
    filter: blur(23.1784px);
  }
}
</style>