<template>
  <div class="main" @mousemove="mouseMove">
    <div class="container">
      <Header />
      <div class="main-inner">
        <div class="center">
          <div class="text-main">FULL-CYCLE EVENT AGENCY</div>
          <div class="circle"></div>
        </div>
      </div>
      <Menu />
      <RoundAnim />
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue"
import Menu from "../components/Menu.vue";
import RoundAnim from "../components/RoundAnim.vue";

export default {
  components: {RoundAnim, Menu, Header},
  methods: {
    mouseMove(event) {
      let x = event.clientX;
      let y = event.clientY;
      let text = document.querySelector('.text-main')
      text.style.top = `${49.8 + y/2000}%`;
      text.style.left = `${49.7 + x/2000}%`;
    }
  }
}
</script>

<style lang="scss" scoped>
.main {
  background: #BEBEBE;
  background-size: 100% 100%;
  &-inner {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.text-main {
  font-size: 82px;
  position: absolute;
  z-index: 1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  width: 100%;
  max-width: 1024px;
  min-width: 300px;
}
.circle {
  border-radius: 50%;
  width: 578px;
  height: 578px;
  background: #FFCB46;
  filter: blur(38px);
  font-size: 30px;
}

.container {
  padding: 24px 19px 19px;
  height: 100vh;
  text-align: center;
}
</style>