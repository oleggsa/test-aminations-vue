<template>
  <div>
    <nav class="menu">
      <ul>
        <li class="item-1">
          <router-link
              class="hover-underline-animation"
              to="/test"
          >
            where?
          </router-link>
        </li>
        <li class="item-2">
          <router-link
              class="hover-underline-animation"
              to="/test"
          >
            who?
          </router-link>
        </li>
        <li class="item-3">
          <router-link
              class="hover-underline-animation"
              to="/test"
          >
            what?
          </router-link>
        </li>
      </ul>
    </nav>
    <BurgerMenu />
  </div>
</template>

<script>
import BurgerMenu from "./BurgerMenu.vue";
export default {
  name: "Menu",
  components: {BurgerMenu},
}
</script>

<style lang="scss" scoped>
ul {
  @media (max-width: 592px) {
    display: none;
  }
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
    left: -20px;
    top: 50%;
    transform: translateY(-50%) rotate(270deg);
    @media (max-width: 1024px) {
      left: -30px;
    }
  }
  .item-2 {
    left: 50%;
    bottom: 20px;
    transform: translateX(-50%);
    @media (max-width: 1024px) {
      bottom: 10px;
    }
  }
  .item-3 {
    right: -20px;
    top: 50%;
    transform: translateY(-50%) rotate(90deg);
    @media (max-width: 1024px) {
      right: -30px;
    }
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