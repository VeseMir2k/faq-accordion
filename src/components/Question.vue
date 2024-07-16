<template>
  <div class="question-container">
    <h2 class="question-container__question">
      What is Frontend Mentor, and how will it help me?
    </h2>
    <Button />
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Question",
  components: { Button },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.question-container {
  display: flex;
  align-items: center;
}
</style>
