<template>
  <nav class="menu">
    <ul>
      <li class="item-1"><router-link class="hover-underline-animation" to="/test">where?</router-link></li>
      <li class="item-2"><router-link class="hover-underline-animation" to="/test">who?</router-link></li>
      <li class="item-3"><router-link class="hover-underline-animation" to="/test">what?</router-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Menu",
}
</script>

<style lang="scss" scoped>
ul {
  li {
    list-style-type: none;
    position: absolute;
    z-index: 2;
    a {
      text-decoration: none;
      color: #373737;
      &:hover {
        color: white;
        transition: 0.2s;
      }
    }
  }
  .item-1 {
    left: 0;
    top: 50%;
    transform: rotate(270deg);
  }
  .item-2 {
    left: 50%;
    bottom: 19px;
  }
  .item-3 {
    right: 0;
    top: 50%;
    transform: rotate(90deg);
  }
}
.hover-underline-animation {
  display: inline-block;
  position: relative;
}

.hover-underline-animation::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #fff;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>