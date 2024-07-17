<template>
  <div class="answer-container">
    <p class="answer-container__answer">
      {{ answer }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Answer",
  props: {
    answer: {
      type: String,
      required: true,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.answer-container {
  padding-top: 24px;
}
</style>
