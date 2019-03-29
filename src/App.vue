<template>
  <div class="meituan-listr">
    <headercom @searchEvent="searchFn"></headercom>
    <toolbarcom @sortEvent="sortFn"></toolbarcom> 
    <listcom :options="infolist"></listcom> 
  </div>
</template>

<script>
import icons from "./assets/font/iconfont.css"
import headercom from "./components/headercom.vue"
import toolbarcom from "./components/toolbar.vue"
import listcom from "./components/listcom.vue"
let datajson=[
                {
            "id": 0,
            "frontImg": "https://img.meituan.net/msmerchant/4ec3dd6b6dc8add6f845c5242c24a0d3147795.jpg",
            "name": "惠丰堂饭庄（唐家岭店）",
            "areaName": "海淀区",
            "distance": "412m",
            "avgPrice": 86,
            "avgScore": 5,
            "cateName": "鲁菜",
            "maidan": [
                {
                    "content": "6人餐498元，12人餐898元起",
                    "icon": "http://p1.meituan.net/codeman/93231059874052e97c0976c8a6e30dbe910.png"
                },
                {
                    "content": "89.8代100元",
                    "icon": "http://p1.meituan.net/codeman/5b202af2ecf82c69a433a246296ca4791278.png"
                }
            ]
        },
         {
            "id": 1,
            "frontImg": "https://img.meituan.net/msmerchant/4ec3dd6b6dc8add6f845c5242c24a0d3147795.jpg",
            "name": "北京鲜火锅",
            "areaName": "海淀区",
            "distance": "390m",
            "avgPrice": 80,
            "avgScore": 3.5,
            "cateName": "火锅",
            "maidan": [
                {
                    "content": "69代100元，78代100元",
                    "icon": "http://p1.meituan.net/codeman/93231059874052e97c0976c8a6e30dbe910.png"
                },
                {
                    "content": "买单立享7.8折",
                    "icon": "http://p1.meituan.net/codeman/5b202af2ecf82c69a433a246296ca4791278.png"
                }
            ]
        },{
            "id": 2,
            "frontImg": "https://img.meituan.net/msmerchant/4ec3dd6b6dc8add6f845c5242c24a0d3147795.jpg",
            "name": "太熟悉家常菜（北清路店）",
            "areaName": "海淀区",
            "distance": "2.3km",
            "avgPrice": 182,
            "avgScore": 3.4,
            "cateName": "家常菜",
            "maidan": [
                {
                    "content": "6人餐498元，12人餐898元起",
                    "icon": "http://p1.meituan.net/codeman/93231059874052e97c0976c8a6e30dbe910.png"
                },
                {
                    "content": "89.8代100元",
                    "icon": "http://p1.meituan.net/codeman/5b202af2ecf82c69a433a246296ca4791278.png"
                }
            ]
        }
            ]
export default {
  name: 'App',
  components: {headercom,toolbarcom,listcom},
   data(){
        return{
            infolist:datajson
        }
    },
    methods:{
      sortFn(id){
        // console.log(id)
       if(id==3){
         this.infolist.sort((a,b)=>{
           return a.avgPrice-b.avgPrice
         })
       }else if(id==2){
         this.infolist.sort((a,b)=>{
           return a.avgScore-b.avgScore
         })
       }
      },
      //搜索功能
      searchFn(txt){
        //   alert(txt)
      this.infolist=datajson
        this.infolist=this.infolist.filter((item)=>{
            return item.name.indexOf(txt)!==-1
        })
      }
    }
}
</script> 

<style>

</style>
