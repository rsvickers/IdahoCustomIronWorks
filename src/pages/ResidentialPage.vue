<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <h2 class="mt-4 mb-3 text-center funFont">Check out our Residential Work</h2>
            <div class="col-12 col-md-8 d-flex justify-content-center mt-3">
                <img class="coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" />
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res1.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res2.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res3.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res4.jpg" alt="">
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res5.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res6.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res7.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res8.jpeg" alt="">
            </div>
        </section>

        <section class="row">
            <div class="col-12">
                <Contact />
            </div>
        </section>

    </div>
</template>

<script>

import Contact from '../components/Contact.vue'
import res2 from '../assets/img/res2.jpg'
import res3 from '../assets/img/res3.jpg'
import res5 from '../assets/img/res5.jpg'
import res7 from '../assets/img/res7.jpg'
import res8 from '../assets/img/res8.jpeg'
export default {
    data() {
        return {
            images: [
                { url: res2, caption: 'Image 2' },
                { url: res3, caption: 'Image 2' },
                { url: res5, caption: 'Image 2' },
                { url: res7, caption: 'Image 2' },
                { url: res8, caption: 'Image 2' },

            ],
            currentImageIndex: 0
        };
    },
    computed: {
        currentImage() {
            return this.images[this.currentImageIndex];
        }
    },
    mounted() {
        // Logic to change images every 5 seconds
        setInterval(() => {
            this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
        }, 2000);
    }
};
</script>

<style scoped>
.coolImg {
    height: 65dvh;
    width: 100%;
    object-position: center;
    object-fit: cover;
    box-shadow: 5px 5px 20px black;
}

.smallImg {
    height: 15rem;
    width: 30rem;
    object-position: center;
    object-fit: cover;
    box-shadow: 5px 5px 20px black;
    overflow: hidden
}

.funFont {
    font-family: "Tektur", sans-serif;
    font-weight: 400;
    font-style: normal;
}
</style>