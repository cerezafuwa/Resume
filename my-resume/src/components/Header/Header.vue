<template>
  <div id="header">
    <div class="header-content">
      <span>{{ introduction }}</span>
      <span>{{ project }}</span>
      <span>{{ education }}</span>
    </div>
  </div>

</template>
<script type="text/ecmascript-6">
  export default {
    name: 'header',
    data() {
      return {
        introduction:'Introduction',
        project: 'Project',
        education: 'Education'
      }
    }
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
