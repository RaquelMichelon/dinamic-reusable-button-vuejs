<template>
  <div id="app">
    <app-button @click="handleClickShowAlert" buttonText="Click Me" />
    <app-button
      @click="handleClickPrintConsole"
      :dark="true"
      buttonText="Click Me"
    />
  </div>
</template>

<script>
import AppButton from "./components/Button";
export default {
  name: "App",
  components: {
    AppButton,
  },
  methods: {
    handleClickShowAlert() {
      alert("Hi from button clicked!");
    },
    handleClickPrintConsole() {
      console.log("Hi from button clicked!");
    },
  },
};
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
}
</style>
