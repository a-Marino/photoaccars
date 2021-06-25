<template>
    <div class="content">
        <div class="lg">
            <h1 class="logo">photoaccars</h1>
            <div class='about'>
                <h2>Im Andres Marino</h2>
                <h3>I like Photography, Cars and Videogames</h3>
                <router-link to="/images" class="btn-pictures">
                    <img src="@/assets/images/more.svg" alt="more">
                </router-link>
            </div>
            <p class="footer">
                Check out my <a href="https://portfolio-andres-marino.web.app/" target="blank" class="link">Portfolio</a>
            </p>
        </div>
        <div class="sm">
            <h1 class="logo-sm">photoaccars</h1>
            <p>Im Andres Marino</p>
            <p>I like Photography, Cars and Videogames</p>
            <div v-for='(imagen, index) in imagenesState' :key='index' class="div-imagenes-mov">
                <img :src="imagen.imgPath" :alt="imagen.title" class="img-movil">
            </div>
        </div>
    </div>
</template>

<script>
    import {mapState} from 'vuex'

    export default {
        name: 'Index',
        computed: {
            ...mapState('imagenes', ['imagenesState']),
        },
    }
</script>

<style scoped>
    .lg {
        height: 100vh;
        width: 100vw;
        background-image: url('https://steamuserimages-a.akamaihd.net/ugc/1686017249213474176/B92B9BFA9A693661E19B7B5047934C38D6D9B0E5/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.5);
        color: white;
    }

    .logo {
        writing-mode: vertical-lr;
        font-family: 'Bebas Neue', cursive;
        padding: 20px;
    }

    .about {
        margin-top: 50px;
        display: flex;
        flex-direction: column;
        overflow: hidden;
    }

    .about h2 {
        margin-left: 100px;
        font-size: 3.5em;
    }

    .about h3 {
        margin-top: 30px;
        margin-left: 200px;
        font-size: 1.5em;
    }

    .btn-pictures {
        align-self: center;
        margin-top: 50px;
        width: 70px;
        border: none;
        outline: none;
        border-radius: 5px;
        transition: .2s ease-out;
        cursor: pointer;
        
    }

    .btn-pictures:hover {
        transform: scale(1.1);
    }

    .footer {
        position: absolute;
        bottom: 0;
        right: 0;
        margin: 10px;
    }

    .link {
        text-decoration: none;
        color: white;
        font-weight: bold;
        font-size: 1.3em;
    }

    .sm {
        display: none;
    }

    .logo-sm {
        font-family: 'Bebas Neue', cursive;
        padding: 5px;
    }

    .img-movil {
        width: 350px;
        height: auto;
        margin-top: 15px;
    }

    .div-imagenes-mov {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    @media (max-width: 640px) { 
        .lg {
            display: none;
        }

        p {
            font-weight: 600;
            padding-left: 5px;
        }

        .sm {
            display: inline;
            height: 100vh;
            width: 100vw;
            color: white;
        }
    }
</style>