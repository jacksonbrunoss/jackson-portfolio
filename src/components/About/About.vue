<template>
  <section class="about">
    <div class="container">
      <div class="content">
        <div class="content-box">
          <Title :title="title" />
          <h5>Jackson Bruno Sousa Silva</h5>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
          <SocialLinks class="links" />
        </div>
        <div class="content-box">
          <img src="../../assets/avatar.png" alt="Jackson Bruno" />
          <img src="../../assets/avatar-2.png" alt="Jackson Bruno" class="img-mobile" />
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
.img-mobile {
  display: none;
}
/* Responsive */
@media (max-width: 963px) {
  .content {
    flex-direction: column;
  }
  .content-box {
    flex: 100%;
    h5 {
      text-align: center;
    }
    p {
      text-align: center;
      font-size: 1.125rem;
      max-width: 100%;
    }
    .img-mobile {
      display: block;
      padding: 32px 0px 0px 0px;
      margin: auto;
    }
    img {
      display: none;
    }
    .links {
      display: none;
    }
  }
}
</style>