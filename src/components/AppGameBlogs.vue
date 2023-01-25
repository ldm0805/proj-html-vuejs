<template>
    <div class="background_joy">

        <carousel :items-to-show="3" :wrap-around="true">
            <slide v-for="(item, index) in slides" :key="index">
                <div class="d-flex flex-column g-5">
                    <div class="img-cont">
                        <img :src="item.image" />
                    </div>
                    <div class="description text-white">
                        <h5 class="py-3">
                            <i class="fa-regular fa-calendar-days"></i>
                            {{ item.dategame }}
                            <i class="fa-regular fa-comments"></i>
                            {{ item.comment }}
                        </h5>
                        <p>{{ item.description }}</p>
                    </div>
                </div>
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
        Slide,
        Navigation,
    },
    data() {
        return {
            slides: [
                {
                    image: '../../public/img/Consequunt-magni-dolores.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'Jan 18,2021',
                    comment: '0 Comment'
                },
                {
                    image: '../../public/img/Et-quasi-architecto-beate.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Laborum-et-dolor-fuga-Et.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Rerum-facilis-est-et-exped.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'
                },
                {
                    image: '../../public/img/Omnis-iste-natus-error-sit.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Nisi-ut-aliquid-ex-ea-com.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Illo-inventore-veritatis-quasi.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Architecto-beatae-vitae-dicta.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/At-vero-eos-et-accusamus.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
                {
                    image: '../../public/img/Blandit-praesen-volupta.jpg',
                    description: '"Post Format: Chat, Lorem Ipsum is simply text"',
                    dategame: 'May 30,2021',
                    comment: '0 Comment'

                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


.img-cont {
    width: 400px;

    img {
        width: 100%;
    }
}

i {
    padding: 0px 10px;
    color: $yellow;
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