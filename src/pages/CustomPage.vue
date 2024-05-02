<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <h2 class="mt-4 mb-3 text-center funFont">Check out our Custom Work</h2>
            <div class="col-12 col-md-8 d-flex justify-content-center mt-3">
                <img class="coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" />
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus1.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus2.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus3.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus4.jpg" alt="">
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus5.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus6.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus7.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/cus8.jpg" alt="">
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
import cus1 from '../assets/img/cus1.jpg'
import cus2 from '../assets/img/cus2.jpg'
import cus3 from '../assets/img/cus3.jpg'
import cus4 from '../assets/img/cus4.jpg'
import cus5 from '../assets/img/cus5.jpg'
import cus6 from '../assets/img/cus6.jpg'
import cus7 from '../assets/img/cus7.jpg'
export default {
    data() {
        return {
            images: [
                { url: cus4, caption: 'Image 4' },
                { url: cus3, caption: 'Image 3' },
                { url: cus1, caption: 'Image 1' },
                { url: cus2, caption: 'Image 2' },
                { url: cus5, caption: 'Image 5' },
                { url: cus6, caption: 'Image 6' },
                { url: cus7, caption: 'Image 7' },
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