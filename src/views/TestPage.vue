<template>
  <div class="test">
    <h1>Test</h1>
    <h1><router-link to="/">Home</router-link></h1>
  </div>
</template>

<script>
export default {
  name: "TestPage"
}
</script>

<style lang="scss" scoped>
.test {
  position: absolute;
  top: 50%;
  left: 50%;
  text-align: center;
  transform: translate(-50%, -50%);
}
</style>