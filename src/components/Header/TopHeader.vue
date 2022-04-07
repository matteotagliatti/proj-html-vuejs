<template>
  <div class="mb">
    <div class="header-container">
      <div class="top-header">
        <!-- Left -->
        <div>
          <span class="lang">English</span
          ><i class="fa-solid fa-chevron-down"></i>
        </div>
        <!-- Right -->
        <div class="right">
          <!-- Link -->
          <div>
            <ul>
              <li v-for="(link, index) in topHeaderLinks" :key="index">
                <a :href="link.url">{{ link.name }}</a>
              </li>
            </ul>
          </div>
          <!-- Icons -->
          <div class="icons">
            <i
              v-for="(icon, index) in topHeaderIcons"
              class="fa-brands"
              :class="icon"
              :key="index"
            ></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopHeader",
  data() {
    return {
      topHeaderLinks: [
        {
          name: "Courses",
          url: "#",
        },
        {
          name: "Zoom",
          url: "#",
        },
        {
          name: "Pages",
          url: "#",
        },
        {
          name: "Bundles",
          url: "#",
        },
        {
          name: "Course Formats",
          url: "#",
        },
        {
          name: "Add Course",
          url: "#",
        },
        {
          name: "Demos",
          url: "#",
        },
      ],
      topHeaderIcons: [
        "fa-twitter",
        "fa-instagram",
        "fa-behance",
        "fa-dribbble",
        "fa-git",
        "fa-linkedin",
        "fa-pinterest",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/style/style.scss";

.mb {
  border-bottom: 1px solid $anthensgray;
}

.top-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;

  a,
  span,
  i {
    opacity: 0.6;
    font-size: 0.9rem;
  }

  ul {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    gap: 2rem;
  }

  li {
    list-style: none;

    a {
      color: black;
    }
  }

  .lang {
    margin-right: 0.7rem;
  }

  .right {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    gap: 3rem;

    .icons {
      display: flex;
      gap: 1rem;
    }
  }
}
</style>
