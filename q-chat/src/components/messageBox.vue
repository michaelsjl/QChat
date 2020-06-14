<template>
  <div class="message-box" v-scroll-bottom="messages">
    <div v-for="item in this.messages" class="msg">
      <div class="user-head">
        <div class="head"></div>
      </div>
      <div class="user-msg">
        <span :style="right" :class="right">{{ item.text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    messages: Array
  },
  data() {
    return {
      data: 0
    };
  }
};
</script>

<style lang="scss" scoped>
.message-box {
  height: 400px;
  overflow-y: scroll;
  background: #1d1b1b;
  color: aliceblue;
  .msg {
    width: 20%;
    min-height: 2.5rem;
    margin: 1rem 0.5rem;
    position: relative;
    display: flex;
    justify-content: flex-start !important;
    .user-head {
      min-width: 2.5rem;
      width: 20%;
      width: 2.5rem;
      height: 2.5rem;
      border-radius: 50%;
      background: #f1f1f1;
      display: flex;
      justify-content: center;
      align-items: center;
      .head {
        width: 1.2rem;
        height: 1.2rem;
      }
    }
    .user-msg {
      width: 80%;
      word-break: break-all;
      position: relative;
      z-index: 5;
      span {
        display: inline-block;
        padding: 0.5rem 0.7rem;
        border-radius: 0.5rem;
        margin-top: 0.2rem;
        font-size: 0.88rem;
      }
      .left {
        background: white;
        animation: toLeft 0.5s ease both 1;
      }
      .right {
        background: #53a8ff;
        color: white;
        animation: toright 0.5s ease both 1;
      }
    }
  }
}
</style>
