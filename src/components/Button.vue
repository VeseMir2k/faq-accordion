<template>
  <div @click="handleToggle" class="button">
    <img src="../assets/icon-plus.svg" alt="" />
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    handleToggle: {
      type: Function,
      require: true,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.button {
  margin-left: 24px;
}
</style>
