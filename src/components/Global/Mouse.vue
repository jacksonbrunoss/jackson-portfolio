<template>
  <div class="mouse"></div>
</template>

<script>
export default {
  name: "Mouse"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.mouse {
  bottom: 0;
  position: relative;
  width: 30px;
  height: 60px;
  border: 1px solid var(--light);
  border-radius: 30px;
  overflow: hidden;
  &:before {
    content: "";
    position: absolute;
    width: 3px;
    height: 8px;
    background: var(--light);
    border-radius: 30px;
    left: 50%;
    top: 10%;
    transform: translate(-50%, 0);
    animation: animate 2s linear infinite;
  }
}
@keyframes animate {
  0% {
    transform: translate(-50%, 0px);
  }
  70% {
    transform: translate(-50%, 10px);
  }
}
</style>
