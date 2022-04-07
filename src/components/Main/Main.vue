<template>
  <div>
    <JumbotronDiv />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
  },
};
</script>

<style lang="scss">
.container {
  max-width: 1100px;
  margin: 0 auto;
}
</style>
