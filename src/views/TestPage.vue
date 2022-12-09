<template>
  <div class="test">
    <h1>Test</h1>
    <h2><router-link to="/">Home</router-link></h2>
  </div>
</template>

<script>
export default {
  name: "TestPage"
}
</script>

<style lang="scss" scoped>
.test {
  background: #BEBEBE;
  background-size: 100% 100%;
  height: 100vh;
  width: 100vw;
  overflow: hidden;
}
h1, h2 {
  position: relative;
  text-align: center;
  padding-top: 200px;
}
</style>