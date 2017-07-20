<template>
  <div class="subtitle" :id="id">
    <div class="subtitle-content">
      <p>—</p>
      <h2>{{titleName}}</h2>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
      name: 'subtitle',
      props: ['titleName', 'id']
  }
</script>

<style>
  .subtitle{
    margin:-50px 6%;
    background:url("red.svg") no-repeat;
    background-size:100% 100%;
    width:100px;
    height:100px;
    border-radius:6px;
    z-index:999;
    position:absolute;
    transition-duration:0.5s;
    box-shadow:0 0 0 0 #aaa;
  }

  .subtitle-content{
    color:#fff;
    padding-left:10px;
    width:100px;
  }

  p{
    font-size:17px;
    font-weight:400;
  }

  h2{
    margin: 0 5px;
    font-size:17px;
    font-weight:400;
  }

  .subtitle:hover{
    border-radius:15px;
    box-shadow:0 0 5px 0 #f5549e;
  }

</style>
