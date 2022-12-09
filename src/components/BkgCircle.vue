<template>
  <div class="circle"></div>
</template>

<script>
export default {
  name: "BkgCircle"
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
  @media (max-width: 1024px) {
    width: 482px;
    height: 482px;
  }
}
</style>