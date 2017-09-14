<template>
  <div>
    <tool-bar>
    </tool-bar>
    <div class="main">
      <ad-map></ad-map>
      <manage-list></manage-list>
    </div>
    <h1 v-bind:title="msg">{{msg}}</h1>
    <h2>{{message}}</h2>
    <input v-model="message">
    <h2>Essential Links</h2>
    <p v-if="seen">现在你看到我了1</p>
    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ol>
    <button v-on:click="reverseMessage">逆转消息</button>
  </div>
</template>

<script>

import ToolBar from './Top.vue'
import AdMap from './AdMap.vue'
import ManageList from './ManageList.vue'
export default {
  name: 'hello',
  data () {
    return {
      message: 'Hello Vue!',
      msg: '页面加载于 ' + new Date().toLocaleString(),
      seen: true,
      todos: [
        { text: '学习 JavaScript' },
        { text: '学习 Vue' },
        { text: '整个牛项目' }
      ]
    }
  },
  components: {
    ToolBar,
    AdMap,
    ManageList
  },
  methods: {
    reverseMessage: function () {
      this.msg = this.msg.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  padding:0;
  margin:0
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.main{
  text-align:left;
  padding: 0 10px 10px;
}
</style>
