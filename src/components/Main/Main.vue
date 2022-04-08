<template>
  <div>
    <JumbotronDiv />
    <GridDiv />
    <FirstSlide />
    <CoursesDiv />
    <SecondSlide />
    <NewsletterDiv />
    <PopularCoursesDiv />
  </div>
</template>

<script>
import JumbotronDiv from "./Jumbotron.vue";
import GridDiv from "./Grid.vue";
import FirstSlide from "./FirstSlide.vue";
import CoursesDiv from "./Courses.vue";
import SecondSlide from "./SecondSlide.vue";
import NewsletterDiv from "./Newsletter.vue";
import PopularCoursesDiv from "./PopularCourses.vue";

export default {
  name: "MainDiv",
  components: {
    JumbotronDiv,
    GridDiv,
    FirstSlide,
    CoursesDiv,
    SecondSlide,
    NewsletterDiv,
    PopularCoursesDiv,
  },
};
</script>

<style lang="scss"></style>
