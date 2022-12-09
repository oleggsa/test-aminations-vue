<template>
  <div class="main" @mousemove="mouseMove">
    <BkgText />
    <LangSwitch />
    <Header />
    <div class="container">
      <div class="main-inner">
        <div class="center">
          <div class="text-main">FULL-CYCLE EVENT AGENCY</div>
          <BkgCircle />
        </div>
      </div>
      <Menu />
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue"
import Menu from "../components/Menu.vue";
import BkgText from "../components/BkgText.vue";
import LangSwitch from "../components/LangSwitch.vue";
import BkgCircle from "../components/BkgCircle.vue";

export default {
  components: {BkgCircle, LangSwitch, BkgText, Menu, Header},
  methods: {
    mouseMove(event) {
      let x = event.clientX;
      let y = event.clientY;
      const ratio = 2000;
      let text = document.querySelector('.text-main')
      text.style.top = `${49.8 + y/ratio}%`;
      text.style.left = `${49.7 + x/ratio}%`;
    }
  }
}
</script>

<style lang="scss" scoped>
.main {
  background: #BEBEBE;
  background-size: 100% 100%;
  overflow: hidden;
  position: relative;
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
  padding: 25px;
  //@media (max-width: 1100px) {
  //  max-width: 968px;
  //}
  @media (max-width: 1024px) {
    font-size: 58px;
    max-width: 800px;
  }
  //@media (max-width: 768px) {
  //  max-width: 700px;
  //}
  @media (max-width: 592px) {
    font-size: 34px;
    max-width: 500px;
  }
}

.container {
  padding: 24px 19px 19px;
  height: 100vh;
  position: relative;
}
</style>