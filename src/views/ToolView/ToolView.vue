<template>
  <div class="tool-box">
    <div class="tool-option">
      <div class="tag-option">
        <div class="fixed-option">
          <div class="option-item">
            <button><span>文件</span></button>
          </div>
        </div>
        <div class="variable-option">
          <div
            ref="tool"
            class="option-item"
            v-for="(item, index) in options"
            :key="index"
            @click="
              currIndex = index;
              currentComp = item.name;
            "
            :class="currIndex === item.index ? 'tool-bar-active' : ''"
          >
            <div>
              <span>{{ item.title }} </span>
            </div>
          </div>

          <div class="option-item">
            <div>
              <span>编辑</span>
            </div>
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
      <keep-alive>
        <component :is="currentComp" />
      </keep-alive>
    </div>
  </div>
</template>

<script>
import HelpBar from "@/components/ToolBar/HelpBar.vue";
import InsertionBar from "@/components/ToolBar/InsertionBar.vue";
import LayoutBar from "@/components/ToolBar/LayoutBar.vue";
import ReferenceBar from "@/components/ToolBar/ReferenceBar.vue";
import ReviewBar from "@/components/ToolBar/ReviewBar.vue";
import StartBar from "@/components/ToolBar/StartBar.vue";
import ViewBar from "@/components/ToolBar/ViewBar.vue";

export default {
  name: "ToolView",
  components: {
    HelpBar,
    InsertionBar,
    LayoutBar,
    ReferenceBar,
    ReviewBar,
    StartBar,
    ViewBar,
  },
  data() {
    return {
      currentComp: "start-bar",
      currIndex: 0,
      // maxIndex: 2, // 2 for phone, 6 for pc
      options: [
        {
          index: 0,
          name: "start-bar",
          title: "开始",
        },
        {
          index: 1,
          name: "insertion-bar",
          title: "插入",
        },
        {
          index: 2,
          name: "layout-bar",
          title: "布局",
        },
        {
          index: 3,
          name: "reference-bar",
          title: "引用",
        },
        {
          index: 4,
          name: "review-bar",
          title: "审阅",
        },
        {
          index: 5,
          name: "view-bar",
          title: "视图",
        },
        {
          index: 6,
          name: "help-bar",
          title: "帮助",
        },
      ],
    };
  },
};
</script>

<style scoped>
.tool-box {
  color: #252423;
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
.tag-option a {
  color: #252423;
  outline: none;
  border: none;
  text-decoration: none;
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
  height: 100%;
  padding: 0 11px;
}
.variable-option .option-item div {
  display: flex;
  align-items: center;
  position: relative;
  width: 100%;
  height: 100%;
}
.tool-bar-active div::before {
  content: "";
  display: block;
  position: absolute;
  width: 14px;
  height: 3px;
  bottom: 0;
  left: 4px;
  background-color: #185abd;
  transition: all 0.4s;
}
.tool-bar-active div::after {
  content: "";
  display: block;
  position: absolute;
  width: 14px;
  height: 3px;
  bottom: 0;
  left: 18px;
  background-color: #185abd;
  transition: width 0.4s;
}
.variable-option .option-item span {
  font-size: 14px;
  margin: 0 4px;
}
.variable-option .option-item:last-child {
  padding: 0;
  margin-left: 20px;
  width: 80px;
}
.tool-bar-active {
  font-weight: 600;
}
.option-item:hover {
  background-color: #edebe9;
  font-weight: 600;
}
.tool-bar-active:hover div::before {
  left: -11px;
  width: 29px;
}
.tool-bar-active:hover div::after {
  width: 29px;
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
