<template>
  <div id="introduction">
    <div class="introduction-bg">
      <div class="introduction-rec1"></div>
      <div class="introduction-rec2"></div>

    </div>
  </div>
</template>
<script type="text/ecmascript-6">
export default{
    name: 'introduction'
}
</script>

<style>

  .introduction-bg{
    width: 500px;
    height: 400px;
  }
  .introduction-rec1{
    position: relative;
    height: 80px;
    width: 80px;
    background-color: lightpink;
    border-radius: 10px;
    opacity: 0.6;
    left:147px;
    top:100px;
  }
  .introduction-rec2{
    position: relative;
    height: 100px;
    width: 100px;
    background-color: blue;
    border-radius: 10px;
    opacity: 0.1;
    left: 200px;
    top:80px;
  }
</style>
