<template>
  <div class="home-search-bar">
    <input v-model="searchText" class="input-search" type="text" @keydown.enter="doSearch">
    <button class="btn-search" @click="doSearch">搜索</button>
  </div>
</template>

<script>
import Util from "@/common/Util"
export default {
  name:"home-search-bar",
  data(){
    return{
      searchText:""
    }
  },
  methods:{
      doSearch(){
           Util.searchAPI(this.$router,this.searchText)
          
        }
      }
  }





</script>

<style lang="less" scoped>
@import "./../themes/base.less";

.home-search-bar{
  max-width:650px;
  
}
.input-search{
  outline: none ;//取消选中高光
  width:70%;
  height:@home-search-bar-height;
  box-sizing:border-box;
  border:solid 1px @color-border-gray;
  vertical-align: bottom;
  font-size: 1.2em;
  
  border-top-left-radius:@home-search-bar-border-radios;
  border-bottom-left-radius:@home-search-bar-border-radios;
  padding:20px;//搜索框内与左边框的距离
  
}
.btn-search{
  outline: none ;//取消选中高光
  width:30%;
  height:@home-search-bar-height;
  box-sizing:border-box;
  background-color: @color-primary;
  color: white;
  font-size: 1.6em;
  border:none;

  
  border-top-right-radius:@home-search-bar-border-radios;
  border-bottom-right-radius:@home-search-bar-border-radios;
  
}
</style>
