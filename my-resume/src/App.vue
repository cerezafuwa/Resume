<template>
  <div id="app">

    <v-header></v-header>
    <introduction></introduction>
    <skill :skills="resume.skills"></skill>

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

  created () {
    this.fetchData()
  },
  watch:{
    '$route':'fetchData'
  },
  methods:{
    fetchData(){
      this.$http.get('/static/resume-zh-CN.json').then((response)=>{
      this.resume = response.body
    })
    }
  }

}
</script>

<style>
#app {

}
</style>
