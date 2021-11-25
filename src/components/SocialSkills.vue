<template>
  <div class="social-skills">
      <div class="social-skills-wrapper" id="services">
        <div v-for="skill in skillSet" :key="skill.id">
          <img :src="skill.skillUrl" :alt="skill.skillname">
        </div>
      </div>
  </div>
  
  
</template>

<script>
export default {
  data(){
    return{
      skillSet:[
        { id:1, skillname:'html', skillUrl:'https://img.icons8.com/color/48/000000/html-5--v1.png' },
        { id:2, skillname:'css3', skillUrl:'https://img.icons8.com/color/48/000000/css3.png' },
        { id:3, skillname:'sass', skillUrl:'https://img.icons8.com/color/48/000000/sass.png' },
        { id:4, skillname:'javascript', skillUrl:'https://img.icons8.com/color/48/000000/javascript--v1.png' },
        { id:5, skillname:'react', skillUrl:'https://img.icons8.com/color/48/000000/react-native.png' },
        { id:6, skillname:'nodejs', skillUrl:'https://img.icons8.com/fluency/48/000000/node-js.png' },
        { id:7, skillname:'vuejs', skillUrl:'https://img.icons8.com/color/48/000000/vue-js.png' },
        { id:8, skillname:'python', skillUrl:'https://img.icons8.com/color/48/000000/python--v1.png' },
        { id:9, skillname:'django', skillUrl:'https://img.icons8.com/color/48/000000/django.png' },
        { id:10, skillname:'mongodb', skillUrl:'https://img.icons8.com/color/48/000000/mongodb.png' },
        { id:11, skillname:'postgresql', skillUrl:'https://img.icons8.com/color/48/000000/postgreesql.png' },
        { id:12, skillname:'git', skillUrl:'https://img.icons8.com/color/48/000000/git.png' },
        { id:13, skillname:'notion', skillUrl:'https://img.icons8.com/color/48/000000/notion--v1.png' },
        { id:14, skillname:'mailchimp', skillUrl:'https://img.icons8.com/bubbles/50/000000/mailchimp.png' }, 
      ]
    }
  }
}
</script>

<style>
    .social-skills-wrapper {
      display: flex;
      flex-wrap: wrap;
      width: 85vw;
      margin: 0 auto;
      justify-content:space-around;
      text-align: center;
      align-items: center;
      padding:30px 0px;
      
    }
    .social-skills-wrapper img{
      width:60px;
    }
    .social-skills-wrapper div{
      margin: 5px 0px 0px 5px;
    }
    .social-skills-wrapper div:hover{
      transform:scale(1.2);
      /* transform: rotate(15deg); */
      transition: all 0.5s ease;
    }

    @media screen and (max-width:1080px){
      .social-skills-wrapper img{
      width:40px;
      }
      .social-skills-wrapper>* {
      flex: 1 1 100px;
    }
    }

</style>