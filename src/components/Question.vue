<template>
  <div class="question-container">
    <h2 class="question-container__question">
      {{ question }}
    </h2>
    <button @click="console.log(index)">+</button>
  </div>
</template>

<script>
export default {
  name: "Question",
  props: {
    index: {
      type: Number,
    },
    question: {
      type: String,
      required: true,
    },
  },
  //   emits: ["isShow"],
  //   setup(props, { emit }) {
  //     const updateIsShowAnswer = () => {
  //       emit("isShow", !props.isShowAnswerIndex);
  //     };
  //     return { updateIsShowAnswer };
  //   },
  // };
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
