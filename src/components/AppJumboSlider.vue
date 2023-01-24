<script>
export default {
    data() {
        return {
            autoplay: null,
            activeImage: 0,
            slides: [
                {
                    image: 'img/01.webp',
                    title: 'Marvel\'s Spiderman Miles Morale',
                    text: 'Experience the rise of Miles Morales as the new hero masters incredible, explosive new powers to become his own Spider-Man.',
                },
                {
                    image: 'img/02.webp',
                    title: 'Ratchet & Clank: Rift Apart',
                    text: 'Go dimension-hopping with Ratchet and Clank as they take on an evil emperor from another reality.',
                },
            ],
        }
    },
    created() {
        //L'autoplay si avvia all'apertura della pagina
        this.startAutoplay();
    },

    methods: {
        // Click sulle thumbs
        changeImage(currentIndex) {
            this.activeImage = currentIndex;
        },
        // Click sulle frecce
        next() {
            this.activeImage++;
            if (this.activeImage > this.slides.length - 1) {
                this.activeImage = 0;
            }
        },
        prev() {
            this.activeImage--;
            if (this.activeImage < 0) {
                this.activeImage = this.slides.length - 1;
            }
        },
        // Autoplay
        startAutoplay() {
            this.autoplay = setInterval(() => {
                this.next()
            }, 3000)
        },
        stopAutoplay() {
            clearInterval(this.autoplay);
            this.autoplay = null;
        }
    }
}
</script>
<template lang="">
    <div class="cont-all d-flex flex-column g-2">
        <div id="app">
            <!-- Container -->
            <div class="container mt-2">
                    <div class="item">
                        <!-- Effetto del mouse over e leave -->
                        <div class="image" @mouseover="stopAutoplay" @mouseleave="startAutoplay">
                        <!-- Immagini in slides -->
                        <img v-bind:src="slides[activeImage].image" v-bind:alt="slides[activeImage].title">
                        </div>
                        <!-- Titoli e testi sull'immagine -->
                        <div class="text">
                            <h2>{{slides[activeImage].title}} </h2>
                            <p>{{slides[activeImage].text}}</p>
                        </div>
                    </div>
                    <!-- Creo la thumbs -->
                    <div class="thumbs" >
                        <!-- Click sulle frecce -->
                        <div class="prev" @click="prev"></div>
                        <div class="next" @click="next"></div>
                        <!-- Controllo sulle thumbs per inserire la classe active -->
                        <div class="thumb" v-for="(thumb, index) in slides" :class="(activeImage === index) ? 'active' : '' ">
                            <!-- Click sulle thumbs -->
                            <img v-bind:src="thumb.image" v-bind:alt="thumb.title" @click="changeImage(index)"/>
                        </div>
                    </div>
            </div>
                    <!-- Bottoni play e pausa -->
                    <div class="buttons">
                        <button class="btn btn-play" @click="startAutoplay"><i class="fas fa-play"></i></button>
                        <button class="btn btn-pause" @click="stopAutoplay"><i class="fas fa-pause"></i></button>
                    </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.image {
    height: 100%;
}

.item {
    float: left;
    width: 700px;
    height: 300px;
    position: relative;
}

.item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.item .text {
    position: absolute;
    right: 20px;
    bottom: 20px;
    text-align: right;
    color: white;
}

.thumbs {
    float: left;
    height: 300px;
    width: 180px;
    background: #000;
    position: relative;
}

.thumb {
    height: calc((300px) / 5);
    opacity: 0.5;
}

.thumb img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.thumb.active {
    outline: 2px solid #ccc;
    opacity: 1;
}

.prev,
.next {
    width: 20px;
    height: 20px;
    margin: 10px 0;
    border-radius: 50%;
    background: #ccc;
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    cursor: pointer;
    z-index: 999;
}

.next {
    bottom: 0;
}

/*
EXTRA: in questo esempio gli accordion vengono creati
usando 2 bordi di un quadratino ruotato di 45 gradi
In una versione base si possono usare delle icone
oppure i caratteri ∧ (&and;) e ∨ (&or;)
 */
.prev::after {
    content: '';
    width: 10px;
    height: 10px;
    border-top: 1px solid black;
    border-right: 1px solid black;
    display: block;
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%) rotate(-45deg);
}

.next::before {
    content: '';
    width: 10px;
    height: 10px;
    border-top: 1px solid black;
    border-right: 1px solid black;
    display: block;
    position: absolute;
    bottom: 35%;
    left: 50%;
    transform: translate(-50%) rotate(135deg);
}

.buttons {
    display: flex;
    justify-content: center;
}

.cont-all {
    height: 100vh;
    background: linear-gradient(#121212, #0a2744, #30475E);
}

.btn {
    padding: 20px 50px;
    margin: 20px;
    border: none;
    border-radius: 50px;
}

.btn-play {
    background-color: rgb(3, 106, 190);
}

.btn-pause {
    background-color: yellow;

}

.btn-play:hover {
    outline: 2px solid white;
    background-color: rgb(1, 53, 95);
}

.btn-pause:hover {
    outline: 2px solid white;
    background-color: rgb(145, 145, 1);
}
</style>