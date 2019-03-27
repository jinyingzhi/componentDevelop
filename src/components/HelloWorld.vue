<template>
     
    <div class="listmain">
       <!-- {{options}} -->
      <img src="../assets/img1.png" alt="">
      <div class="info">
        <b>{{options.title}}</b>
        <span class="price">{{options.price}}</span><span class="add">{{options.add}}</span>
        <p><span>潮汕火锅</span><span>回头率高</span></p>
        <span>支持预定</span>
      </div>
    </div>
</template>

<script>
export default {
   props:["options"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
