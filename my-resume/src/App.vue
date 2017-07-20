<template>
  <div id="app">

    <v-header></v-header>
    <introduction></introduction>
    <skill :titleName="titles.skill" :skills="resume.skills"></skill>

  </div>
</template>

<script>
import header from './components/Header/Header';
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
        resume: {},
        language: 'zh-CN',
        subtitles: {
          'zh-CN': {
            overview: '个人简介',
            project: '项目经历',
            skill: '专业技能',
            info: '了解更多'
          },
          'En': {
            overview: 'Overview',
            project: 'Projects',
            skill: 'Skills',
            info: 'Contact Me'
          }
        }
      }
  },
  computed: {
    titles: function () {
      return this.subtitles['zh-CN']
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
