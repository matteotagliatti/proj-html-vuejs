<template>
  <div class="large-container">
    <h1>Recent courses</h1>
    <!-- Categories -->
    <div class="categories">
      <span
        v-for="(category, index) in categories"
        :key="index"
        :class="index === 0 ? 'active' : ''"
        >{{ category }}</span
      >
    </div>
    <!-- Courses Grid -->
    <div class="grid">
      <div class="grid-element" v-for="(course, index) in courses" :key="index">
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
                <span class="stars">{{ displayStars }}</span> {{ course.stars }}
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
    <div>
      <a class="btn">Show All</a>
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
        {
          img: require("../../assets/img/photo-1475452779376-caebfb988090-544x322.jpeg"),
          category: "Bicycling",
          title: "Road Bike Manual or How to Be a Champion",
          hours: "6",
          price_final: "20",
        },
        {
          img: require("../../assets/img/cristian-grecu-762012-unsplash-min-scaled-544x322.jpg"),
          category: "Documentary",
          title: "How to Make Beautiful Landscape photos?",
          hours: "6",
          price_final: "60",
        },
        {
          img: require("../../assets/img/landscape-544x322.jpg"),
          category: "Art",
          title: "Let's paint Van Gogh's Starry Night",
          hours: "6",
          price_final: "79",
        },
        {
          img: require("../../assets/img/12345-1-544x322.png"),
          category: "Nvidia",
          title: "Nvidia and UE4 Technologies Practice",
          stars: 5,
          free: true,
        },
        {
          img: require("../../assets/img/jakob-owens-198234-unsplash-min-1-544x322.png"),
          category: "Art",
          title: "How to Work with LEgendary RED Camera",
          hours: 6,
          free: true,
        },
        {
          img: require("../../assets/img/promo_tf-544x322.jpg"),
          category: "Software Development",
          title: "MasterStudy Mobile LMS App",
          hours: 2,
          free: true,
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

.large-container {
  padding: 6rem 0;
  text-align: center;
}

h1 {
  margin-bottom: 3rem;
}

.btn {
  margin: 0 auto;
  width: 8rem;
}

.categories {
  @include flex(row, center, center);
  gap: 3rem;
  padding: 0 10rem;
  color: $denim;
  margin: 3rem;

  .active {
    padding: 0.7rem 1rem;
    border-radius: 3rem;
    color: $william;
    background-color: $lightblue;
  }
}

.grid {
  display: grid;
  grid-template-columns: repeat(6, minmax(0, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;

  .grid-element {
    border: 1px solid $anthensgray;
    text-align: left;

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
            font-size: 0.8rem;
            color: grey;
          }
        }
      }
    }
  }
}
</style>
