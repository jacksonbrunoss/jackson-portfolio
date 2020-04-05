<template>
  <footer class="footer">
    <div class="container">
      <div class="content">
        <p>&#169; Copyright {{ano}} - Todos os direitos reservados.</p>
        <Brand />
      </div>
    </div>
  </footer>
</template>

<script>
import Brand from "@/components/Global/Brand";
export default {
  name: "Footer",
  components: {
    Brand
  },
  data() {
    return {
      ano: ""
    };
  },
  methods: {
    Year() {
      const year = new Date().getFullYear();
      this.ano = year;
    }
  },
  created() {
    this.Year();
  }
};
</script>

<style lang="scss" scoped>
.footer {
  width: 100%;
  padding: 16px 15px;
}
.content {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>