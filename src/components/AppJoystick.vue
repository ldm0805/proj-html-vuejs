<template>
    <carousel :items-to-show="1.5">
        <slide v-for="(item, index) in slides" :key="index">
            <img v-bind:src="slides[index].image" />
        </slide>

        <template #addons>
            <navigation />
            <pagination />
        </template>
    </carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
    name: 'App',
    components: {
        Carousel,


        Slide,
        Pagination,
        Navigation,
    },
    data() {
        return {
            slides: [
                {
                    image: '../../public/img/09-608x608.jpg',
                },
                {
                    image: '../../public/img/10-608x608.jpg',
                },
                {
                    image: '../../public/img/11-608x608.jpg',
                },
                {
                    image: '../../public/img/12-608x608.jpg',
                },
                {
                    image: '../../public/img/13-608x608.jpg',
                },
                {
                    image: '../../public/img/14-608x608.jpg',
                },
                {
                    image: '../../public/img/15-608x608.jpg',
                },
                {
                    image: '../../public/img/16-608x608.jpg',
                },
                {
                    image: '../../public/img/17-608x608.jpg',
                },
                {
                    image: '../../public/img/18-608x608.jpg',
                },
            ],
        }
    }
}
</script>
