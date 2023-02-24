<template>
  <button v-bind="$attrs" :class="[dark ? 'dark' : 'light', 'baseButton']">
    {{ buttonText }}
  </button>
</template>

<script>
export default {
  props: {
    buttonText: {
      type: String,
      default: () => "Button Text",
    },
    dark: {
      type: Boolean,
      default: () => false,
    },
  },
};
</script>

<style scoped>
.baseButton {
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  margin-top: 10px;
}
.light {
  background: white;
  color: black;
  border: 1px solid gray;
}
.dark {
  background: black;
  color: white;
}
</style>