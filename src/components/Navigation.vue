<template>
    <div data-aos="fade-down" data-aos-easing="linear" data-aos-duration="400">
        <header>
            <div class="logo animate__animated animate__hinge animate__delay-2s animate__slower"> Portfolio </div>
                <nav>
                    <ul class="nav__links">
                        <li v-for="menuItem in menuLinks" :key="menuItem">
                            <a :href="menuItem.linktag"> {{menuItem.nameLink}} </a>
                        </li>
                    </ul>  
                </nav>
                <!-- <a href="#" class="cta"> <button>Contact me </button></a> -->
        </header>
    </div>
</template>

<script>
export default {
    data(){
        return{
            menuLinks: [
                {nameLink:'Work', linktag:'#work'},
                {nameLink:'About Me', linktag:'#aboutme'},
                {nameLink:'Services', linktag:'#services'},
            ]
        }
    }
}
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;500;700&display=swap');

    li, a, button {
        font-family: 'Montserrat', sans-serif;
        font-weight: 300;
        font-size:14px;
        color: black;
        text-decoration: none;
    }

    header{
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding: 30px 10%;
        margin-top:5vh;
    }

    .logo{
        font-family: 'Montserrat', sans-serif;
        cursor: pointer;
        margin-right: auto;
        font-weight: 700;
    }

    .nav__links{
        list-style: none;
    }

    .nav__links li {
        display: inline-block;
        padding: 0px 20px;
    }

    .nav__links li a {
        transition: all 0.4s ease 0s;
    }

    .nav__links li a:hover {
        color: rgb(0, 0, 0);
        font-weight: 400;
        border-inline: 2px solid rgb(0, 0, 0);
        padding: 0.5em;
        transition: all 0.4s ease 0s;
    }

    /* Queries for the website  */ 
    @media screen and (max-width: 465px) {
        header{
           justify-content: center;
           font-size: 1.2rem;
        }
        .logo{
            display: none;
        }
    }

</style>