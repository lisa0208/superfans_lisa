<template>
    <div node-type="stop-popup" class="stop-popup">
        <div style="position: fixed; height: 100%; background-color: rgba(0, 0, 0, 0.2); display: block;" class="comp-general-popover-bg">
        <div style="width: 448px; height: 245px;" class="r-container-fluid comp-general-popover-body">
            <div style="display:block" class="r-row comp-general-popover-head">提示
            <div class="comp-general-popover-close">X</div>
            </div>
            <div class="r-row comp-general-popover-loading"></div>
            <div class="r-row comp-general-popover-content">
        <!--Created by liusha on 16/8/17.-->
        <div class="popupBody">
        <div class="stop-plan">
            <div class="icon-warn"></div><span>移除操作需要先结束使用此包的计划,请先结束相关计划？</span>
        </div>
        <div class="popup-footer">
            <div node-type="confirm-cancel" class="btn" @click="$emit('close')">确认</div>
        </div>
        </div></div>
            <div class="r-row comp-general-popover-foot"></div>
        </div>
        </div>
    </div>
</template>
<script>

</script>
<style>
.comp-general-popover-bg {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: initial;
    background-color: rgba(0,0,0,0.2);
    padding: 20px 0;
    z-index: 99999;
}
.comp-general-popover-body {
    min-width: 300px;
    height: initial;
    border-left: 1px solid #bababa;
    border-right: 1px solid #bababa;
    border-bottom: 1px solid #bababa;
    background: #fff;
    font-family: "'MicrosoftYaHei', 'Microsoft YaHei'", 'Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', 'Hiragino Sans GB', tahoma, arial, sans-serif;
    font-weight: 400;
    font-style: normal;
}
.comp-general-popover-bg .r-container-fluid {
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
}
.comp-general-popover-bg .comp-general-popover-body {
    display: inline-block;
    vertical-align: middle;
    max-width: 99%;
}
.comp-general-popover-body .comp-general-popover-head {
    height: 45px;
    line-height: 45px;
    border-top: 2px solid #22bb9a;
    border-bottom: 1px solid #f2f2f2;
    font-size: 14px;
    padding: 0 15px;
    font-weight: bold;
    text-align: left;
    -ms-word-break: break-all;
    word-break: break-all;
    word-break: break-word;
    -webkit-hyphens: auto;
    -moz-hyphens: auto;
    -ms-hyphens: auto;
    hyphens: auto;
}
.comp-general-popover-bg .r-row {
    margin-right: -15px;
    margin-left: -15px;
}
.comp-general-popover-body .comp-general-popover-head .comp-general-popover-close {
    float: right;
    width: 24px;
    height: 25px;
    margin-top: 8px;
    background-size: cover;
    cursor: pointer;
    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAyCAYAAAAayliMAAAC+0lEQ…EEaDJSGcZEQNk6TQNNBDQZqQxjIqBsnaaBJgKajFSG+QkleEi0mM9V2QAAAABJRU5ErkJggg==);
}
.comp-general-popover-bg .r-row {
    margin-right: -15px;
    margin-left: -15px;
}
.comp-general-popover-loading {
    text-align: center;
    margin: 5px 0;
}
.comp-general-popover-bg .r-row {
    margin-right: -15px;
    margin-left: -15px;
}
.popupBody {
    position: relative;
}
.stop-plan {
    height: /*76px;*/ 124px;
}
.icon-warn {
    width: 37px;
    height: 42px;
    margin: auto;
    background: url(/weiboad/apps/sf/images/tool-icon.png) -100px 0;
}
.stop-plan .icon-warn {
    margin: 20px auto 30px;
}
.popup-footer {
    background: #f5f5f5;
    height: 56px;
    text-align: center;
}
.popupBody .btn {
    padding: 0 15px;
    height: 28px;
    background: #22bb9a;
    border-radius: 3px;
    border: 1px #1fb191 solid;
    box-sizing: border-box;
    display: inline-block;
    line-height: 27px;
    color: #fff;
    cursor: pointer;
    text-align: center;
    min-width: 70px;
}
.popup-footer .btn {
    margin: 10px 5px;
    width: 102px;
    height: 36px;
    line-height: 35px;
}
</style>