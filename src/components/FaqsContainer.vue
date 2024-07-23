<template>
  <div class="faqs-container">
    <FaqsContainerTitle />
    <QuestionAnswer />
  </div>
</template>

<script>
import FaqsContainerTitle from "./FaqsContainerTitle.vue";
import QuestionAnswer from "./QuestionAnswer.vue";

export default {
  name: "FaqsContainer",
  components: { FaqsContainerTitle, QuestionAnswer },
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

@media (min-width: 650px) {
  .faqs-container {
    min-width: auto;
    max-width: 600px;
  }
}
</style>
