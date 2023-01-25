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
                    star: 8,
                    namejoy: 'Buddy and Lucky Solitaire',
                    price: '83-90'

                },
                {
                    image: '../../public/img/10-327x327.jpg',
                    hoverImage: '../../public/img/11-327x327.jpg',
                    star: 8,
                    namejoy: 'Taishou x Alice Epilogue',
                    price: '83-90'

                },
                {
                    image: '../../public/img/11-327x327.jpg',
                    hoverImage: '../../public/img/12-327x327.jpg',
                    star: 8,
                    namejoy: 'Labyrinths of the World',
                    price: '83-90'

                },
                {
                    image: '../../public/img/12-327x327.jpg',
                    hoverImage: '../../public/img/13-327x327.jpg',
                    star: 8,
                    namejoy: 'Reginald\'s  Death Arena',
                    price: '83-90'

                },
                {
                    image: '../../public/img/13-327x327.jpg',
                    hoverImage: '../../public/img/14-327x327.jpg',
                    star: 8,
                    namejoy: 'Martin Goes on the Attack',
                    price: '£77'

                },
                {
                    image: '../../public/img/14-327x327.jpg',
                    hoverImage: '../../public/img/15-327x327.jpg',
                    star: 8,
                    namejoy: 'What\'s in the Window',
                    price: '£15'

                },
                {
                    image: '../../public/img/15-327x327.jpg',
                    hoverImage: '../../public/img/16-327x327.jpg',
                    star: 8,
                    namejoy: 'Lengend of Mana Remastered',
                    price: '83-90'

                },
                {
                    image: '../../public/img/16-327x327.jpg',
                    hoverImage: '../../public/img/17-327x327.jpg',
                    star: 8,
                    namejoy: 'Babol the Waling Box',
                    price: '83-90'

                },
                {
                    image: '../../public/img/17-327x327.jpg',
                    hoverImage: '../../public/img/18-327x327.jpg',
                    star: 8,
                    namejoy: 'Adam The Storyteller',
                    price: '£75'

                },
                {
                    image: '../../public/img/18-327x327.jpg',
                    hoverImage: '../../public/img/17-327x327.jpg',
                    star: 8,
                    namejoy: 'The little Tank Hunter',
                    price: '£83'

                },
            ],
        }
    },
    methods: {
        filledStars() {
            let starFull = Math.round(this.slides.star / 2);
            let starsFilledArr = [];
            for (let i = 0; i < starFull; i++) {
                starsFilledArr.push('fa-solid fa-star');
            }
            //Implementazione stelle vuote
            let starEmpty = 5 - starFull;
            for (let i = 0; i < starEmpty; i++) {
                starsFilledArr.push('fa-regular fa-star');
            }
            return starsFilledArr
        },
    },
}
</script>
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
        <carousel :items-to-show="4" :wrap-around="true">
            <slide v-for="(item, index) in slides" :key="index">
                <div class="card_">
                    <img :src="hovered === index ? item.image : item.hoverImage" @mouseover="hovered = index"
                        @mouseleave="hovered = null" />
                    <i v-for="(value, index) in filledStars()" :key="index" :class="value"></i>
                    <h5>{{ item.namejoy }}</h5>
                    <p>{{ item.price }}</p>
                </div>
            </slide>

            <template #addons>
                <navigation />
            </template>
        </carousel>
    </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

h6 {
    padding: 1em;
    border: 1px solid white;
    color: white;
}

.card_ {

    h5 {
        @include upbold;
        color: white;

        &:hover {
            color: $yellow;
        }
    }

    p {
        color: white;
    }
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