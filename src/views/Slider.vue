<template>
    <div class="slider">
        <div v-for='(imagen, index) in imagenesState' :key='index' :style="`background-image:url(${imagen.imgPath})`" class="slider-content">
            <div class="img-nav">
                <router-link to="/" class="back">Back</router-link>
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
    }
}
</script>

<style scoped>
    .slider {
        height: 100vh;
        scroll-snap-type: y mandatory;
        overflow-y: scroll;
    }

    .slider-content{
        height: 100vh;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        scroll-snap-align: center;
    }

    .img-nav {
        background-color: rgba(0, 0, 0, 0.39);
        color: white;
        height: 50px;
        text-align: center;
        line-height: 50px;
    }

    .back {
        float: left;
        margin-left: 10px;
        color: white;
        text-decoration: none;
        font-weight: bold;
        font-size: 1em;
        cursor: pointer;
    }
</style>