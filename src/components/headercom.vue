<template>
    <div class="header">
        <span class="iconfont icon-zuojiantou left"></span>
        <input type="text" placeholder="请输入要搜索的内容" @keyup.enter="$emit('searchEvent',$event.target.value)">
        <span class="iconfont icon-gerentouxiang opp"></span>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.header{
    width:100%;
    height:40px;
    display: flex;
    background:pink;
    justify-content: space-around;
}
.left{
   
    line-height: 40px;
}
.opp{
    line-height: 40px;
}
</style>
