<template>
  <div class="message-box" v-scroll-bottom="messages">
    <li v-for="item in this.messages">
      {{ item.text }}
    </li>
  </div>
</template>

<script>
export default {
  props: {
    messages: Array
  },
  data () {
    return {
      data: 0
    }
  }
}
</script>

<style scoped>
.message-box{
  /* position: absolute;
  height: calc(100% - 6.5rem);
  width: 100%;
  margin-top: 3rem; */
  height: 400px;
  overflow-y: scroll;
  background: #1d1b1b;
  color: aliceblue;
}
</style>
