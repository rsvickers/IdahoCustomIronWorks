<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <!-- <h3 class="mt-4 mb-5 text-center">Check out our UltraLox gallery</h3> -->
            <div class="col-12 d-flex justify-content-center mb-3">
                <img class="img-fluid ultralox"
                    src="https://idahocustomironworks.com/wp-content/uploads/2021/08/UL-Logo-2020-Horizontal-300x59.png"
                    alt="UltraLox Interlocking Technology">
            </div>
            <div class="col-12 col-md-8 d-flex justify-content-center mt-3">
                <img class="coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" />
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul8.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul7.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul6.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul1.jpg" alt="">
            </div>
        </section>

        <section class="row mt-5 mx-3 mb-3">
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul2.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul3.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul4.jpg" alt="">
            </div>
            <div class="col-md-3 col-12 d-flex mt-4 img-fluid">
                <img class="smallImg rounded mx-3" src="/src/assets/img/ul5.jpg" alt="">
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

import ul1 from '../assets/img/ul1.jpg'
import ul2 from '../assets/img/ul2.jpg'
import ul3 from '../assets/img/ul3.jpg'
import ul4 from '../assets/img/ul4.jpg'
import ul5 from '../assets/img/ul5.jpg'
export default {
    data() {
        return {
            images: [
                // { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358', caption: 'Image 1' },
                // { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421247711_805891481577713_2508292849161234904_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=1uudPkntXJoAb5oVJkL&_nc_ht=scontent-sea1-1.xx&oh=00_AfAWeSRTFC-jvAzdsFBKdCLdLDseiniaHl0Y-O0_CoH9HA&oe=662CAF06', caption: 'Image 2' },
                // { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421249062_805891474911047_6568836907381943794_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_ohc=N_11mRCmfhsAb67Qhdl&_nc_ht=scontent-sea1-1.xx&oh=00_AfAWnHJGogpsqyPwJI8iZua4bkULseh1dmqCuHl5c1IMfQ&oe=662C974C', caption: 'Image 3' },
                { url: ul3, caption: 'Image 4' },
                { url: ul4, caption: 'Image 4' },
                { url: ul5, caption: 'Image 4' },
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
    height: 15em;
    width: 30em;
    object-position: center;
    object-fit: cover;
    box-shadow: 5px 5px 20px black;
    overflow: hidden
}

.ultralox {
    max-height: 40dvh;
    width: 55dvh;
}
</style>