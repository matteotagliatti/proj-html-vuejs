<template>
  <div>
    <TopHeader />
    <BottomHeader />
  </div>
</template>

<script>
import TopHeader from "./TopHeader.vue";
import BottomHeader from "./BottomHeader.vue";

export default {
  name: "HeaderDiv",
  components: {
    TopHeader,
    BottomHeader,
  },
};
</script>

<style lang="scss">
@import "../../assets/style/style.scss";

.header-container {
  max-width: 1600px;
  min-width: 1000px;
  margin: 0 auto;
  padding: 0 2rem;
}
</style>
