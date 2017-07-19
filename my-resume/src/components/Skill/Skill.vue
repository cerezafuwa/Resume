<template>
  <div id="skill">
    <div class="skill-bg">
      <ul class="skills">
        <li v-for="skill in skills">
          <p>{{skill.name.toUpperCase()}}</p>
          <div class="score-container"></div>
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
//          "skills": [
//            {
//              "name": "javascript",
//              "score": 0.7
//            },
//            {
//              "name": "html",
//              "score": 0.9
//            },
//            {
//              "name": "css",
//              "score": 0.8
//            },
//            {
//              "name": "java",
//              "score": 0.75
//            },
//            {
//              "name": "c++",
//              "score": 0.7
//            },
//            {
//              "name": "c",
//              "score": 0.6
//            },
//            {
//              "name": "git",
//              "score": 1
//            },
//            {
//              "name": "photoshop",
//              "score": 0.95
//            },
//            {
//              "name": "illustrator",
//              "score": 0.95
//            },
//            {
//              "name": "corel painter",
//              "score": 0.75
//            }
//          ]
        }
    },
    props: ['skills']
  }
</script>
<style>
  #skill{
    margin-top: 150px;
    background-color: #edecf5;
  }
  .skill-bg{
    height: 240px;
    margin-left: 200px;
    width: 80%;
  }
  .skills{
    column-count: 2;
    column-gap: 100px;
  }
  .score-container{
    background-color: darkseagreen;
    border-radius: 999em;
    width: 150px;
    height: 10px;
    display: inline-flex;
    margin-left: -20px;
  }
  li{
    display:block;
  }
  .score-container:hover{
    background-color: firebrick;
  }
  p{
    display:inline-block;
    width:50%;
    margin-top: 13px;
  }

</style>
