<template>
  <div id="app">
    <div class="header">
         <span class="iconfont icon-zuojiantou ico" ></span>
      <input type="text" class="tet">
      <span class="iconfont icon-gerentouxiang gr"></span>
    </div> 
     <div class="nav">
       <ul class="list">
        <li>全部类目</li>
        <li>附近商家</li>
        <li>智能排序</li>
        <li>筛选</li>

      </ul>
    </div>
    <listmain v-for="item in lists" :key="item.id" :options="item"></listmain> 
  </div>
</template>

<script>
import "./assets/font/iconfont.css"
import listmain from "./components/HelloWorld.vue"
export default {
  name: 'App',
  data(){
    return{
      lists:[
        {
          img:"img1.png",
          title:"小木船潮汕牛肉火锅(马连洼店)",
          id:0,
          price:"114/人",
          add:"农业大学西区",
          description:["第三名","回头率多"]
        },
        {
          img:"img2.png",
          title:"林之语精致料理铁板烧(上地店)",
          price:"213/人",
          id:1,
          add:"农业大学西区",
          description:["第三名","回头率多"]
        },
        {
          img:"img3.png",
          title:"70后餐厅",
          price:"66/人",
          id:2,
          add:"农业大学西区",
          description:["第三名","回头率多"]
        }
      ]
    }
  },
  components:{listmain}
}
</script>

<style>
.header{
  width:100%;
  height:50px;
  background:#EBECED;
  border-bottom: 1px solid gray;
}
.ico{
  line-height: 50px;
}
.tet{
  width:300px;
  height:30px;
  border-radius: 20px;
}
.nav{
  width:100%;
  height:40px;
  background:#FFFFFF;
}
.nav ul{
  width:100%;
  height:100%;
  list-style: none;
  display: flex;
  border: 1px solid gray;
}
.nav ul li{
  width:25%;
  line-height: 40px;
  text-align: center;
}
</style>
