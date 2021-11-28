<template>
<div data-aos="fade-up" data-aos-easing="ease" data-aos-duration="500">
    <div class="otherprojectsUi">
        <div data-aos="fade-down" data-aos-easing="ease" data-aos-duration="1000">
            <div class="otherprojectsUi-bgtext">
                <h1> {{titleBigText}} </h1>
            </div>
        </div>

        <div class="otherprojectsUi-wrapper">
            <div v-for="item in projects" :key="item.id" class="otherProjectOverlay">
                <figure class="c4-izmir c4-border-left c4-gradient-top-right c4-image-pan-left" style="--primary-color: #16A085;--secondary-color: #c9df5494; --border-width: 2px;">
            <img :src="item.bgImg" :alt="item.projectName">
            <figcaption class="c4-layout-bottom-left">
                <h3> {{item.projectName}}</h3>
                <p> {{item.projectDesc}} </p>
                    <span class="btn-section" v-if="item.repoL">
                        <button> <a :href="item.repoL"> Repo </a>  </button>
                        <button> <a :href="item.urlSite"> Explore </a> </button>
                    </span>
                        <span class="btn-section" v-else>
                        <button><a :href="item.urlSite" target="_blank"> Explore </a></button>
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
            titleBigText: 'UI | UX',
            hover:false,
            projects:[
                {   
                    id:1, 
                    projectName: 'Cabaret Fest 2021', 
                    projectDesc:'A mockup website for cabaret performers in greater Boston and New England made in Figma.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16921563/media/55d83a0197e3232d1b03d66490f7ec10.png?compress=1&resize=800x600',
                    repoL:null, 
                    urlSite:'https://www.figma.com/file/Qep5i2S1w3oK4v2vD5Mtqq/Website---Providencetowncabaretfest.com?node-id=0%3A1'
                },
                {
                    id:2, 
                    projectName: 'NeighborGoods', 
                    projectDesc:'A mockup for a full-stack website done in teams.  In this project, it is possible to see all the wireframes and prototypes from start to finish.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16921791/media/bc12ada73bfd16702562d0bf4ac771d7.png?compress=1&resize=800x600', 
                    repoL:null, 
                    urlSite:'https://www.figma.com/file/vgGZ6RwBzmplh2vHXgtdee/Small-Business-Hackathon?node-id=127%3A29'
                },
                {   
                    id:3, 
                    projectName: 'Todd Gordon Studio', 
                    projectDesc:'A mockup for a vocal studio website.  I had to re-design the old website by revitalizing it by making it totally responsive.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16921690/media/e2145619c6166c1fb2e28e8bac191a2f.png?compress=1&resize=800x600',
                    repoL:null, 
                    urlSite:'https://www.figma.com/file/j71Zs3uxQtmeOLLse3rite/Todd-website?node-id=0%3A1'
                },
                {
                    id:4, 
                    projectName: 'Travel Lite', 
                    projectDesc:'A mockup website for a company with a passion for hot-air balloons for exploring the world.',
                    display:false, 
                    bgImg: 'https://cdn.dribbble.com/users/5334371/screenshots/16921615/media/6a12d3707ee687af4df180ed3b34cbb5.png?compress=1&resize=800x600', 
                    repoL:null, 
                    urlSite:'https://www.figma.com/file/e6DENgfp4KN3G8xOAihw4n/Website---Ballons'
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

    .otherprojectsUi {
        width:85vw;
        margin:0 auto;
        position: relative;
    }
    .otherprojectsUi-bgtext h1{
        font-family: 'Playfair Display', serif;
        margin-top: 3rem;
        font-size:7.4rem;
        user-select: none;
        text-align: left;
        color: rgba(128, 128, 128, 0.24);
        z-index: 10;
        
    }
    .otherprojectsUi-wrapper{
        display:grid;
        margin-top: 25px;
        grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
        grid-row-gap:    15px;
        grid-column-gap: 15px;
        align-items: center;
        justify-content: space-around;
    }
    .otherprojectsUi-wrapper div{
        min-height: 280px;
    }
    .otherprojectsUi-wrapper div{
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
   
    .otherProjectOverlay h3{
        text-align:center;
        padding-top:15px;
        height:40px;
        font-weight: 400;
    }
    .otherProjectOverlay p{
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
        .otherprojectsUi-bgtext h1{
            text-align:center;
            margin-top: 25px;
        }
        .otherprojectsUi-wrapper div p{
            font-size: 0.8rem;
        }
    }

    @media screen and (max-width:920px){
        .otherprojectsUi-bgtext h1{
            text-align:center;
            font-size: 4.2rem;
        } 
        .btn-section{
            margin-top: 25px;
        }
    }

    @media screen and (max-width:680px){
        .otherprojectsUi-bgtext h1{
            text-align:center;
            font-size: 2.6rem;
        }  
        .otherprojectsUi {
            width:90vw;
            margin:0 auto;
        }
    }

</style>
