
<template>
<div data-aos="fade-up" data-aos-easing="linear" data-aos-duration="500">

<div class="work-page">
      
    <h2 class="heading-work" id="work">
          | Work | 
    </h2> 

      <div class="grid-work-template">
          <div class="grid-template">
              
                    <div class="grid-item" v-for="workItem in projects" :key="workItem.projectId" :style="'background-image: url('+workItem.projectImg+')'">
                        
                        <h2 class="project-naame">
                            {{workItem.projectName}}
                        </h2>
                        <p class="description-project">
                            {{workItem.projectDescription}}
                        </p>
                        <div class="project__links">
                            <!-- <a :href="workItem.projectRepoLink" class="link-project"> <button> Repo </button> </a> -->
                            <a :href="workItem.projectExploreLink" target="_blank" class="link-project"> <button> Explore </button> </a>
                        </div>
                        
                    </div>             
          </div>

      </div>

  </div>

</div>

  

</template>


<script>
import SequentialEntrance from 'vue-sequential-entrance'
import 'vue-sequential-entrance/vue-sequential-entrance.css'


export default {
    data(){
        return {
            projects:[
                {
                    projectId:1, 
                    projectName:'Center Centre - UIE', 
                    projectDescription:"Web Developer | Email Specialist. I helped to develop email marketing for 30.000 UX designers and worked closely with Jared Spool. I've developed new features for the company website and helped with the hiring process of the latest web developer intern.", 
                    projectRepoLink:'#', 
                    projectExploreLink:'https://www.uie.com/', 
                    projectDisplay:false, 
                    // projectImg:"https://cdn.dribbble.com/users/5358639/screenshots/15260952/media/043b78563d0e928c0fd871403253698b.png?compress=1&resize=1200x900" 
                    projectImg:"https://cdn.dribbble.com/users/988698/screenshots/3423782/develop_isometric_perspective.jpg?compress=1&resize=800x600",
                },
                {
                    projectId:2, 
                    projectName:'Twentieth Century Boston', 
                    projectDescription:"WordPress Developer | I created the e-commerce website for the Jewelry Company in Boston. I also managed all the online business and maintenance of the site. I generated reports and sent email marketing with promotions and sales on the website.", 
                    projectRepoLink:'https://www.w3.org', 
                    projectExploreLink:'https://boston-vintagejewelry.com/', 
                    projectDisplay:false, 
                    projectImg:"https://www.sketchappsources.com/resources/source-image/3d-dash-illustration-sumit_choudhary.png" 
                },
                {
                    projectId:3, 
                    projectName:'General Assembly Fellowship', 
                    projectDescription:"Full-time 500+ hours immersive program where I designed and implemented multiple full-stack applications using MVC framework and OOP.  I built quality RESTful APIs, integrating data from third-party APIs, and worked closely with the development team.", 
                    projectRepoLink:'', 
                    projectExploreLink:'https://generalassemb.ly/education/software-engineering-immersive/boston', 
                    projectDisplay:false, 
                    // projectImg:"https://cdn.dribbble.com/users/2319164/screenshots/15425940/001_desktop_set.png" 
                    projectImg:"https://cdn.dribbble.com/users/918057/screenshots/5303882/media/73b32d2565dd6f6d94a44a02407d6d84.png?compress=1&resize=800x600"  
                },    
            ]
        }
    }

}
</script>

<style>
    .work-page{
        width:100%;
        height:100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .grid-work-template{
        padding:15px 0px
    }

    .grid-template{
        display:grid;
        grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
        grid-row-gap:    15px;
        grid-column-gap: 15px;
        width:85vw;
        grid-auto-rows: 280px;
    }

    .grid-item{
        display:flex;
        flex-direction: column;
        background-color:pink;
        justify-content:center;
        align-items:center;
        text-align:center;
        background-position: center;
        background-repeat: no-repeat;
        background-size: 100%;
        font-family: 'Montserrat', sans-serif;
        background-color:rgba(255, 255, 255, 0.601);
        opacity:0.85;
        background-size: 100%;
        object-fit: cover;
    }

/* background-position: center;
        background-repeat: no-repeat;
        background-position: center;
        background-repeat: no-repeat; 
        object-fit: contain;
        background-size: cover;
        .fill {object-fit: fill;}
.contain {object-fit: contain;}
.cover {object-fit: cover;}
.scale-down {object-fit: scale-down;}
.none {object-fit: none;}*/

    .grid-item h2{
        font-size: 1.8rem;
        opacity: 0.8;
        margin-top:0px;   
    }

    .grid-item p{
        padding: 5px 0px;
        width: 90%;
        opacity: 0.9;
        font-size: 0.9rem;
        color: rgba(0, 0, 0, 1);
        margin-top:-25px;
        font-weight: 400;
        
    }

    .grid-item:hover{
        cursor: pointer;
    }


    .project__links{
        margin-top:15px;
    }
    .project__links button{
        color :white;
        background-color:black;
        opacity: 0.8;
    }
    .project__links button:hover{
        opacity: 1;
    }
 
    h2{
        font-size: 3.0rem;
        font-family: 'Montserrat', sans-serif;
        margin-top: 100px;
        margin-bottom: 50px;
    }
   
    @media screen and (max-width:480px) {
        .grid-item h2{
        padding-top: 25px;
        font-size: 1.4rem;
        opacity: 0.8;
        margin-top: 0px;
        }
        .grid-item p{
        padding: 0px 0px;
        width: 90%;
        opacity: 1;
        font-size: 0.7rem;
        color: rgba(0, 0, 0, 1);
        margin-top: -50px;
        }
        .grid-item{
            width: 90%;
        }
    }


</style>




