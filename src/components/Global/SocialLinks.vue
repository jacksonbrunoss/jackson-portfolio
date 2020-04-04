<template>
  <div class="social">
    <ul>
      <li>
        <a href="#">
          <i class="bx bxl-facebook"></i>
        </a>
      </li>
      <li>
        <a href="#">
          <i class="bx bxl-twitter"></i>
        </a>
      </li>
      <li>
        <a href="#">
          <i class="bx bxl-linkedin"></i>
        </a>
      </li>
      <li>
        <a href="#">
          <i class="bx bxl-github"></i>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SocialLinks"
};
</script>

<style lang="scss" scoped>
.social ul {
  display: flex;
  > li a i {
    color: var(--light);
    font-size: 2rem;
    margin: 10px 32px 10px 0px;
    transition: 0.3s linear;
    &:hover {
      color: var(--primary);
      transition: 0.3s linear;
    }
  }
}
</style>