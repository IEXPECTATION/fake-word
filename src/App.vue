<template>
  <tittle-view DocumentName="Document" />
  <tool-view />

</template>

<script>
import TittleView from "./views/TittleView/TittleView.vue";
import ToolView from "./views/ToolView/ToolView.vue";

export default {
  name: "App",
  components: {
    TittleView,
    ToolView,
  },
};
</script>

<style>
#app {
  font-family: "Segoe UI", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
