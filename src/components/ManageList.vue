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
        <tr v-if="!lists">
          <td colspan="7">您还没有创建任何类型受众包，请点击左上角创建</td>
        </tr>
        <tr id="{item.id}" v-for="item in lists">
          <td id="{item.id}" class="title">{{item.name}}</td>
          <td class="time">{{item.createdAt}}</td>
          <td>{{item.dataSourceStr}}</td>
          <td node-type="audiencesSize">------</td>
          <td>------</td>
          <td node-type="abnormal" class="abnormal"><i node-type="abnormal-tips"></i><span>异常</span><em class="abnormal-tips-show"><i node-type="abnormal-tips"></i>覆盖人群数大于等于 1000 时才可投放</em></td>
          <td>------</td>
          <td class="operation"  v-if="item.status == 1">
            <div node-type="toolDel" status="1" class="action">移除</div>
          </td>
          <td class="operation" v-else-if="item.status == 2">
            <div node-type="toolDel" status="2" class="action">移除</div>
            <div node-type="toolExtend" class="action">扩展</div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
var url = '/aj/tool_aud/search.json'

/**
var data = {
  'code': 10000,
  'result': {
    'page': '1',
    'pageSize': '10',
    'pageTotal': 5,
    'total': 49,
    'list': [
      {
        'id': 3320,
        'time': '2017-09-05',
        'name': '设备号-20W个-6M',
        'reason': '覆盖人群数大于等于 1000 时才可投放',
        'isUsing': 0,
        'isDeleteEnable': 1,
        'status': 2,
        'statusStr': '异常',
        'dataSourceStr': '上传包',
        'dataFormatsStr': '设备'
      }]
  }
}
var lists = data.result.list
**/
export default {
  name: 'hello',
  data () {
    return {
      message: 'Hello Vue!',
      lists: ''
    }
  },
  mounted () {
    var aq = this
    fetch(url).then(function (response) {
      return response.json()
    }).then(function (data) {
      aq.lists = data.result.list
    }).catch(function (e) {
      console.log('Oops, error')
    })
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
    font-weight: bold;
  }
.message-list table td{
  text-align: center;
  line-height: 30px;
  border-bottom: 1px #f2f2f2 solid;
  padding: 5px 0
}
.message-list table tbody .operation div {
    color: #32cbcc;
    cursor: pointer;
    display: inline-block;
    margin: 0 10px;
}
.abnormal{
  width:50px;
  color: #f28823;
  position: relative;
}
.operation{
  width:150px;
}
.operation .action{
  display:inline-block;
  cursor: pointer;
}
.abnormal i {
    background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA8AAAAQCAYAAADJViUEAAAAGXRFW…QE5wKxLxBvBuJkoKbX6Mqwa4YYwAMk7wGxElDjF2xKAAIMADA8Tl6N9zkgAAAAAElFTkSuQmCC);
    width: 15px;
    height: 15px;
    display: inline-block;
    margin-right: 5px;
    vertical-align: middle;
}
.abnormal em {
    display: none;
    line-height: 30px;
    border: 1px #ddd solid;
    border-radius: 5px;
    padding: 0 7px;
    position: absolute;
    bottom: 44px;
    left: 50%;
    margin-left: -90px;
    background: #fff;
    width: 180px;
}
</style>