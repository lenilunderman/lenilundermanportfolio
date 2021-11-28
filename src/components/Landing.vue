<template>
<div data-aos="fade-up" data-aos-easing="ease" data-aos-duration="300">
    <div class="landing-content">
        <div class="landing-wrapper">
            <div class="landing-greeting">
                <h3 style="display: inline;"> {{greeting}}</h3> <div class="animate__animated animate__tada animate__repeat-3" style="display: inline-block;"> &nbsp; 👋  &nbsp; </div> 
            </div>
            <h1> {{t1}} </h1>
            <h1>  {{t2}} </h1>
            <h1>  {{t3}} </h1>
            <p>
                {{headingInfo}}
            </p> 
        </div>
  
        <div class="cta-buttons">
            <a :href="email" target="_blank"><button>Connect with me </button></a>
            <a :href="resume" target="_blank"><button>Download CV </button></a>
        </div>

    </div>
</div>  
</template>

<script>
export default {
    data(){
        return{
            greeting:"Hi, I'm Leni",
            t1:'I build digital',
            t2:'products, websites,',
            t3:'and experiences',
            headingInfo:"I'm a coder and enthusiastic developer. I love to learn about new technologies and frameworks. Vue is my specialty but I have significant expertise in React as well. I am resourceful, self-motivated, and love to create beautiful designs and applications. I am fluent in Portuguese.",
            email:'https://us1.list-manage.com/contact-form?u=9e3da0d8a733d15ee81ab58b6&form_id=d3df97378ef48177327f8dd2e00ed707',
            resume:'https://drive.google.com/file/d/1AJPs5c5uqP4-OXEfWkmLrNCGVSrf1SXM/view'
        }
    }
}
</script>

<style>
    .landing-wrapper{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 25px 0px;
        font-family: 'Montserrat', sans-serif;
        /* animation: slowDisplay;
        animation-duration: 2.5s; */
    }
    .landing-greeting{
        padding: 20px;
    }
    .heading{
        padding: 40px 10px 20px 10px;
    }
    .cta-buttons{
        display: flex;
        align-items: center;
        justify-content: center;
    }

    button{
    padding: 15px 25px;
    border:none;
    margin: 0px 15px;
    transition: all 0.3s ease 0s;
    background-color: rgb(0, 0, 0);
    cursor: pointer;
    color:white
    }

    button:hover{
    background-color: rgba(16, 31, 129, 0.8);
    color: rgb(255, 255, 255);
    }

     h1{
        font-size: 3.2rem;
    }

    p{
        font-size: 1.0rem;
        width: 40rem;
        font-weight: 300;
        text-align: center;
        line-height: 1.5rem;
        padding: 25px 0px 10px 0px;
    }


    @media screen and (max-width: 680px) {
        h1{
            font-size: 2.5rem;
        }
        p{
            font-size: 0.8rem;
            width:30rem;
            text-align: center;
        }
    }

    @media screen and (max-width:480px) {
        h1{
            font-size:1.8rem
        }
        p{
            width: 20rem;
            text-align: center;
        } 
    }

    /* @keyframes slowDisplay {
        0%{
            opacity: 0;
        }
        50%{
            opacity: 0.5;
        }
        100%{
            opacity: 1;
        }
        
    } */

</style>