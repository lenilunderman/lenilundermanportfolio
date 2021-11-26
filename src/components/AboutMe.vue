<template>
<!-- <figure class="c4-izmir">
  <img src="https://source.unsplash.com/FaPxZ88yZrw/400x300" alt="Sample Image">
  <figcaption>
      <h3>
        Some sample text
      </h3>
    </figcaption>
</figure> -->

    <h2 class="heading-aboutme" id="aboutme"> | {{sectionName}} | </h2> 
    
    <div class="aboutme-section">
        <div class="aboutmeInfo">

            <h1> {{brandTag}} </h1>
            <div class="aboutmePblock">
                <br>
                <p> {{p1}} <br><br>
                    {{p2}} <br><br>
                    {{p3}} 
                </p>
            </div>
          
        </div>

        <div class="aboutmeImg">

            <img :src="imgLink" alt="dev">

        </div>
    </div>

</template>

<script>
export default {
    data(){
        return{
            sectionName:'About Me',
            brandTag:'Web Developer',
            p1:'Hi there! I am a software engineer from the Boston area, and I love to create clean and modern websites and applications. I believe products should bring users a great experience, ease of use, and efficiency.',
            p2:'I am highly motivated, self-driven, and resourceful with experience in Javascript, React, Vue, Python, Django, and other technologies.',
            p3:'My goal is to innovate one project at a time.',
            imgLink:'https://i.ibb.co/fYnm6XM/leni-final.png',
        }
    }

}
</script>

<style>
    /* Style for the gallery of the website  */
    @import '../assets/styles/gallery.css';
    
    .heading-aboutme{
        text-align: center;
    }
    
    .aboutme-section{
        display:flex;
        width: 85vw;
        margin: 0 auto;
        flex-wrap: wrap;
        
    }
    .aboutmeInfo{
        flex: 2 auto;
        padding: 15px 0px 15px 30px;
        position: relative;
    }
    .aboutmeInfo h1 {
        
        font-size:7.4rem;
        text-align: left;
        margin-bottom: 50px;
        position: absolute;
        top: 1px;
        color: rgba(197, 194, 194, 0.396);
        width: 90%;
        user-select: none; 
    }
    .aboutmeInfo p {
        font-size:1.1rem;
        text-align: left;
        line-height: 1.5rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 300;
    }
    .aboutmeImg img{
        width:480px;
        height:350px;
        transform: scaleX(1);
    }
    .aboutmeImg{
        flex: 1;
    }

    .aboutmePblock{
        margin-top: 80px;
        z-index: 10;
    }
    .heading-aboutme {
        
        padding: 25px 0px;
    }

    /* Media queries sections for different devices */

    @media screen and (max-width:1350px){
        .aboutmeInfo{
            display: inline-block;
        }
        .aboutmeInfo h1{
            text-align:center;
            margin-top: 25px;
        }
        .aboutmeImg img{
            display: none;
        }
        .aboutmePblock p{
        text-align:center;
        width:80vw;  
        } 
    }


    @media screen and (max-width:920px){
        .aboutmeInfo h1{
            margin-top:25px;
            font-size: 3.8rem;
        }
        .aboutmePblock p{
            font-size:0.9rem;
        }
    }


    @media screen and (max-width:680px){
        .aboutmeInfo h1{
            font-size: 2.8rem;
        }
    }

    @media screen and (max-width:480px){
        .aboutmeInfo{
            order: 2;
            padding: 15px 10px 15px 10px;
        }
        .aboutmeImg img{
            display:block;
            width: 320px;
            height: 280px;
            transform: scaleX(1);
        }
        .aboutmeInfo h1{
            font-size: 2.4rem;
        }
        .aboutmeInfo p{
            text-align: center;
        }
    }
</style>