<template>
  <div class="software-info">
    <div class="software-switch">
      <button @click="SwitchSoftware">ICON</button>
    </div>
    <div class="software-name">Word</div>
    <div class="document-name">{{ DocumentName }}</div>
    <div class="document-search">ICON</div>
    <div class="user-picture">ICON</div>
  </div>
</template>

<script>
export default {
  name: "TittleView",
  props: ["DocumentName"],
  methods: {
    SwitchSoftware() {
      window.alert("Hello!");
    },
  },
};
</script>

<style>
.software-info {
  display: flex;
  height: 48px;
  color: white;
  background-color: #185abd;
}
.software-switch {
  flex: 1;
  padding: 14px 5px;
  background-color: #1651aa;
}
.software-switch button {
  background-color: transparent;
  outline: none;
  border: none;
}
.software-name {
  flex: 1;
  padding: 14px 5px;
  font-size: 16px;
  font-weight: 600;
}
.document-name {
  flex: 5;
  padding: 14px 10px;
  text-align: left;
}
.document-search {
  flex: 1;
  padding: 14px 5px;
}
.user-picture {
  flex: 1;
  padding: 14px 5px;
}
</style>