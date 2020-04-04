<template>
  <header class="wrapper">
    <div class="container">
      <div class="content">
        <Hero />
        <!-- <div class="mouse"></div> -->
      </div>
    </div>
  </header>
</template>

<script>
import Hero from "@/components/Header/Hero";
export default {
  name: "Header",
  components: {
    Hero
  }
};
</script>

<style lang="scss" scoped>
.wrapper {
  width: 100%;
}
.content {
  width: 100%;
  height: 700px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
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
