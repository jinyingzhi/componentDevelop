<template>
  <div class="main">
    <section class="box">
        
      <ul class="lis">  
        <li>全部类目</li>
        <li>附近商家</li>
        <li>智能排序</li>
        <li>筛选</li>
      </ul>
      <div class="cont">
        <dl>
          <dt>
            <img src="../image/pic.png" alt="">
          </dt>
          <dd>
            <p class="title">{{options.title}}</p>
            <span class="price">￥{{options.price}}</span><span class="address">{{options.address}}</span><br>
            <span class="mz">{{options.mz}}</span> <span class="yd">{{options.yd}}</span>
            <p class="yud">{{options.yud}}</p>
            <section>
              <p class="tuan">{{options.tuan}}</p>
              <p class="quan">{{options.quan}}</p>
            </section>
          </dd>
        </dl>
      </div>
    </section>
  </div>
</template>

<script>

export default {
  props:['options']
}
</script>

 <style scoped>
  .main{
    flex: 1;
  }
  .box{
    display: flex;
    flex-direction: column;
  }
 
  .cont{
    flex: 1;
    margin-top: -20px;
  }
  .cont dl{
      width: 100%;
      height: 180px;
      display: flex;
      border-bottom: 1px solid #ccc;
  }
  .cont dt{
    /* margin-left: 60px; */
    width: 35%;
  }
  .cont dd{
    line-height: 20px;
    margin-top: -25px;
  }
  .cont section{
    display: inline-block;
    width:65%;
    height: 70px;
    border-top: 1px solid #ccc;
    line-height: 15px;
    margin-top: -5px;
  }
   .lis{
    display: flex;
    height: 45px;
    line-height: 45px;
    border-bottom: 1px solid #ccc;
  }
  .lis li{
    width: 25%;
    text-align: center;
    list-style: none;
  }
</style>
