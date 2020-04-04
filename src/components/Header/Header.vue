<template>
  <header class="wrapper">
    <div class="container">
      <div class="content">
        <Hero />
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
</style>
