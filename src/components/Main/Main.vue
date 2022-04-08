<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
    <FirstSlide />
    <CoursesDiv />
    <SecondSlide />
    <NewsletterDiv />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";
import FirstSlide from "./FirstSlide.vue";
import CoursesDiv from "./Courses.vue";
import SecondSlide from "./SecondSlide.vue";
import NewsletterDiv from "./NewsletterDiv.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
    FirstSlide,
    CoursesDiv,
    SecondSlide,
    NewsletterDiv,
  },
};
</script>

<style lang="scss"></style>
