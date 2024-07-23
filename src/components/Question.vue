<template>
  <div class="question-container" @click="toggleAnswer">
    <h2 class="question-container__question">
      {{ question }}
    </h2>
    <button class="question-container__button">
      <img v-if="isShow" src="../assets/icon-minus.svg" alt="" />
      <img v-else src="../assets/icon-plus.svg" alt="" />
    </button>
  </div>
</template>

<script>
import minusIcon from "../assets/icon-minus.svg";
import plusIcon from "../assets/icon-plus.svg";

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
  &__button {
    cursor: pointer;
  }
}
</style>
