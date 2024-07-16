<template>
  <div class="question-answer-container">
    <Question />
    <Answer />
  </div>
</template>

<script>
import { ref } from "vue";
import Question from "./Question.vue";
import Answer from "./Answer.vue";

export default {
  name: "QuestionAnswer",
  components: { Question, Answer },
  setup() {
    const isShowAnswer = ref(false);

    return { isShowAnswer };
  },
};
</script>

<style lang="scss" scoped></style>
