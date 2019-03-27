<template>
  <div id="app">
    <headercom></headercom>
    <mainbody v-for="item in shoplist" :key="item.id" :options="item"></mainbody>
  </div>
</template>

<script>
import headercom from './components/headercom.vue'
import mainbody from './components/mainbody.vue'

import './font/iconfont.css'

export default {
  name: 'App',
  data(){
    return {
      shoplist:[{
        title:'小木船潮汕牛肉火锅',
        price:'114/人',
        address:'农业大学西区100m',
        mz:'潮汕牛肉火锅',
        yd:'回头客多',
        yud:'支持预定',
        tuan:'团:8人餐888元',
        quan:'券:93代100元',
        img:'../image/pic.png',
        id:0
      },{
        title:'林之雨精致料理铁板烧',
        price:'213/人',
        address:'农业大学西区100m',
        mz:'日式铁板烧',
        yd:'包间可订',
        yud:'支持预定',
        tuan:'团:单人餐198元',
        quan:'券:95代100元',
        img:'../image/pic.png',
        id:1
      }]
    }
  },
  components: {
    headercom,mainbody
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
}
</style>
