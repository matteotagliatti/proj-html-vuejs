<template>
  <div class="container">
    <!-- First row with 3 elements -->
    <div class="grid-3">
      <div v-for="(element, index) in topElements" :key="index">
        <i class="fa-solid" :class="element.icon"></i>
        <h3>{{ element.title }}</h3>
        <p>{{ element.para }}</p>
      </div>
    </div>
    <!-- Grid courses -->
    <div class="grid-courses">
      <div
        v-for="(course, index) in courseElements"
        :key="index"
        :class="index === 0 ? 'span-2' : ''"
      >
        <img :src="course.img" :alt="course.title" />
        <div class="course-text">
          <h3>{{ course.title }}</h3>
          <p>{{ course.number }} Courses</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GridDiv",
  data() {
    return {
      topElements: [
        {
          icon: "fa-earth-europe",
          title: "Worldwide Recognize",
          para: "Our online course certificates can be used around the world and also in most popular universities and companies.",
        },
        {
          icon: "fa-display",
          title: "Mostly Online Learning (sd)",
          para: "Masterstudy online certificates can be obrained in a range of specialized areas and typically take about a year to complete.",
        },
        {
          icon: "fa-calendar-check",
          title: "Grafuate in as little as 1 Year",
          para: "Online post-graduate certificates are a popular way to develop your professional qualifications of Masterstudy.",
        },
      ],
      courseElements: [
        {
          img: require("../../assets/img/cat_1-770x375.jpg"),
          title: "Software Development",
          number: "5",
        },
        {
          img: require("../../assets/img/cat_2-544x322.jpg"),
          title: "Art",
          number: "8",
        },
        {
          img: require("../../assets/img/cat_3-740x310.jpg"),
          title: "Material Design",
          number: "5",
        },
        {
          img: require("../../assets/img/cat_4-740x310.jpg"),
          title: "Music",
          number: "5",
        },
        {
          img: require("../../assets/img/cat_5-740x310.jpg"),
          title: "Exercise",
          number: "5",
        },
        {
          img: require("../../assets/img/cat_6-740x310.jpg"),
          title: "Photography",
          number: "5",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/style/style.scss";

.grid-3 {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 2rem;
  margin-bottom: 6rem;

  div {
    background-color: $lightblue;
    padding: 2rem;
    @include flex(column, flex-start, flex-start);
    gap: 1rem;
    transition: box-shadow 0.5s;
    &:hover {
      box-shadow: rgba(99, 99, 99, 0.2) 0px 4px 12px 0px;
      cursor: pointer;
    }
    &:hover p {
      opacity: 1;
    }

    i {
      color: $denim;
      font-size: 3rem;
    }

    p {
      opacity: 0.5;
      transition: opacity 0.5s;
    }
  }
}

.grid-courses {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  grid-template-rows: repeat(3, minmax(0, 1fr));
  row-gap: 4rem;
  column-gap: 2rem;
  height: 35rem;
  margin-bottom: 10rem;

  div {
    img {
      width: 100%;
      height: 100%;
      margin-bottom: 0.5rem;
    }

    .course-text {
      @include flex(row, space-between, center);
    }
  }

  .span-2 {
    grid-column: span 2;
    grid-row: span 2;
  }
}
</style>
