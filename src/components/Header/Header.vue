<template>
  <header class="wrapper">
    <div class="container">
      <div class="content">
        <Hero />
        <div class="box-mouse">
          <Mouse />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import Hero from "@/components/Header/Hero";
import Mouse from "@/components/Global/Mouse";
export default {
  name: "Header",
  components: {
    Hero,
    Mouse
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
.box-mouse {
  position: absolute;
  width: 100%;
  height: 700px;
  z-index: -1;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  margin-top: -32px;
}
</style>
