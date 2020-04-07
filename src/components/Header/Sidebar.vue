<template>
  <nav class="sidebar-menu" v-if="active">
    <div class="content">
      <ul class="menu">
        <li>
          <a href="#about">quem sou</a>
        </li>
        <li>
          <a href="#cases">portfólio</a>
        </li>
        <li>
          <a href="#contact">contato</a>
        </li>
      </ul>
      <button class="btn">peça um orçamento</button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "sidebar-menu",
  props: ["active"]
};
</script>

<style lang="scss" scoped>
.sidebar-menu {
  z-index: 998;
  position: fixed;
  background: var(--dark);
  width: 100%;
  top: 0;
  right: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.menu {
  text-align: center;
  > li {
    color: #fff;
    > a {
      display: block;
      font-size: 1.5rem;
      color: var(--light);
      text-transform: uppercase;
      font-weight: 500;
      margin: 32px 0px;
      transition: 0.2s linear;
      &:hover {
        color: var(--primary);
        transition: 0.2s linear;
      }
    }
  }
}
/* Responsive */
@media (max-width: 963px) {
}
</style>