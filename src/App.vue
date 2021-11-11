<template>
  <tittle-view />
  <tool-view />
  <writing-view />
</template>

<script>
import TittleView from "./views/TittleView/TittleView.vue";
import ToolView from "./views/ToolView/ToolView.vue";
import WritingView from "./views/WritingView/WritingView.vue";
export default {
  name: "App",
  components: {
    TittleView,
    ToolView,
    WritingView,
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
