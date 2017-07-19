<template>
  <div id="app">

    <v-header></v-header>
    <introduction></introduction>
    <skill></skill>

  </div>
</template>

<script>
import header from './components/Header/Header'
import introduction from "./components/Introduction/Introduction";
import skill from "./components/Skill/Skill";
export default {
  name: 'app',
  components: {
    'v-header': header,
    'introduction': introduction,
    'skill': skill
  },
  data(){
      return{
          resume: {}
      }
  },
  created: function () {
    this.$http.get('/static/resume-zh-CN.json').then(resp => {
      this.resume = resp.body
    })
  }
}
</script>

<style>
#app {

}
</style>
