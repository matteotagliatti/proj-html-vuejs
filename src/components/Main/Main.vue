<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
    <FirstSlide />
    <CoursesDiv />
    <SecondSlide />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";
import FirstSlide from "./FirstSlide.vue";
import CoursesDiv from "./Courses.vue";
import SecondSlide from "./SecondSlide.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
    FirstSlide,
    CoursesDiv,
    SecondSlide,
  },
};
</script>

<style lang="scss"></style>
