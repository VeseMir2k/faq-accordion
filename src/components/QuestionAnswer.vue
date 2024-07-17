<template>
  <div class="question-answer-container">
    <div v-for="(questionAnswer, index) in questionsAnswersData" :key="index">
      <Question
        :question="questionAnswer.question"
        :index="index"
        :isShowIndex="isShowIndex"
        @is-show="updateIndex"
      />
      <Answer
        :answer="questionAnswer.answer"
        :index="index"
        v-if="isShowIndex === index"
      />
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
    const isShowIndex = ref("-1");

    const updateIndex = (value) => {
      isShowIndex.value = value;
      console.log(value);
    };

    return {
      questionsAnswersData,
      isShowIndex,
      updateIndex,
    };
  },
};
</script>

<style lang="scss" scoped></style>
