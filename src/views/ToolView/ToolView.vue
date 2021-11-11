<template>
  <div class="tool-box">
    <div class="tool-option">
      <div class="tag-option">
        <div class="fixed-option">
          <div class="option-item">
            <!-- <button @click="sayHi"></button> -->
            <button @mouseenter="bold" @mouseleave="normal" ><span>文件</span></button>
          </div>
        </div>
        <div class="variable-option">
          <div class="option-item option-item-active">
            <router-link to="/file"><span>开始</span></router-link>
          </div>
          <div class="option-item">
            <router-link to="/file"><span>插入</span></router-link>
          </div>
          <div class="option-item" v-if="false">
            <router-link to="/file"><span>布局</span></router-link>
          </div>
          <div class="option-item" v-if="false">
            <router-link to="/file"><span>引用</span></router-link>
          </div>
          <div class="option-item" v-if="false">
            <router-link to="/file"><span>审阅</span></router-link>
          </div>
          <div class="option-item" v-if="false">
            <router-link to="/file"><span>视图</span></router-link>
          </div>
          <div class="option-item" v-if="false">
            <router-link to="/file"><span>帮助</span></router-link>
          </div>
          <div class="option-item">
            <span>⋁</span>
          </div>
        </div>
      </div>
      <div class="extra-option">
        <div class="pen-option">ICON</div>
        <div class="share-option">ICON</div>
        <div class="comment-option">ICON</div>
      </div>
    </div>
    <div class="tool-handler">
      <router-view></router-view>
      <!-- <div class="text">
        <div class="undo">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
        <div class="paste">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
      </div>
      <div class="font">
        <div class="bolder">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
        <div class="italic">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
        <div class="underline">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
      </div>
      <div class="paragraph">
        <div class="align">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
      </div>
      <div class="more">
        <div class="dot">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
      </div>
      <div class="style">
        <div class="selection">
          <div class="items">🟥</div>
          <div class="drop-down">⋁</div>
        </div>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "ToolView",
  methods: {
    bold() {
      console.log("bold");
      console.log(this.$refs);
    },
    normal() {
      console.log("normal");
    }
  },
};
</script>

<style scoped>
.tool-box {
  background-color: #f3f2f1;
  height: 76px;
  display: flex;
  flex-direction: column;
}
.tool-option {
  height: 40px;
  font-size: 14px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.tag-option {
  display: flex;
  flex-direction: row;
  height: 34px;
}
.fixed-option {
  display: flex;
  padding-left: 19px;
  padding-right: 19px;
  height: 100%;
  align-items: center;
}
.fixed-option .option-item {
  display: flex;
  align-items: center;
  height: 100%;
}
.fixed-option button {
  outline: none;
  border: none;
  height: 100%;
  width: 100%;
}
.fixed-option span {
  font-size: 14px;
  margin: 0 4px;
}
.variable-option {
  display: flex;
  flex-direction: row;
  height: 100%;
}
.variable-option .option-item {
  display: flex;
  align-items: center;
  height: 100%;
  padding: 0 11px;
}
.variable-option .option-item span {
  font-size: 14px;
  margin: 0 4px;
}
.variable-option .option-item:last-child {
  padding: 0;
  width: 30px;
}
.option-item-active {
  font-weight: 600;
}
.extra-option {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.tool-handler {
  height: 40px;
  box-shadow: 0px 1px 2px rgba(100, 100, 100, 0.2);
  display: flex;
  flex-direction: row;
}

.text {
  display: flex;
  flex-direction: row;
  padding: 0 3px;
}
.undo {
  display: flex;
  flex-direction: row;
}
.paste {
  display: flex;
  flex-direction: row;
}

.font {
  display: flex;
  flex-direction: row;
}

.paragraph {
  display: flex;
  flex-direction: row;
}
.more {
  display: flex;
  flex-direction: row;
}
.style {
  display: flex;
  flex-direction: row;
}
.bolder {
  display: flex;
  flex-direction: row;
}

.italic {
  display: flex;
  flex-direction: row;
}
.underline {
  display: flex;
  flex-direction: row;
}
.paragraph {
  display: flex;
  flex-direction: row;
}
/* style of mouse hovers */
/* background-color: #edebe9; */
/* font-weight: 600; */

/* .tool-option-active::after {
  content: "";
  display: block;
  position: absolute;
  height: 10px;
  width: 30px;
  margin-left: 34px;
  border-top: 3px solid #185abd;
} */
</style>