<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <h2 class="mt-4 mb-3 text-center funFont">Check out our Residential Work</h2>
            <div class="col-12 d-flex justify-content-center mt-3">
                <img class="coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" />
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res1.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res2.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res3.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res4.jpg" alt="">
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res5.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res6.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/res7.jpg" alt="">
            </div>
            <div class="col-3 d-flex mt-4 img-fluid">
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
export default {
    data() {
        return {
            images: [
                // { url: '/src/assets/img/res1.jpg', caption: 'Image 1' },
                { url: '/src/assets/img/res2.jpg', caption: 'Image 2' },
                { url: '/src/assets/img/res3.jpg', caption: 'Image 3' },
                { url: '/src/assets/img/res5.jpg', caption: 'Image 4' },
                // { url: '/src/assets/img/res6.jpg', caption: 'Image 5' },
                { url: '/src/assets/img/res7.jpg', caption: 'Image 6' },
                { url: '/src/assets/img/res8.jpeg', caption: 'Image 6' },
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
    width: 100dvh;
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