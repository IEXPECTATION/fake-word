<template>
  <div ref="board" class="writing-board" contenteditable="true">
    <span>Writing View</span>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$refs.board.focus();
  },
  methods: {},
};
</script>

<style>
.writing-board {
  margin: 20px auto;
  padding: 3px;
  width: 52%;
  outline: none;
  height: 100vh;
  background-color: white;
  border: 1px solid rgba(0, 0, 0, .3);
  padding-top: 120px;
}

.writing-board *{
  margin-left: 80px;
}
</style>
