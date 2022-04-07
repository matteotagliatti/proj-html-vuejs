<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
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
