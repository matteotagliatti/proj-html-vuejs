<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
    <FirstSlide />
    <CoursesDiv />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";
import FirstSlide from "./FirstSlide.vue";
import CoursesDiv from "./Courses.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
    FirstSlide,
    CoursesDiv,
  },
};
</script>

<style lang="scss"></style>
