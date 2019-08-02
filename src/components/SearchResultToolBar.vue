//搜索工具栏
<template>
  <div class="search-result-toolbar">
    <img class="logo" src="./../assets/logo 2.png" @click="goHome">
    <RoundSearchBar :search="search" /> 
  </div>
</template>


<script>
import RoundSearchBar from '@/components/RoundSearchBar.vue'
export default {
  name:'search-result-toolbar',
  props:['search'],
  components:{
    RoundSearchBar
  },
  methods:{
    goHome(){
      this.$router.push("/")
    }
  }
}
</script>

<style lang="less" scoped>
@import "./../themes/base.less";
.search-result-toolbar{
  text-align: left;//整体居左
  padding: @space-large;
  border-bottom: solid 1px @color-border-gray;
}
.logo{
  height: @round-search-bar-height*0.8;//logo高度
  vertical-align: middle;
  margin:@space-large;

}
</style>
