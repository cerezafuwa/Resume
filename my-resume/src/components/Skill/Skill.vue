<template>
  <div id="skill">
    <div class="skill-bg">
      <ul class="skills">
        <li v-for="skill in skills">
          <p>{{skill.name.toUpperCase()}}</p>
        </li>

      </ul>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    name: 'skill',
    data(){
        return{
          "skills": [
            {
              "name": "javascript",
              "score": 0.7
            },
            {
              "name": "html",
              "score": 0.9
            },
            {
              "name": "css",
              "score": 0.8
            },
            {
              "name": "java",
              "score": 0.75
            },
            {
              "name": "c++",
              "score": 0.7
            },
            {
              "name": "c",
              "score": 0.6
            },
            {
              "name": "git",
              "score": 1
            },
            {
              "name": "photoshop",
              "score": 0.95
            },
            {
              "name": "illustrator",
              "score": 0.95
            },
            {
              "name": "corel painter",
              "score": 0.75
            }
          ]
        }
    }
  }
</script>
<style>
  #skill{
    margin-top: 150px;
  }
  .skill-bg{
    height: 150px;
    margin-left: 100px;
  }
  .skills{
    column-count: 2;
  }
  li{
    display: inline;
  }
</style>
