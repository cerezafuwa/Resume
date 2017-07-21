<template>
  <div id="header">
    <div class="header-content">
      <span><a href="#introduction">{{ nav_1 }}</a></span>
      <span><a href="#skill">{{ nav_2 }}</a></span>
      <span>{{ nav_3 }}</span>
      <span>{{ nav_4 }}</span>
    </div>
  </div>

</template>
<script type="text/ecmascript-6">
  import skill from "../Skill/Skill";
  import introduction from "../Introduction/Introduction";

  export default {
    name: 'header',
    data() {
      return {
      }
    },
    props:['nav_1','nav_2','nav_3','nav_4']
  }
</script>

<style>
  #header{
    position: fixed;
    width: 100%;
    z-index: 9999;
    background-color: #f3f2fb;
    opacity: 0.8;
  }

  .header-content{
    margin-right: 80px;
    display: flex;
    justify-content:flex-end;
    height: 60px;
    align-items: center;
  }

  span{
    margin: 7px;
  }
</style>
