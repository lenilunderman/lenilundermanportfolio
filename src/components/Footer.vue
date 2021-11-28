<template>
<div data-aos="fade-up" data-aos-duration="600">
  <div class="footer-section">
      <footer>
          <h1> {{pageTitle}} </h1>
          <h3> {{pageHeading}} </h3>
          
          <address><a href="https://us1.list-manage.com/contact-form?u=9e3da0d8a733d15ee81ab58b6&form_id=d3df97378ef48177327f8dd2e00ed707" target="_blank"> lenilunderman@gmail.com </a> </address>
          <div class="footerNetworkLinks">
            <span v-for="item in socialLinks" :key="item.iconName">
                <a :href="item.skillWebsite" target="_blank"><i :class="item.skillClass"></i></a>
            </span>
          </div>
      </footer>
  </div>
</div>
</template>

<script>
export default {
    // This component uses font awesome, to get the right icon for the page, visit the website 
    // https://fontawesome.com/v6.0/icons?s=solid%2Cbrands

    data(){
        return{
            pageTitle:'| Contact Me |',
            pageHeading: "Let's create your next digital product together.",
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
    .footer-section{
        width: 85vw;
        margin: 0 auto;
    }
    footer{
        font-family: 'Montserrat', sans-serif;
        margin-top: 5rem;
        text-align: center;
    }
    footer h1{
        font-size:3rem;
        margin-bottom:2rem;
    }
    footer h3{
        padding: 0.5rem;
        font-weight: 400;
    }
    address{
        font-family: 'Montserrat', sans-serif;
        margin: 15px 10px;
        font-weight: 800;
        font-style:normal;
    }
    address a{
        font-size:1.2rem;
        font-weight: 300;
    }

    address a:hover{
        padding-bottom: 3px;
        background-color: #e2e5eb;
        padding: 0px 10px;
        transition: all 0.3s ease-in-out;
    }

    .footerNetworkLinks{
        padding: 50px 0px 70px 0px;
    }
    .footerNetworkLinks span{
        margin: 0px 1rem;
        padding-bottom: 6px;
    }
    @media screen and (max-width:880px){
        footer h1{
            margin-top:25px;
            font-size: 2.6rem;
        }
    }

    @media screen and (max-width:680px){
        footer h1{
            margin-top:25px;
            font-size: 2.4rem;
        }
        footer h3{
            font-size: 1.1rem;
        }
        address a{
        font-size:1rem;
        font-weight: 300;
        }
        .footerNetworkLinks{
        padding: 45px 0px 35px 0px;
        }
        .footerNetworkLinks span{
            margin: 0px 0.5rem;
        }
    }
    @media screen and (max-width:490px){
        footer h1{
            margin-top:25px;
            font-size: 2.4rem;
        }
        footer h3{
            font-size: 0.9rem;
        }
        .footerNetworkLinks{
        padding: 25px 0px 50px 0px;
        }
    }

</style>