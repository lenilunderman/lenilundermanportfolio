<template>
    <div class="galleryView">

        <div class="galleryView-wrapper">
            <div v-for="item in projects" :key="item.id" class="galleryOverlay">
                <figure class="c4-izmir c4-border-center c4-gradient-top-left" style="--primary-color: #000046; --secondary-color: #1CB5E0; --border-width: 5px;">
            <img :src="item.bgImg" :alt="item.projectName">
            <figcaption>
                <h3> {{item.projectName}}</h3>
                <p> {{item.projectDesc}} </p>
                    <span class="btn-section" v-if="item.repoL">
                        <button> <a :href="item.repoL"> Repo </a>  </button>
                        <button> <a :href="item.urlSite"> Explore </a> </button>
                    </span>
                        <span class="btn-section" v-else>
                        <button><a href="item.urlSite" target="_blank"> Explore </a></button>
                    </span>
            </figcaption>
            </figure>
            </div>
        </div>
        
    </div> 
</template>

<script>
export default {

    data(){
        return{
            titleBigText: 'UI | UX',
            hover:false,
            projects:[
                {
                    id:1, 
                    projectName: 'item1', 
                    projectDesc:'lorem lor sit amet consectetur adipisicirem lor sit consectetur adipisicing elit. Molestia rem lor sit amet consectetur adipisicing elit. Molestia',
                    display:false, 
                    bgImg: 'https://s.abcnews.com/images/Business/GTY_rabbit_sr_140508_16x9_992.jpg', 
                    repoL:'https://www.google.com1/', 
                    urlSite:'https://www.google.com/'
                },
                {   
                    id:2, 
                    projectName: 'item2', 
                    projectDesc:'Sit  damtrd amet consectetur adipisicing elit. Molestiae, atrem ipsum',
                    display:false, 
                    bgImg: 'https://images.unsplash.com/photo-1496821623243-68126e428f31?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80',
                    repoL:null, 
                    urlSite:'https://www.google.com/'
                },
                {
                    id:3, 
                    projectName: 'item3', 
                    projectDesc:'Daerorem lor sit amet consectetur adipisicing elit. Dtsiae, at. gorem ipsum',
                    display:false, 
                    bgImg: 'https://images.unsplash.com/photo-1518796745738-41048802f99a?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8cmFiYml0fGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80', 
                    repoL:null, 
                    urlSite:'https://www.google.com/'
                },
                {   
                    id:4, 
                    projectName: 'item2', 
                    projectDesc:'Gardvrem lor sit amet consectetur adipisicing elit. Dtsiae, at. trorem dagnum',
                    display:false, 
                    bgImg: 'https://i.insider.com/5bf43911110d4c1bb210b93c?width=700&format=jpeg&auto=webp',
                    repoL:null, 
                    urlSite:'https://www.google.com/'
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
    @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Serif&family=Montserrat:wght@300;500;700&family=Playfair+Display:ital,wght@0,400;0,600;1,700&display=swap');
    /* Style for the gallery of the website  */
    @import '../assets/styles/gallery.css';

    .galleryView {
        width:85vw;
        margin:0 auto;
        position: relative;
    }
    .galleryView-bgtext h1{
        font-family: 'Playfair Display', serif;
        margin-top: 3rem;
        font-size:7.4rem;
        user-select: none;
        text-align: left;
        color: rgba(197, 194, 194, 0.396);
        z-index: 10;
        
    }
    .galleryView-wrapper{
        display:grid;
        margin-top: 25px;
        grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
        grid-row-gap:    15px;
        grid-column-gap: 15px;
        align-items: center;
        justify-content: space-around;
    }
    /* .galleryView-wrapper div{
        min-height: 280px;
    } */
    .galleryView-wrapper div{
        min-height: 280px;
        background-color:rgb(170 182 201 / 35%);
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
   
    .galleryOverlay h3{
        text-align:center;
        padding-top:15px;
        height:40px;
        font-weight: 400;
    }
    .galleryOverlay p{
        width: 95%;
        text-align:center;
        text-align:center;
        margin: 0 auto;
        font-size: 0.9rem;
        padding-top: 20px;
    }

    .btn-section{
        width: 100%;
        display: inline-block;
        margin: 0 auto;
        text-align: center;
        margin-top: 25px;
    }

    .btn-section a{
        color: white;
    }

    @media screen and (max-width:1350px){
        .galleryView-bgtext h1{
            text-align:center;
            margin-top: 25px;
        }
        .galleryView-wrapper div p{
            font-size: 0.8rem;
        }
    }

    @media screen and (max-width:920px){
        .galleryView-bgtext h1{
            text-align:center;
            font-size: 4.2rem;
        } 
        .btn-section{
            margin-top: 25px;
        }
    }

    @media screen and (max-width:680px){
        .galleryView-bgtext h1{
            text-align:center;
            font-size: 2.6rem;
        }  
        .galleryView {
            width:90vw;
            margin:0 auto;
        }
    }

</style>
