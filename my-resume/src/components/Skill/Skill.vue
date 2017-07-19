<template>
  <div id="skill">
    <subtitle :titleName="titleName" id="subtitle-skill"></subtitle>
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
  import subtitle from './components/Subtitle/Subtitle'

  export default{
    name: 'skill',
    components: {
      'subtitle': subtitle,
    },
    data(){
        return{

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
