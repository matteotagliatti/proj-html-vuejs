<template>
  <div class="second-slide">
    <div class="container">
      <h1 class="title">We Are Proud</h1>
      <p class="para">
        Certificate courses are instructed by highly educated and qualified
        intructions who hold doctoral and master's level degrees.
      </p>
      <div class="numbers">
        <div v-for="(element, index) in elements" :key="index">
          <h2>{{ element.number }}</h2>
          <p>{{ element.text }}</p>
        </div>
      </div>
    </div>
    <img src="../../assets/img/we_proud.png" alt="background" />
  </div>
</template>

<script>
export default {
  name: "SecondSlide",
  data() {
    return {
      elements: [
        {
          number: "2000",
          text: "Students",
        },
        {
          number: "950",
          text: "Courses",
        },
        {
          number: "1600",
          text: "Hours Video",
        },
        {
          number: "150",
          text: "Countries Reached",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/style/style.scss";

.second-slide {
  padding-top: 6rem;
  text-align: center;
  background: $backgroundlightblue;

  p {
    opacity: 0.6;
  }

  img {
    margin-top: -4rem;
    width: 100%;
  }

  .title {
    margin-bottom: 2rem;
  }

  .para {
    padding: 0 14rem;
    margin-bottom: 2rem;
  }

  .numbers {
    @include flex(row, center, center);

    div {
      padding: 2rem 4rem;
      border-right: 1px solid $anthensgray;

      h2 {
        font-size: 3rem;
      }

      p {
        text-transform: uppercase;
      }
    }
  }
}
</style>
