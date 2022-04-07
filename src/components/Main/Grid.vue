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

  div {
    background-color: $lightblue;
    padding: 2rem;
    @include flex(column, flex-start, flex-start);
    gap: 1rem;

    i {
      color: $denim;
      font-size: 3rem;
    }

    p {
      opacity: 0.5;
    }
  }
}
</style>
