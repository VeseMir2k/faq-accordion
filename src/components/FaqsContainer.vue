<template>
  <div class="faqs-container">
    <FaqsContainerTitle />
  </div>
</template>

<script>
import FaqsContainerTitle from "./FaqsContainerTitle.vue";

export default {
  name: "FaqsContainer",
  components: { FaqsContainerTitle },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.faqs-container {
  min-width: 100%;
  background-color: var(--white);
  padding: 24px;
  border-radius: 8px;
}
</style>
