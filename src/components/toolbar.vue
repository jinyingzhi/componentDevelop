<template>
    <ul class="listbar">
        <li v-for="item in toollist" :class="{active:i==item.id}" :key="item.id" @click="itemTab(item.id)">{{item.name}}<span :class="['iconfont',i==item.id?'icon-xiasanjiao':'icon-top-s'] "></span></li>
    </ul>
</template>

<script>
export default {
    data(){
        return {
            i:null,
           toollist:[
            {name:"全部类目",id:0},
            {name:"附近商家",id:1},
            {name:"星级排序",id:2},
            {name:"价格排序",id:3}
        ] 
        }
            
    },
    methods:{
        itemTab(id){
            this.$emit('sortEvent',id)
            this.i=id
        }
    }
}
</script>

<style>
ul{
    width:100%;
    height:40px;
    border:1px solid gray;
    display: flex;
    list-style: none;
    margin:0;
    padding:0;
    justify-content: space-around;
}
ul li{
    line-height: 40px;
}
.active{
    color:pink;

}
</style>
