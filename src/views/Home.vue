<template>
  <div class="home">
    <div class="home-search-panel">
      <MySearchLogo class="my-search-logo"/> 
      <HomeSearchBar class="home-search-bar"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import MySearchLogo from '@/components/MySearchLogo.vue'
import HomeSearchBar from '@/components/HomeSearchBar.vue'

export default {
  name: 'home',
  components: {
    
    MySearchLogo,
    HomeSearchBar
  }
}
</script>

<style lang="less" scoped>
.home-search-panel{
  text-align: center;//整体居中
}
.my-search-logo{
  margin-top: 60px;
  margin-bottom: 30px;//搜索框与图标之间增加间隔
}
.home-search-bar{
  margin: auto;
}
</style>
