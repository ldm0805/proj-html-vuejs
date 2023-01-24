<template>
    <div class="background_joy">
        <div class="productsCont">
            <h5 class="text-white">Our Products</h5>
            <div class="d-flex">
                <div>
                    <h6>Featured</h6>
                </div>
                <div>
                    <h6>New Arrival</h6>
                </div>
                <div>
                    <h6>Best Sellers</h6>
                </div>
            </div>
        </div>
        <carousel :items-to-show="3" :wrap-around="true">
            <slide v-for="(item, index) in slides" :key="index">
                <img :src="hovered === index ? item.image : item.hoverImage" @mouseover="hovered = index"
                    @mouseleave="hovered = null" />
            </slide>

            <template #addons>
                <navigation />
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
        Navigation,

        Slide,
        Navigation,
    },
    data() {
        return {
            hovered: null,
            slides: [
                {
                    image: '../../public/img/09-327x327.jpg',
                    hoverImage: '../../public/img/11-327x327.jpg',

                },
                {
                    image: '../../public/img/10-327x327.jpg',
                    hoverImage: '../../public/img/11-327x327.jpg',

                },
                {
                    image: '../../public/img/11-327x327.jpg',
                    hoverImage: '../../public/img/12-327x327.jpg',

                },
                {
                    image: '../../public/img/12-327x327.jpg',
                    hoverImage: '../../public/img/13-327x327.jpg',

                },
                {
                    image: '../../public/img/13-327x327.jpg',
                    hoverImage: '../../public/img/14-327x327.jpg',

                },
                {
                    image: '../../public/img/14-327x327.jpg',
                    hoverImage: '../../public/img/15-327x327.jpg',

                },
                {
                    image: '../../public/img/15-327x327.jpg',
                    hoverImage: '../../public/img/16-327x327.jpg',

                },
                {
                    image: '../../public/img/16-327x327.jpg',
                    hoverImage: '../../public/img/17-327x327.jpg',

                },
                {
                    image: '../../public/img/17-327x327.jpg',
                    hoverImage: '../../public/img/18-327x327.jpg',

                },
                {
                    image: '../../public/img/18-327x327.jpg',
                    hoverImage: '../../public/img/17-327x327.jpg',

                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

h6 {
    padding: 1em;
    border: 1px solid white;
    color: white;
}

.productsCont {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1em;

}

button {
    color: yellow;
}
</style>