<template>
  <div class="toolbar">
    <div class="logo-menu">
      <div class="menu">
        <ul>
          <li><a href="http://ad.weibo.com">首页</a></li>
          <li><a href="http://ad.weibo.com">推广</a></li>
          <li><a href="http://ad.weibo.com">报表</a></li>
          <li class="active"><a href="http://ad.weibo.com">工具</a></li>
          <li><a href="http://ad.weibo.com">账户</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  margin: 0;
  color: #fff;
}
ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
  line-height: 60px
}

a {
  color: #42b983;
  color: #fff;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}

.toolbar{
  background: #22354a;
  font-size: initial;
  min-width: 1200px;
  margin-bottom: 9px;
}
</style>
