<template>
<div class="parent">
  <div class="line1">
    <span class="text3">FULL-CYCLE EVENT AGENCY FULL-CYCLE EVENT AGENCY</span>
    <span class="text4">FULL-CYCLE EVENT AGENCY FULL-CYCLE EVENT AGENCY </span>
  </div>
  <div class="line2">
    <span class="text">FULL-CYCLE EVENT AGENCY FULL-CYCLE EVENT AGENCY</span>
    <span class="text2">FULL-CYCLE EVENT AGENCY FULL-CYCLE EVENT AGENCY</span>
  </div>
</div>
</template>

<script>
export default {
  name: "BkgText"
}
</script>

<style lang="scss" scoped>
.parent {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%) rotate(-0.13turn);
  width: 2000px;
  //transform: rotate(200);
}

.line1, .line2 {
  width: 100%;
  white-space: nowrap;
  font-weight: bold;
  font-style: italic;
  font-size: 52px;
  -webkit-text-stroke: 2px #373737;
  opacity: 0.1;
  color: transparent;
}

.text, .text2 {
  display:inline-block;
  animation: 26s moveDiagonally infinite linear;
}
.text2 {
  animation: 26s moveDiagonallySecond infinite linear;
  animation-delay: 13s;
}

.text3, .text4 {
  display:inline-block;
  animation: 26s moveDiagonallyReverse infinite linear;
}
.text4 {
  animation: 26s moveDiagonallyReverseSecond infinite linear;
  animation-delay: 13s;
}

</style>