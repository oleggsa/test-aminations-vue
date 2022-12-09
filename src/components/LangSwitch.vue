<template>
  <div class="button">
    <div class="img">
      <img src="../assets/tongue.svg" alt="tongue">
    </div>
  </div>
</template>

<script>
export default {
  name: "LangSwitch"
}
</script>

<style lang="scss" scoped>
.button {
  position: absolute;
  top: 28px;
  left: 24px;
  height: 38px;
  width: 38px;
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  img {
    opacity: 1;
  }
}
</style>