<template>
<div data-aos="fade-up" data-aos-easing="ease" data-aos-duration="500">
    <div class="other-projects">
<div data-aos="fade-down" data-aos-easing="ease" data-aos-duration="1000">
            <div class="other-projects-bgtext">
                <h1> {{titleBigText}} </h1>
            </div>
</div>
        <div class="other-projects-wrapper">
            <div v-for="item in projects" :key="item.id" class="project-overlay" id="projItem">
                    <figure class="c4-izmir c4-border-center c4-gradient-top-left c4-image-zoom-out" style="--primary-color: #22a87b; --secondary-color: #1CB5E0; --border-width: 2.5px; --overlay-opacity: 0.1;">
                <img :src="item.bgImg" :alt="item.projectName">
                <figcaption>
                    <h3> {{item.projectName}}</h3>
                    <p> {{item.projectDesc}} </p>
                        <span class="btn-section" v-if="item.repoL">
                            <button> <a :href="item.repoL" target="_blank"> Repo </a>  </button>
                            <button> <a :href="item.urlSite" target="_blank"> Explore </a> </button>
                        </span>
                            <span class="btn-section" v-else>
                            <button><a href="item.urlSite" target="_blank"> Explore </a></button>
                        </span>
                </figcaption>
                </figure>
            </div>
        </div>
    </div> 
</div>
</template>

<script>
export default {

    data(){
        return{
            titleBigText: 'Web Projects',
            hover:false,
            projects:[
                {
                    id:1, 
                    projectName: 'Hulu Clone', 
                    projectDesc:'Application created using Tailwind CSS Framework, React, and 3rd party API to integrate data. This application demonstrates the basics of React and how to manipulate data.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16821737/media/dc72b0842bd2f538950db6d39d713daf.png', 
                    repoL:'https://github.com/lenilunderman/huluclone', 
                    urlSite:'https://huluclone.vercel.app/?genre=fetchTrending'
                },
                {   
                    id:2, 
                    projectName: 'Totally Wired Sculpture', 
                    projectDesc:"An e-commerce website created used WordPress and E-commerce to sell wired sculptures across the US. The initial design and initial sketch for this website was made in Figma.",
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16822012/media/b026d393b9e0566154c4e416d3a4450d.png',
                    repoL:null, 
                    urlSite:'https://murphywired.com'
                },
                {
                    id:3, 
                    projectName: 'Social Media Trends', 
                    projectDesc:'A simple application using Javascript ES6 and Bulma CSS Framework. This application demonstrates how to use array functions and how to integrate a licensed chart library.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16822454/media/8ebf9f4fe9dc57dd7e4a7d9ecec23aeb.png', 
                    repoL:'https://github.com/lenilunderman/social_media_trends', 
                    urlSite:'https://lenilunderman.github.io/social_media_trends/'
                },
                {   
                    id:4, 
                    projectName: 'ToRo Player', 
                    projectDesc:'A fun project created using HTML5, SCSS, vanilla javascript, and the audio web API, a clean way to keep all your music in one place, and list it whenever you like it.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16822552/media/5aa5e12d789d8b560aedad2668aadabb.png',
                    repoL:'https://github.com/lenilunderman/ToRoMusicPlayer', 
                    urlSite:'https://lenilunderman.github.io/ToRoMusicPlayer/'
                },             
            ]
        }
    },

    methods:{
        mouseIn(item){
            console.log(item.display);
            item.display = !item.display;
        },
        mouseOut(item){
            console.log(item.display);
            item.display = !item.display;
        }
    
    }
}


</script>

<style>
   /* Style for the gallery of the website  */
    @import '../assets/styles/gallery.css';

    .other-projects {
        /* --primary-color: #22a87b; 
        --secondary-color: #1CB5E0; */
        width:85vw;
        margin:0 auto;
        position: relative;
        font-family: 'Playfair Display', serif;
    }
    .other-projects-bgtext h1{
        
        font-size:7.4rem;
        user-select: none;
        text-align: right;
        color: rgba(128, 128, 128, 0.24);
        z-index: 10;
        margin-bottom: 10px;
        
    }
    .other-projects-wrapper{
        display:grid;
        /* margin-top: 25px; */
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        grid-row-gap:    15px;
        grid-column-gap: 15px;
        justify-content: space-around;
        align-items: inherit;
    }
    .other-projects-wrapper div{
        min-height: 280px;
    }
    .other-projects-wrapper div{
        min-height: 280px;
        /* background-color:rgb(170 182 201 / 35%); */
        transition: all 2.5 ease-in-out;
        opacity:.85;
        background-position: center;
        background-repeat: no-repeat;
        background-position: center;
        background-repeat: no-repeat; 
        object-fit: contain;
        background-size: cover;
        font-family: 'Montserrat', sans-serif;
        justify-content:center;
    }
   
    .project-overlay h3{
        text-align:center;
        padding-top:15px;
        height:40px;
        font-weight: 400;
        font-size: 1.2vw;
    }
    .project-overlay p{
        width: 95%;
        text-align:center;
        text-align:center;
        margin: 0 auto;
        font-size: 0.7vw;
        padding-top: 5px;
    }

    .btn-section{
        width: 100%;
        display: inline-block;
        margin: 0 auto;
        text-align: center;
        /* margin-top: 25px; */
    }
    .btn-section button{
        padding: 10px 15px;
        margin: 0px 5px;
        width:fit-content;
        
    }

    .btn-section a{
        color: white;
    }

    .c4-izmir:hover figcaption > * {
        padding: 1px 10px 1px 10px;
    }

    @media screen and (max-width:1448px){
        #projItem:hover h3{
            font-size: 1.1rem;
        }
    }

    @media screen and (max-width:1350px){
        .other-projects-bgtext h1{
            text-align:center;
            margin-top: 25px;
        }
        .other-projects-wrapper div p{
            font-size: 0.8rem;
        }
    }

    @media screen and (max-width:920px){
        .other-projects-bgtext h1{
            text-align:center;
            font-size: 4.2rem;
        } 
    }

    @media screen and (max-width:680px){
        .other-projects-bgtext h1{
            text-align:center;
            font-size: 2.6rem;
        }  
        .other-projects {
            width:90vw;
            margin:0 auto;
        }
        .project-overlay h3{
            font-size: 2.8vw;
        }
    }

</style>
