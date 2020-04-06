<template>
  <section class="portfolio">
    <div class="container">
      <Title :title="title" />
      <Carousel />
    </div>
  </section>
</template>

<script>
import Title from "@/components/Global/Title";
import Carousel from "@/components/Portfolio/Carousel";
export default {
  name: "Portfolio",
  components: {
    Carousel,
    Title,
  },
  data() {
    return {
      title: "Portfólio",
    };
  },
};
</script>

<style lang="scss" scoped>
.portfolio {
  width: 100%;
  padding: 96px 15px;
}
</style>
