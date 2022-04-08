<template>
  <div class="popular-courses">
    <div class="large-container">
      <h1>Popular courses</h1>
      <p>Discover our most popular courses for self learning.</p>
      <!-- Courses Grid -->
      <div class="grid">
        <div
          class="grid-element"
          v-for="(course, index) in courses"
          :key="index"
        >
          <!-- Img -->
          <div class="image-container">
            <img :src="course.img" :alt="course.title" />
          </div>
          <div class="course-text-info">
            <!-- Text -->
            <div class="course-text">
              <p class="category">{{ course.category }} ></p>
              <h3>{{ course.title }}</h3>
            </div>
            <!-- Divider -->
            <hr />
            <!-- Info -->
            <div class="course-info">
              <!-- Left -->
              <div>
                <div v-if="course.hours" class="hours">
                  <i class="fa-solid fa-clock"></i> {{ course.hours }} hours
                </div>
                <div v-if="course.stars">
                  <span class="stars">{{ displayStars }}</span>
                  {{ course.stars }}
                </div>
              </div>
              <!-- Right -->
              <div>
                <div v-if="course.free" class="free">Free</div>
                <div v-if="course.price_final" class="price">
                  <span v-if="course.price_discount" class="discount"
                    >${{ course.price_discount }}</span
                  >
                  <span class="final">${{ course.price_final }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="slider">
        <div>
          <i class="fa-solid fa-chevron-left"></i>
        </div>
        <div>
          <i class="fa-solid fa-chevron-right"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoursesDiv",
  data() {
    return {
      courses: [
        {
          img: require("../../assets/img/photo-1461749280684-dccba630e2f6-544x322.jpeg"),
          category: "Apache",
          title: "Web Coding and Apache Basics",
          hours: "6",
          free: true,
        },
        {
          img: require("../../assets/img/cat_2-740x310.jpg"),
          category: "Art",
          title: "Real Things Art Painting by Jason Ni",
          hours: "6",
          price_discount: "60",
          price_final: "45",
        },
        {
          img: require("../../assets/img/course-preview-544x322.jpg"),
          category: "Software Development",
          title: "Basics of Masterstudy",
          stars: 5,
          free: true,
        },
        {
          img: require("../../assets/img/photo-1496307042754-b4aa456c4a2d-544x322.jpeg"),
          category: "Electronic",
          title: "How to be a DJ? Make Electronic Music",
          stars: 5,
          price_discount: "59",
          price_final: "49",
        },
        {
          img: require("../../assets/img/photo-1416339134316-0e91dc9ded92-scaled-544x322.jpeg"),
          category: "Communication",
          title: "Design Intrumnets for Communication",
          hours: "6",
        },
        {
          img: require("../../assets/img/cathryn-lavery-67852-unsplash-544x322.jpg"),
          category: "Art",
          title: "Make your Concept Right and Beautiful",
          hours: "6",
          price_final: "70",
        },
      ],
    };
  },
  computed: {
    displayStars() {
      return "★★★★★";
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/style/style.scss";

.popular-courses {
  background-color: $backgroundlightblue;
}

.large-container {
  padding: 6rem 0;
  text-align: center;
}

h1 {
  margin-bottom: 2rem;
}

p {
  margin-bottom: 4rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(6, minmax(0, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;

  .grid-element {
    border: 1px solid $anthensgray;
    text-align: left;
    background-color: white;

    .image-container {
      height: 10rem;
      position: relative;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }

    .course-text-info {
      padding: 1.2rem;
      @include flex(column, space-between, flex-start);
      gap: 1rem;
      height: 10.5rem;

      .course-text {
        .category {
          font-size: 0.8rem;
          opacity: 0.4;
          margin-bottom: 0.6rem;
        }

        h3 {
          font-size: 1rem;
        }
      }

      hr {
        width: 100%;
        color: $anthensgray;
      }

      .course-info {
        width: 100%;
        @include flex(row, space-between, center);

        .hours {
          opacity: 0.5;
        }

        .stars {
          font-size: 1.3rem;
          color: goldenrod;
        }

        .free,
        .final {
          font-weight: bold;
        }

        .price {
          position: relative;

          .discount {
            position: absolute;
            top: -0.8rem;
            right: 0;
            font-size: 0.9rem;
            color: grey;
          }
        }
      }
    }
  }
}

.slider {
  text-align: center;
  @include flex(row, center, center);

  div {
    @include flex(row, center, center);
    padding: 1rem 1.2rem;
    background-color: white;
    border: 1px solid $anthensgray;

    i {
      opacity: 0.5;
    }
  }
}
</style>
