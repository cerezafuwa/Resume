<template>
  <div id="skill">
    <subtitle :titleName="titleName" id="subtitle-skill"></subtitle>
    <div class="skill-bg">
      <ul class="skills">
        <li v-for="skill in skills">
          <p>{{skill.name.toUpperCase()}}</p>
          <div class="score-container">
            <svg :style="getLengthStyle(skill)" class="score" xmlns:xlink="http://www.w3.org/1999/xhtml">
            </svg>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  import subtitle from "../Subtitle/Subtitle";

  export default{
    name: 'skill',
    components: {
      subtitle
    },
    methods: {
      getLengthStyle: function (skill) {
        return 'width: ' + skill.score * 200 + 'px'
      }
    },
    data(){
        return{
        }
    },
    props: ['skills','titleName']
  }
</script>
<style>
  #skill{
    margin-top: 150px;
    background-color: #f3f2fb;
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
    background-color: #c1c1c1;
    border-radius: 999em;
    width: 200px;
    height: 13px;
    display: inline-flex;
    margin-left: -50px;
  }
  li{
    display:block;
  }
  .score:hover{
    background-color: #d46e7a;
    box-shadow:0 0 5px #c0c0c0;

  }

  p{
    display:inline-block;
    width:50%;
    margin-top: 11px;
  }
  .score{
    height:13px;
    border-radius:999em;
    background-color: #74c8de;
  }


</style>
