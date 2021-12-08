
<template>
<div data-aos="fade-up" data-aos-easing="linear" data-aos-duration="500">

<div class="work-page">
      
    <h2 class="heading-work" id="work">
          | Work | 
    </h2> 

      <div class="grid-work-template">
          <div class="grid-template">
              <div v-for="item in projects" :key="item.id" class="project-overlay">
                <figure class="c4-izmir c4-border-center c4-gradient-top-left" style="--primary-color: #000046; --secondary-color: #1CB5E0; --border-width: 4px;">
                    <img :src="item.projectImg" alt="Sample Image">
                    <figcaption>
                        <div class="description-section">
                            <span class="title-project">{{item.projectName}}</span>
                            <span class="project-info"> {{item.projectDescription}} </span>
                            <span class="btn-projectExplore">
                               <a :href="item.projectExploreLink" target="_blank"> Explore  </a> 
                            </span>
                        </div>         
                    </figcaption>
                    
                </figure>
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
                    projectExploreLink:'https://medium.com/@lennylunderman/what-i-learned-during-an-internship-5f5335c55e6d', 
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
figure{
    font-family: 'Montserrat', sans-serif;
    opacity: 0.8;
}

.description-section{
    display: flex;
    flex-direction: column;
    font-size: 0.8rem;
    margin-top:15px;
    font-family: 'Montserrat', sans-serif;
}
.description-section, .project-info{
    font-family: 'Montserrat', sans-serif;
    font-weight: 200;
    line-height: 1.3em;
}
.btn-projectExplore{
    background-color: rgba(16, 31, 129, 0.8);
    width:5rem;
    margin: 0 auto;
    color: rgb(255, 255, 255);
}
.btn-projectExplore a{
    color: rgb(255, 255, 255);
}

    .work-page{
        width:100%;
        height:100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .grid-work-template{
        padding:15px 0px;
        width: 85vw;
        min-height: 100px;
    }

    .grid-template{
        display:grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        grid-row-gap:    15px;
        grid-column-gap: 15px;
        align-self: center; 
    }

    h2{
        font-size: 3.0rem;
        font-family: 'Montserrat', sans-serif;
        margin-top: 100px;
        margin-bottom: 50px;
    }
    .title-project{
        display: block;
        font-size: 1.2rem;
    }

    @media screen and (max-width:1525px){
        .project-overlay:hover h3 {
            font-size: 8px;
        }
        .project-overlay:hover p{
            font-size: 12px;
        }

        .project-overlay:hover, .btn-section{
            font-size: 16px;
        }
        .title-project{
            font-size: 1.0rem;
        }
    }
    @media screen and (max-width:480px){
        .description-section{
            font-size:0.6rem
        }
    }

</style>





