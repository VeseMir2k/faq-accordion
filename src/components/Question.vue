<template>
  <div class="question-container">
    <h2 class="question-container__question">
      {{ question }}
    </h2>
    <button @click="toggleAnswer">{{ isShow ? "-" : "+" }}</button>
  </div>
</template>

<script>
export default {
  name: "Question",
  props: {
    index: {
      type: String,
      required: true,
    },
    isShow: {
      type: Boolean,
      required: true,
    },
    question: {
      type: String,
      required: true,
    },
  },
  emits: ["isShow"],
  setup(props, { emit }) {
    const toggleAnswer = () => {
      emit("isShow", props.index);
    };
    return { toggleAnswer };
  },
};
</script>

<style lang="scss" scoped>
.question-container {
  display: flex;
  align-items: center;
}
</style>
