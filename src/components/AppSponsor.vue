<template>
    <div class="background_joy">

        <carousel :items-to-show="1" :wrap-around="true">
            <slide v-for="(item, index) in slides" :key="index">
                <div class="d-flex flex-column g-5">
                    <div class="img-cont">
                        <img :src="item.image" />
                    </div>
                    <div class="description">
                        <h5 class="py-3">{{ item.nameprof }} <span>{{ item.profession }}</span></h5>
                        <p>{{ item.description }}</p>
                    </div>
                </div>
            </slide>
            <template #addons>
                <Navigation />
            </template>
        </carousel>
    </div>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'

export default {
    name: 'App',
    components: {
        Carousel,

        Slide,
        Navigation,
    },
    data() {
        return {
            slides: [
                {
                    image: '../../public/img/brand-01.png',
                },
                {
                    image: '../../public/img/brand-02.png',
                },
                {
                    image: '../../public/img/brand-03.png',
                },
                {
                    image: '../../public/img/brand-04.png',
                },
                {
                    image: '../../public/img/brand-05.png',
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;



.carousel__item {
    min-height: 200px;
    width: 100%;
    background-color: var(--vc-clr-primary);
    color: var(--vc-clr-white);
    font-size: 20px;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.carousel__slide {
    padding: 20px;
}

.carousel__pagination-button {
    display: block;
    border: 0;
    margin: 0;
    cursor: pointer;
    /* padding: var(--vc-pgn-margin); */
    padding: 0.5em !important;
    background: yellow !important;
}
</style>