<template>
  <div class="contactMeIcons">
        <span v-for="item in socialLinks" :key="item.iconName">
            <a :href="item.skillWebsite" target="_blank"><i :class="item.skillClass"></i></a>
        </span>
       <div class="vertical-line"></div>
  </div>

</template>

<script>
export default {
    // This component uses font awesome, to get the right icon for the page, visit the website 
    // https://fontawesome.com/v6.0/icons?s=solid%2Cbrands

    data(){
        return{
            socialLinks:[
                {id:1, skillClass:'fa-brands fa-linkedin-in fa-2xl', iconName:'linkedin', skillWebsite:'https://www.linkedin.com/in/lenilunderman/'},
                {id:2, skillClass:'fa-brands fa-github fa-2xl', iconName:'github', skillWebsite:'https://github.com/lenilunderman'},
                {id:3, skillClass:'fa-brands fa-twitter fa-2xl', iconName:'twitter', skillWebsite:'https://twitter.com/lenny_lunderman'}
            ]
        }
    }
}
</script>

<style>
    .contactMeIcons {
        display: flex;
        flex-direction: column;
        position: fixed;
        bottom: 0;
        left: 0%;
        padding:10px 20px;
    }
    span{
        margin-bottom: 10px;
        padding: 10px;
    }   

  .contactMeIcons span:hover{
      transform:scale(1.2);
      /* transform: rotate(15deg); */
      transition: all 0.5s ease;
    }

    .vertical-line{
        height:4rem;
        width: .2rem;
        background-color: black;
        margin-left: 40%;  
    }

    @media screen and (max-width:1170px){
      .contactMeIcons{
          widows: 60px;
          padding:5px 5px;
      }
    }
    @media screen and (max-width:800px){
        .contactMeIcons{
            display:none;
        }
    }
 

</style>