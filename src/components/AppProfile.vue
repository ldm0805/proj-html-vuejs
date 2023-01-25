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
                <Pagination />
            </template>
        </carousel>
    </div>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination } from 'vue3-carousel'

export default {
    name: 'App',
    components: {
        Carousel,

        Pagination,

        Slide,
        Navigation,
    },
    data() {
        return {
            slides: [
                {
                    image: '../../public/img/t2-1-100x100_left.jpg',
                    description: '"There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, There are many variations of passages of Lorem Ipsum available"',
                    nameprof: 'Luies Charls',
                    profession: '(Web Designer)'
                },
                {
                    image: '../../public/img/t4-1-100x100_left.jpg',
                    description: '"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting"',
                    nameprof: 'Din Desuza',
                    profession: '(Iphone Developer)'

                },
                {
                    image: '../../public/img/t5-1-100x100_left.jpg',
                    description: '"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting"',
                    nameprof: 'Reema Ghurde',
                    profession: '(Senion Menager)',

                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

span {
    color: $yellow;
}

img {
    border-radius: 100%;
    border: 2px solid $yellow;
}

.description {
    color: white;
    padding: 1em 10em;
}

.img-cont {
    position: relative;

    &:after {
        content: "";
        background: #f9aa01 url(../../public/img/quote.png) no-repeat scroll center 8px;
        width: 28px;
        height: 28px;
        border-radius: 100%;
        position: absolute;
        top: 2px;
        left: 700px;
        display: inline-block;
        margin-left: -14px;
    }

}



h6 {
    padding: 1em;
    border: 1px solid white;
    color: white;
}

.background_joy {
    padding: 3em 0em;
    height: 500px;
    background-image: url('../../public/img/parallax.jpg');
}

button {
    color: yellow;
}

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