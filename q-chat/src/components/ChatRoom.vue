<template>
  <div id="chatRoom">
    <el-container>
      <el-aside width="400px">Southbay</el-aside>
      <el-container>
        <el-main>
          <h1>聊天消息</h1>
          <message-box :messages="messages"></message-box>
        </el-main>
        <el-footer>
          <el-input
            type="textarea"
            :rows="5"
            placeholder="请输入内容"
            v-model="textarea">
          </el-input>
          <el-button type="success" @click="sendMessage">发送消息</el-button>
        </el-footer>
      </el-container>
      <el-aside width="400px">Southbay</el-aside>
    </el-container>
  </div>
</template>

<script>
import MessageBox from './messageBox.vue'

export default {
  components: {
    "message-box": MessageBox,
  },
  data() {
    return {
      textarea: '',
      messages: [
        { text: '学习 JavaScript' },
        { text: '学习 Vue' },
        { text: '整个牛项目' }
      ]
    }
  },
  methods: {
    sendMessage: function () {
      this.messages.push({text: this.textarea})
      this.textarea = ''
    }
  }
}
</script>

<style scoped>

</style>
