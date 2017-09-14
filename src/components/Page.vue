<template>
<div class="clearfix">
    <div id="page" class="Pagination">
    <span class="current prev">&lt;</span>
    <span class="current">1</span>
    <a href="#">2</a>
    <a href="#">3</a>
    <a href="#">4</a>
    <a href="#">5</a>
    <a href="#" class="next">&gt;</a>
    </div>
</div>
</template>
<script>

</script>
<style>
.Pagination {
    margin-top: 10px;
    float:right
}
.Pagination .current.prev, .Pagination .current.next {
    color: #999;
    border-color: #999;
    background: #fff;
}
.Pagination .current {
    background-color: #22bb9a;
    color: #f5fbf9;
    font-size: 12px;
}
.Pagination a, .Pagination span {
    display: inline-block;
    width: 20px;
    height: 20px;
    margin-right: 5px;
    margin-bottom: 5px;
    line-height: 20px;
    text-align: center;
}
.Pagination a {
    text-decoration: none;
    color: #828287;
    font-size: 12px;
}
</style>