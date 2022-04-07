<template>
  <div id="app">
    <HeaderDiv />
    <MainDiv />
    <FooterDiv />
  </div>
</template>

<script>
import HeaderDiv from "./components/Header.vue";
import MainDiv from "./components/Main.vue";
import FooterDiv from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    HeaderDiv,
    MainDiv,
    FooterDiv,
  },
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  font-family: Arial, sans-serif;
  color: black;
  background-color: white;
}

a {
  text-decoration: none;
}
</style>
