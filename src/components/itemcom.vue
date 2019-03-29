<template>
    <div class="minbox">
        <img :src="options.frontImg" alt="">
        <div class="leftbox">
            <div class="top">
                <b class="title">{{options.name}}</b>
                <span class="pf">{{options.avgScore}}</span>
                <span class="price">￥{{options.avgPrice}}</span>
                <span class="add">{{options.areaName}}</span>
                <span class="info"><span>回头率多</span><span>回头率多</span><span>回头率多</span></span>
                <span class="yd">{{options.yd}}</span>
            </div>
            <div class="bottom">
                <p v-for="(v,index) in options.maidan" :key="index"><span></span>{{options.content}}
                <img :src="v.icon">
                <span>{{v.content}}</span>
                </p>
                 
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:["options"]
}
</script>

<style>
.minbox{
    margin:0;
    padding:0;
    width:100%;
    height:200px;
    display: flex;
    justify-content: space-around;
      border:1px solid gray;
}
img{
   width:30%;
   height:100px;
   margin:10px;
}
.leftbox{
    width:70%;
    height:200px;
    margin:0;
    padding:0;
  
}
.leftbox .title{
    margin:10px;
    display: inline-block;
}
.leftbox .pf{
    margin-left:10px;
}
.leftbox .info{
    margin-left:10px;
    margin-top:6px;
}
.leftbox .yd{
    margin-left:10px;
    margin-top:6px;
}
.leftbox span{
    display: inline-block;
}
.top{
    height:120px;
    margin:0;
    padding:0;
    border-bottom:1px solid gray;
}
.bottom{
    height:70px;
   
 
}
.bottom p{
 line-height: 30px;

}
.bottom img{
    width:10px;
    height:10px;
}
.bottom p{
    height:30px;
    margin:0;
    padding:0;
     display: flex;
}
.bottom span{
    display: inline-block;
}
</style>
