<template>
  <section class="hero">
    <h1>
      <span>Jackson Bruno</span>, <br />
      Front-end <i>/</i> UI Design
    </h1>
    <p>
      Sou responsável por dar vida ao seu projeto. Transformo design em páginas
      para a web com agilidade, qualidade e alta perfomance.
    </p>
    <button class="btn">peça um orçamento</button>
  </section>
</template>

<script>
export default {
  name: "Hero"
};
</script>

<style lang="scss" scoped>
.hero {
  h1 {
    text-align: center;
    font-size: 4.5rem;
    line-height: 72px;
    span {
      font-size: 4.5rem;
      background: linear-gradient(99.56deg, #7474bf -5.2%, #348ac7 128.15%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    i {
      font-size: 4.5rem;
      font-weight: 100;
    }
  }
  p {
    margin: 0 auto;
    max-width: 600px;
    text-align: center;
    padding: 32px 0px 64px 0px;
    line-height: 24px;
    color: var(--lighter);
  }
}
</style>
