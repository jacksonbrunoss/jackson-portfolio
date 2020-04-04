<template>
  <section class="about">
    <div class="container">
      <div class="content">
        <div class="content-box">
          <Title :title="title" />
          <h5>Jackson Bruno Sousa Silva</h5>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
          <SocialLinks />
        </div>
        <div class="content-box">
          <img src="../../assets/avatar.png" alt="Jackson Bruno" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Title from "@/components/Global/Title";
import SocialLinks from "@/components/Global/SocialLinks";
export default {
  name: "About",
  data() {
    return {
      title: "Quem Sou"
    };
  },
  components: {
    Title,
    SocialLinks
  }
};
</script>

<style scoped lang="scss">
.about {
  width: 100%;
  height: auto;
  background: var(--gradient);
  padding: 96px 15px;
}
.content {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
.content-box {
  flex: 1 2 380px;
  h5 {
    font-size: 1.125rem;
    padding-bottom: 2rem;
  }
  p {
    max-width: 480px;
    line-height: 28px;
    padding-bottom: 2rem;
    color: var(--lighter);
  }
}
</style>