<template>
  <div id="header">
    <div class="header-content">
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
        project: 'Project',
        education: 'Education'
      }
    }
  }
</script>

<style>
  #header{
    height: 40px;
  }

  .header-content{
    display: flex;
    justify-content:flex-end;
  }

  span{
    margin: 7px;
  }
</style>
