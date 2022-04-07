<template>
  <div class="large-container">
    <h1>Recent courses</h1>
    <div class="categories">
      <span
        v-for="(category, index) in categories"
        :key="index"
        :class="index === 0 ? 'active' : ''"
        >{{ category }}</span
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesDiv",
  data() {
    return {
      categories: [
        "All Categories",
        "Art",
        "Exercise",
        "Material Design",
        "Music",
        "Photography",
        "Software Development",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/style/style.scss";

.large-container {
  padding: 6rem 0;
  text-align: center;
}

h1 {
  margin-bottom: 3rem;
}

.categories {
  @include flex(row, center, center);
  gap: 3rem;
  padding: 0 10rem;
  color: $denim;

  .active {
    padding: 0.7rem 1rem;
    border-radius: 3rem;
    color: $william;
    background-color: $lightblue;
  }
}
</style>
