<template>
  <nav class="navigation">
    <div class="container">
      <div class="content">
        <Brand />
        <div class="menu">
          <ul>
            <li>
              <a href="#">quem sou</a>
            </li>
            <li>
              <a href="#">portfólio</a>
            </li>
            <li>
              <a href="#">contato</a>
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
export default {
  name: "Navbar",
  components: {
    Brand
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
</style>
