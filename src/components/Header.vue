<template>
  <div class="container">
    <!-- Top -->
    <div class="top-header">
      <!-- Left -->
      <div><span>English</span><i class="fa-solid fa-chevron-down"></i></div>
      <!-- Right -->
      <div>
        <!-- Link -->
        <div>
          <ul>
            <li v-for="(link, index) in topHeaderLinks" :key="index">
              <a :href="link.url">{{ link.name }}</a>
            </li>
          </ul>
        </div>
        <!-- Icons -->
        <div>
          <font-awesome-icon
            v-for="(icon, index) in topHeaderIcons"
            :icon="icon"
            :key="index"
          />
        </div>
      </div>
    </div>
    <!-- Bottom -->
  </div>
</template>

<script>
export default {
  name: "HeaderDiv",
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
      topHeaderIcons: ["twitter", "instagram"],
    };
  },
};
</script>

<style scoped lang="scss">
.container {
  width: 1140px;
  margin: 0 auto;
}

.top-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;

  a,
  span {
    opacity: 0.5;
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
}
</style>
