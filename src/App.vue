<template>
  <div id="app"></div>
</template>

<script>
export default {
  name: "App",
  components: {}
};
</script>

<style lang="scss">
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
</style>
