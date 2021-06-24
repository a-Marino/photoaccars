<template>
    <div class="slider">
        <div v-for='(imagen, index) in imagenesState' :key='index' :style="`background-image:url(${imagen.imgPath})`" class="slider-content">
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
</style>