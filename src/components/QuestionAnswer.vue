<template>
  <div class="question-answer-container">
    <div v-for="(questionAnswer, index) in questionsAnswersData" :key="index">
      <Question :question="questionAnswer.question" :index="index" />
      <Answer :answer="questionAnswer.answer" :index="index" />
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import data from "../data.json";
import Question from "./Question.vue";
import Answer from "./Answer.vue";

export default {
  name: "QuestionAnswer",
  components: { Question, Answer },

  setup() {
    const questionsAnswersData = ref(data);

    return {
      questionsAnswersData,
    };
  },
};
</script>

<style lang="scss" scoped></style>
