<template>
  <nav class="navigation">
    <div class="container">
      <div class="content">
        <Brand />
        <div @click="MenuActive" class="menu-mobile">
          <div class="row"></div>
          <div class="row"></div>
          <div class="row"></div>
        </div>
        <transition name="bounce" mode>
          <Sidebar :active="active" />
        </transition>
        <div class="menu">
          <ul>
            <li>
              <a href="#about">quem sou</a>
            </li>
            <li>
              <a href="#cases">portfólio</a>
            </li>
            <li>
              <a href="#contact">contato</a>
            </li>
            <div class="separetion">
              <div></div>
              <div></div>
              <div></div>
            </div>
            <li>
              <a href="#">peça um orçamento</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import Brand from "@/components/Global/Brand";
import Sidebar from "@/components/Header/Sidebar";
export default {
  name: "Navbar",
  components: {
    Brand,
    Sidebar
  },
  data() {
    return {
      active: false
    };
  },
  methods: {
    MenuActive() {
      this.active = !this.active;
    }
  }
};
</script>

<style lang="scss" scoped>
.navigation {
  width: 100%;
  position: absolute;
}
.content {
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 15px;
}
.menu ul {
  display: flex;
}
.menu ul li a {
  margin-left: 32px;
  font-size: 1rem;
  color: var(--light);
  text-transform: uppercase;
  font-weight: 500;
  transition: 0.3s;
  &:hover {
    color: var(--primary);
    transition: 0.3s;
  }
}
.separetion {
  display: flex;
  flex-direction: column;
  position: relative;
  > div {
    width: 3px;
    height: 3px;
    border-radius: 50px;
    margin-bottom: 5px;
    margin-left: 32px;
    background: var(--light);
  }
}
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
/* Responsive */
@media (max-width: 963px) {
  .menu {
    display: none;
  }
  .menu-mobile {
    z-index: 999;
    position: fixed;
    right: 15px;
    cursor: pointer;
    width: 45px;
    background: var(--darker);
    padding: 5px;
    .row {
      width: 100%;
      height: 3px;
      background: var(--light);
      margin: 7px 0px;
    }
    :nth-of-type(3) {
      width: 80%;
    }
  }
}
</style>
