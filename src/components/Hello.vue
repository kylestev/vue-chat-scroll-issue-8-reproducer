<template>
  <div class="hello">
    <div class="message_list" v-chat-scoll>
      <div
        v-for="message in messages"
        v-text="message.body"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      messages: [
        { body: 'message #1' },
        { body: 'message #2' },
        { body: 'message #3' },
        { body: 'message #4' },
        { body: 'message #5' },
        { body: 'message #6' },
        { body: 'message #7' },
        { body: 'message #8' },
        { body: 'message #9' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.message_list {
  display: flex;
  flex-direction: column;
  max-height: 300px;
  max-width: 300px;
  overflow-y: scroll;
}

.message_list .message_list_item {
  flex: 1;
  padding: 5px;
}
</style>
