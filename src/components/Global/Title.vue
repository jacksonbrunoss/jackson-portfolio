<template>
  <h2 class="title">
    {{title}}
    <i>.</i>
  </h2>
</template>

<script>
export default {
  name: "Title",
  props: {
    title: String
  }
};
</script>

<style lang="scss" scoped>
.title {
  font-size: 3.5rem;
  font-weight: 500;
  padding-bottom: 2.5rem;
  > i {
    color: var(--primary);
    font-size: 3.5rem;
    font-style: normal;
  }
}
</style>