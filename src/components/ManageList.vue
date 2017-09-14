<template>
  <div node-type="message-list" class="message-list clearfix">
    <table class="crowd-table">
      <thead>
        <tr>
          <th class="title">人群包名称</th>
          <th class="time">创建时间</th>
          <th class="select-type">
            <select node-type="select-type">
              <option value="0">类型</option>
              <option value="1">上传包</option>
              <option value="2">已有包扩展</option>
              <option value="3">博文互动用户扩展</option>
            </select>
          </th>
          <th>覆盖人群数</th>
          <th>上传数量</th>
          <th class="select-actionStatu">
            <select node-type="select-actionStatu">
              <option value="0">全部状态</option>
              <option value="1">解析中</option>
              <option value="2">解析完成</option>
              <option value="3">异常</option>
              <option value="4">扩展中</option>
              <option value="5">扩展完成</option>
            </select>
          </th>
          <th>使用此人群包的计划</th>
          <th>操作</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td colspan="7">您还没有创建任何类型受众包，请点击左上角创建</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>

export default {
  name: 'hello',
  data () {
    return {
      message: 'Hello Vue!'
    }
  }
}
</script>
<style>
.message-list{
  border: 1px #e7e7e8 solid;
  border-radius: 3px;
  background: #fff;
  padding: 10px;
  position: relative;
}
.message-list table{
  width: 100%;
  border-spacing: 0;
  border-collapse: collapse;
  
}
.message-list table th {
    background: #f5f5f5;
    line-height: 36px;
    border-bottom: 0;
    text-align: center;
    font-weight: bold;}
</style>