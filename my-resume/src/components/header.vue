<template>
  <div id="header">
    {{ msg }}
  </div>
</template>
<script>

  export default{
    name: 'header',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>
<style scoped>
  #header{
    height: 400px;
  }
</style>
