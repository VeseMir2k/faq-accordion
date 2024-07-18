<template>
  <div class="question-answer-container">
    <div v-for="(questionAnswer, index) in data" :key="index">
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
      <hr v-if="index < dataLength()" />
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
    const isShow = reactive([]);

    const dataLength = () => Object.keys(data).length;

    const updateIndex = (index) => {
      isShow[index] = !isShow[index];
      console.log(dataLength());
    };

    return {
      dataLength,
      isShow,
      updateIndex,
      data,
    };
  },
};
</script>

<style lang="scss" scoped>
hr {
  border-top: 1px solid var(--light-pink);
  border-bottom: 0px solid transparent;
  margin: 20px 0;
}
</style>
