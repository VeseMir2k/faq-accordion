<template>
  <div class="question-container">
    <h2 class="question-container__question">
      {{ question }}
    </h2>
    <button @click="updateIsShowIndex">+</button>
  </div>
</template>

<script>
export default {
  name: "Question",
  props: {
    index: {
      type: String,
    },
    isShowIndex: {
      type: String,
    },
    question: {
      type: String,
      required: true,
    },
  },
  emits: ["isShow"],
  setup(props, { emit }) {
    const updateIsShowIndex = () => {
      emit("isShow", props.index);
      console.log(props.index);
    };
    return { updateIsShowIndex };
  },
};
</script>

<style lang="scss" scoped>
.question-container {
  display: flex;
  align-items: center;
}
</style>
