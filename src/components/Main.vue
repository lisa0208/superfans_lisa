<template>
  <div>
    <tool-bar>
    </tool-bar>
    <div class="main">
      <ad-map></ad-map>
      <manage-list></manage-list>
      <page></page>
    </div>
  </div>
</template>

<script>

import ToolBar from './Top.vue'
import AdMap from './AdMap.vue'
import ManageList from './ManageList.vue'
import Page from './Page.vue'

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
    ManageList,
    Page
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
