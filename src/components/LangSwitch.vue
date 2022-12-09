<template>
  <div class="button">
    <div class="lang-wrapper">
      <div class="img">
        <img src="../assets/tongue.svg" alt="tongue">
        <div class="button-hover">
          <button>UA</button>
          <button>EN</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LangSwitch"
}
</script>

<style lang="scss" scoped>
.img {
  display: flex;
  position: relative;
  z-index: 1;
}
.button {
  position: absolute;
  top: 28px;
  left: 24px;
  .lang-wrapper {
    position: relative;
    &:after {
      content: "";
      position: absolute;
      height: 38px;
      width: 38px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      border-radius: 50%;
      top: -12px;
      left: -13px;
    }
    &:hover .button-hover {
      left: 15px;
      opacity: 1;
      z-index: 1;
      animation: 1s changeLanguage forwards;
    }
    &:hover:after {
      width: 130px;
      border-radius: 10px;
    }
  }
  img {
    opacity: 1;
  }
  @media (max-width: 1024px) {
    top: 27px;
    left: 26px;
    height: 34px;
    width: 34px;
  }
  @media (max-width: 592px) {
    top: 25px;
    left: 26px;
  }
  .button-hover {
    position: absolute;
    opacity: 0;
    z-index: -100;
    left: -1000px;
    display: flex;
    flex-direction: row;
    button {
      display: inline-block;
      background: transparent;
      border: none;
      margin-left: 15px;
      cursor: pointer;
    }
  }
}
</style>