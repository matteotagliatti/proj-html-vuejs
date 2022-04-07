<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
    <FirstSlide />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";
import FirstSlide from "./FirstSlide.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
    FirstSlide,
  },
};
</script>

<style lang="scss">
.container {
  max-width: 1100px;
  min-width: 900px;
  margin: 0 auto;
}
</style>
