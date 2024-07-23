<template>
  <div class="question-container" @click="toggleAnswer">
    <h2 class="question-container__question">
      {{ question }}
    </h2>
    <PlusMinusIcon :isShow="isShow" />
  </div>
</template>

<script>
import PlusMinusIcon from "./PlusMinusIcon.vue";

export default {
  name: "Question",
  components: { PlusMinusIcon },
  props: {
    index: {
      type: String,
      required: true,
    },
    isShow: {
      type: Boolean,
      required: true,
      default: false,
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
  justify-content: space-between;
  gap: 24px;
  cursor: pointer;
  &:hover {
    color: var(--pink);
  }
}
</style>
