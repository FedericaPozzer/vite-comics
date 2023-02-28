<script>
import AppHeader from "./components/AppHeader.vue";
import SectionMain from "./components/SectionMain.vue";
import AppFooter from "./components/AppFooter.vue";

// import style from "./assets/css/style.css"

export default {
  components: {
    AppHeader, SectionMain, AppFooter,
  }
}
</script>

<template>
  <AppHeader />

  <SectionMain />

  <AppFooter />
</template>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

.container {
  max-width: 80rem;
  margin: 0 auto;

  /* debug */
  /* border: 1px solid black; */
}

img {
  max-height: 100%;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
