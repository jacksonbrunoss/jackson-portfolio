<template>
  <div id="app">
    <Navbar />
    <Header />
    <About />
    <Contact />
  </div>
</template>

<script>
import Navbar from "@/components/Header/Navbar";
import Header from "@/components/Header/Header";
import About from "@/components/About/About";
import Contact from "@/components/Contact/Contact";
export default {
  name: "App",
  components: {
    Navbar,
    Header,
    About,
    Contact
  }
};
</script>

<style lang="scss">
@import url("https://unpkg.com/boxicons@2.0.5/css/boxicons.min.css");
@import url("https://fonts.googleapis.com/css?family=Rubik:300,300i,400,400i,500,500i,700,700i,900,900i&display=swap");
:root {
  /* Fonts */
  --font: "Rubik", sans-serif;
  /* Colors */
  --primary: #54549c;
  --primary-hover: #7474bf;
  --secundary: #348ac7;
  --dark: #19191f;
  --darker: #34343d;
  --light: #f2f2f3;
  --lighter: #dfdfe2;
  --gradient: linear-gradient(116.07deg, #19191f -1.5%, #141419 102.87%);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background: var(--dark);
  font-family: var(--font);
  font-size: 100%;
  color: var(--light);
}
body,
h1,
h2,
h3,
h4,
h5,
h6,
p,
span,
i,
blockquote,
cite,
ul,
li,
a,
img {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  font-size: 1rem;
}
img {
  display: block;
  max-width: 100%;
}
.container {
  max-width: 1144px;
  margin: 0 auto;
}
.btn {
  display: block;
  padding: 14px 40px;
  margin: auto;
  cursor: pointer;
  background: linear-gradient(99.56deg, #7474bf -5.2%, #348ac7 128.15%);
  border: none;
  border-radius: 5px;
  font-weight: 600;
  color: var(--light);
  text-transform: uppercase;
  transition: 0.3s;
  &:hover {
    transform: scale(1.1);
    transition: 0.3s;
  }
}
</style>
