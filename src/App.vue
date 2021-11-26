<template>

    <Navigation/>
    <Landing/>
    <WorkSection/>
    
    <!--<AboutMe/>
    <SocialSkills/>
    <WebProjects/>
    <ContactMeBar/>
    <UiUxProjects/>
    <Footer/> -->

</template>

<script>

import Navigation from './components/Navigation.vue'
import Landing from './components/Landing.vue'
import WorkSection from './components/WorkSection.vue'
import AboutMe from './components/AboutMe.vue'
import SocialSkills from './components/SocialSkills.vue'
import WebProjects from './components/WebProjects.vue'
import ContactMeBar from './components/ContactMeBar.vue'
import UiUxProjects from './components/UiUxProjects.vue'
import Footer from './components/Footer.vue'

// site done


export default {
  name: 'App',
  components: {
    Navigation, Landing, WorkSection, AboutMe, SocialSkills, WebProjects, ContactMeBar, UiUxProjects, Footer, 
  },
}
</script>

<style>

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

/* Queries for the website  */ 
@media screen and (max-width: 480px) {
  li, a, button{
    font-size: 80%;
    font-weight: bold;
  }
  .nav__links li a:hover {
    color: rgb(0, 0, 0);
    font-weight: 400;
    border-inline: 2px solid rgb(0, 0, 0);
    padding: 0.5em
  }
  header{
    padding: 30px 5%;
  }

  h2{
    font-size: 1.6rem;
  } 

}

</style>
