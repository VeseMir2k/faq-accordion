<template>
  <h1 class="title">
    <img class="title__image" src="../assets/icon-star.svg" alt="" /> FAQs
  </h1>
</template>

<script>
export default {
  name: "FaqsContainerTitle",
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.title {
  display: flex;
  align-items: center;
  text-align: left;
  margin-bottom: 24px;
  &__image {
    margin-right: 24px;
    width: 24px;
    height: 24px;
  }
}
</style>
