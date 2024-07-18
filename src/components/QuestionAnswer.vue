<template>
  <div class="question-answer-container">
    <div v-for="(questionAnswer, index) in questionsAnswersData" :key="index">
      <Question
        :question="questionAnswer.question"
        :index="index"
        :isShow="isShow[index]"
        @is-show="updateIndex"
      />
      <Answer
        :answer="questionAnswer.answer"
        :index="index"
        v-if="isShow[index]"
      />
    </div>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
import data from "../data.json";
import Question from "./Question.vue";
import Answer from "./Answer.vue";

export default {
  name: "QuestionAnswer",
  components: { Question, Answer },

  setup() {
    const questionsAnswersData = ref(data);
    const isShow = reactive([]);

    const updateIndex = (index) => {
      isShow[index] = !isShow[index];
    };

    return {
      questionsAnswersData,
      isShow,
      updateIndex,
    };
  },
};
</script>

<style lang="scss" scoped></style>
