<template>
  <div class="plus-minus-icon">
    <img v-if="isShow" src="../assets/icon-minus.svg" alt="" />
    <img v-else src="../assets/icon-plus.svg" alt="" />
  </div>
</template>

<script>
export default {
  name: "PlusMinusIcon",
  props: {
    isShow: {
      type: Boolean,
      required: true,
      default: false,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.plus-minus-icon {
  margin-left: 24px;
}
</style>
