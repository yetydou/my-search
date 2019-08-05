//搜索页面内容
<template>
  <div class="search-result-item">
    <a class="search-result-item-link" :href="info.url">
      <div class="title">{{info.title}}</div>
      <div class="url">{{info.url}}</div>
      <div class="desc">{{info.data}}--{{info.desc}}</div>
   </a>
  </div>
</template>

<script>
export default {
  props:["info"]
}
</script>

<style lang="less" scoped>
.search-result-item{
  //border:solid 1px red;
  text-align: left;
  padding: 20px;
}
.search-result-item-link{
  text-decoration: none;//去除下划线
}
.title{
  color:blue;
  font-size: 1.3em;
}
.url{
  color:yellowgreen;
  font-weight:bold;
}
.desc{
  color:brown;
}
</style>
