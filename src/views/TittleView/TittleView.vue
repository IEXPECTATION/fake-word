<template>
  <div class="software-info">
    <div class="software-switch">
      <button @click="SwitchSoftware">ICON</button>
    </div>
    <div class="software-name">Word</div>
    <div class="document-name" @click="changeDocumentname">
      {{ DocumentName }}
    </div>
    <div class="document-search">Search Bar</div>
    <div class="user-picture">ICON</div>
  </div>
</template>

<script>
export default {
  name: "TittleView",
  data() {
    return {
      DocumentName: "Document",
    };
  },
  methods: {
    SwitchSoftware() {
      console.log("SwitchSoftware");
    },
    changeDocumentname() {
      console.log("changeDocumentname");
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
  width: 48px;
  padding-top: 12px;
}
.software-switch:hover {
  background-color: #1651aa;
}
.software-switch button {
  background-color: transparent;
  outline: none;
  border: none;
}

.software-name {
  padding-top: 13px;
  padding-left: 8px;
  padding-right: 12px;
  font-weight: 600;
  font-size: 16px;
}

.document-name {
  width: 400px;
  padding-top: 14px;
  padding-left: 11px;
  font-size: 14px;
  text-align: left;
}
.document-name:hover {
  background-color: #1651aa;
  cursor: pointer;
}
.document-search {
  width: 800px;
  padding-left: 10px;
}
.user-picture {
  width: 48px;
  padding-left: 152px;
}
</style>
