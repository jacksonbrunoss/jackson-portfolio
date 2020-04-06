<template>
  <section class="carousel">
    <div class="content-carousel">
      <!-- Using the slider component -->
      <slider ref="slider" :options="options">
        <!-- slideritem wrapped package with the components you need -->
        <slideritem v-for="(item, index) in cases" :key="index" class="corousel-item">
          <div class="img-job">
            <img :src="item.img" :alt="item.name" />
          </div>
          <div class="infos">
            <h3>{{ item.name }}</h3>
            <ul>
              <li v-for="(tech, index) in item.techs" :key="index">{{ tech }}</li>
            </ul>
            <p>{{ item.desc }}</p>
            <a target="blank" :href="item.link">Acesse o projeto</a>
          </div>
        </slideritem>
        <!-- Customizable loading -->
        <div slot="loading">loading...</div>
      </slider>
    </div>
  </section>
</template>

<script>
import { slider, slideritem } from "vue-concise-slider";
import job1 from "../../assets/job-1.png";
export default {
  name: "CarouselPage",
  data() {
    return {
      //data list [array]
      cases: [
        {
          img: job1,
          name: "KryptonDev",
          techs: ["html5", "css3", "js", "Vue"],
          desc: "Front-end desenvolvido por mim, para o cliente KryptonDev.",
          link: "https://warpcgd.github.io/vue-concise-slider/"
        },
        {
          img: job1,
          name: "VitorPica",
          techs: ["html5", "css3", "js", "Vue"],
          desc: "Front-end desenvolvido por mim, para o cliente KryptonDev.",
          link: "https://warpcgd.github.io/vue-concise-slider/"
        }
      ],
      //Slider configuration [obj]
      options: {
        currentPage: 0
      }
    };
  },
  components: {
    slider,
    slideritem
  }
};
</script>

<style lang="scss" scoped>
.content-carousel {
  width: 100%;
  height: auto;
}
.corousel-item {
  padding: 40px 0px;
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
}
.img-job {
  flex: 2;
  margin: 0px 10px;
}
.infos {
  flex: 1;
  text-align: left;
  padding: 0px 0px 0px 40px;
  h3 {
    font-size: 2rem;
    margin-bottom: 40px;
  }
  ul {
    display: flex;
    margin-bottom: 32px;
    li {
      margin: 0px 16px 0px 16px;
      text-transform: uppercase;
      font-weight: 600;
      color: var(--darker);
      transition: 0.2s linear;
      &:hover {
        color: var(--light);
        transition: 0.2s linear;
      }
    }
  }
  p {
    font-size: 1.125rem;
    list-style: 24px;
    color: var(--lighter);
  }
  a {
    background: linear-gradient(99.56deg, #7474bf -5.2%, #348ac7 128.15%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-transform: uppercase;
    font-weight: 600;
    margin: 32px 0px;
    :hover {
      color: var(--light);
    }
  }
}
/* Responsive */
@media (max-width: 963px) {
  .slider-container {
    white-space: normal;
  }
  .corousel-item {
    flex-direction: column;
    align-items: center;
  }
  .img-job {
    flex: 1;
    margin: 0px;
  }
  .infos {
    padding: 32px 0px 0px 0px;
    text-align: center;
    ul {
      justify-content: center;
    }
  }
}
</style>
