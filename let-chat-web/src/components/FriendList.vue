<template>
  <div>
    <el-header height="56px">Header</el-header>
    <ul>
      <li
        class="bdr-b flow-row"
        v-for="(friend, index) in friendList"
        :key="index"
      >
        <div style="width: 60px; margin-right: 10px;">
          <el-avatar
            shape="square"
            :size="60"
            src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png"
          ></el-avatar>
        </div>
        <div style="flex: 1;" class="flex-column">
          <div style="flex: 1; margin-bottom: 8px;" class="flex-row">
            <span class="name">{{ friend.name }}</span>
            <span class="time">{{ friend.time }}</span>
          </div>
          <span class="message" style="flex: 1;">{{ friend.message }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class FriendList extends Vue {
  friendList = [
    { name: "一直旺火火", time: "00:11", message: "[图片]" },
    { name: "璇狗", time: "00:01", message: "唤起时报:爱上 阿斯顿阿达搜索" },
    { name: "西充有", time: "2020/8/10", message: "你那个: 不好吗" },
    { name: "小仙女们和泰迪", time: "2020/8/10", message: "小憩: [表情]" },
    {
      name: "研发交流群",
      time: "2020/8/10",
      message: "各部门注意,明天上午研讨会在3508,记得参加哦!",
    },
  ];
}
</script>

<style lang="less" scoped>
ul {
  margin: 0 0 0 14px;
  padding: 0;
  li {
    text-align: left;
    list-style: none;
    margin: 10px 0;
    padding-right: 10px;
    span {
      display: inline-block;
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }
    .name {
      width: 70%;
      color: #000;
    }
    .time {
      width: 30%;
      max-width: 100px;
      text-align: right;
      opacity: 0.4;
      font-size: 12px;
    }
    .message {
      max-width: 250px;
      opacity: 0.4;
      font-size: 12px;
    }
  }
}
</style>
