<template>
  <div>
    <div class="circle"></div>
    <RoundAnim />
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
.circle {
  border-radius: 50%;
  width: 578px;
  height: 578px;
  background: #FFCB46;
  filter: blur(38px);
  font-size: 30px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  @media (max-width: 1024px) {
    width: 482px;
    height: 482px;
  }
  @media (max-width: 592px) {
    width: 294px;
    height: 294px;
  }
}
</style>