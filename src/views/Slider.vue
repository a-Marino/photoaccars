<template>
    <div class="slider">
        <router-link to="/" class="back"><img src="@/assets/images/back.svg" alt="back"></router-link>
        <div v-for='(imagen, index) in imagenesState' :key='index' :style="`background-image:url(${imagen.imgPath})`" class="slider-content">
            <div class="img-nav">
                <h3>{{imagen.title}}</h3>
            </div>
        </div>
    </div>
</template>

<script>
import {mapState} from 'vuex'

export default {
    name: 'Slider',
    computed: {
        ...mapState('imagenes', ['imagenesState']),
    },
}
</script>

<style scoped>
    .slider {
        height: 100vh;
    }
    
    .slider-content{
        height: 100vh;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
    }

    .img-nav {
        background-color: rgba(0, 0, 0, 0.39);
        color: white;
        height: 50px;
        text-align: center;
        line-height: 50px;
    }

    .back {
        position: fixed;
        right: 0;
        margin-right: 25px;
        margin-top: 10px;
        color: white;
        text-decoration: none;
        font-weight: bold;
        font-size: 1em;
        cursor: pointer;
        width: 2em;
        transition: .2s ease-out;
    }

    .back:hover {
        transform: scale(1.2);
    }
</style>