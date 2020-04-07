<template>
  <section class="contact" id="contact">
    <div class="container">
      <div class="content">
        <Title :title="title" />
        <div class="content-box">
          <h3>Pronto para começarmos um projeto juntos?</h3>
          <p>Estou pronto para começar. A entrega da programação será fiel ao layout proposto pelo designer, com respeito aos prazos e às suas necessidades.</p>
          <a href="#" class="mail">oi.jbss@gmail.com</a>
          <button class="btn btn-contact">
            mande um zap
            <i class="bx bxl-whatsapp"></i>
          </button>
          <SocialLinks />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Title from "@/components/Global/Title";
import SocialLinks from "@/components/Global/SocialLinks";
export default {
  name: "Contact",
  data() {
    return {
      title: "Contato"
    };
  },
  components: {
    Title,
    SocialLinks
  }
};
</script>

<style lang="scss" scoped>
.contact {
  width: 100%;
  background: var(--gradient);
  padding: 96px 15px;
}
.content-box {
  max-width: 800px;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  h3 {
    font-size: 2.5rem;
    background: linear-gradient(99.56deg, #7474bf -5.2%, #348ac7 128.15%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    padding: 32px 0px;
    text-align: center;
  }
  p {
    text-align: center;
    color: var(--lighter);
    line-height: 28px;
    max-width: 700px;
    font-weight: 500;
    padding-bottom: 32px;
  }
  a {
    color: var(--light);
    text-decoration: underline;
    transition: 0.2s linear;
    &:hover {
      color: var(--primary);
      transition: 0.2s linear;
    }
  }
  .btn-contact {
    margin: 32px 0px;
    display: flex;
    align-items: center;
    i {
      margin-left: 8px;
      font-size: 1.125rem;
    }
  }
}
</style>