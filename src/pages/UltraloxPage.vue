<!-- <script setup>
</script>

<template>
    <div class="about">
        <h1>This is the UltraLox page</h1>
    </div>
</template>

<style scoped lang="scss"></style> -->

<!-- <template>
    <div class="gallery">
        <div class="container-fluid">

            <div class="row">
                <h1 class="text-center mt-3">UltraLox Page!</h1>
                <div class="col-md-12 d-flex flex-wrap justify-content-center py-5">
                    <div class="col-md-3 p-3" v-for="(image, index) in images" :key="index">
                        <img class="img-fluid max-height selectable" :src="image.src" :alt="image.alt"
                            @click="enlargeImage(index)" />
                    </div>
                </div>
            </div>
        </div>

        <div v-if="enlargedImageIndex !== -1" class="enlarged" @click="enlargeImage(-1)">
            <img :src="images[enlargedImageIndex].src" :alt="images[enlargedImageIndex].alt" />
        </div>
    </div>

</template>

<script>


export default {
    data() {
        return {
            enlargedImageIndex: -1,
            images: [
                { src: "https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358", alt: "Image 1" },
                { src: "https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/409563652_778889467611248_533411607108688401_n.jpg?stp=cp6_dst-jpg&_nc_cat=105&ccb=1-7&_nc_sid=5f2048&_nc_ohc=fo1fdC3O-nQAb65g4Wp&_nc_ht=scontent-sea1-1.xx&oh=00_AfAKtNEBLK2KqjkRwdXwztDckVx4Pc-AK7wBkHoxs-0qOg&oe=662CA590", alt: "Image 2" },
            ],
        };
    },
    methods: {
        enlargeImage(index) {
            this.enlargedImageIndex = index;
        },
    },

};
</script>

<style scoped lang="scss">
.max-height {
    max-height: 50vh;
    max-width: 50vh;
    height: 50vh;
    width: 100%;
    margin-right: 25px;
    filter: drop-shadow(1rem 1rem 10px rgba(255, 255, 255, 0.23));
    transition: transform 0.3s ease-in-out;
}

.max-height:hover {
    transform: scale(1.1);
}

.enlarged {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.604);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 999;
}

.enlarged img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 15px;
    filter: drop-shadow(0rem 0rem 15px #0a0a0a);

}

.img-fluid {
    border-radius: 15px;
}

.img-fluid:hover {
    margin-right: 25px;
    filter: drop-shadow(1rem 1rem 10px rgba(0, 0, 0, 0.641));
}

.gallery {
    overflow-x: hidden;
    overflow-y: hidden;
}
</style> -->

<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <!-- <h3 class="mt-4 mb-5 text-center">Check out our UltraLox gallery</h3> -->
            <img class="img-fluid ultralox"
                src="https://idahocustomironworks.com/wp-content/uploads/2021/08/UL-Logo-2020-Horizontal-300x59.png"
                alt="UltraLox Interlocking Technology">
            <div class="col-12 d-flex justify-content-center mt-3">
                <img class="img-fluid coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" />
            </div>
        </section>

        <section class="row mt-5 mb-5">
            <div class="col-3 d-flex mt-4">
                <img class="img-fluid smallImg rounded mx-3"
                    src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358"
                    alt="">
                <img class="img-fluid smallImg rounded mx-3"
                    src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358"
                    alt="">
                <img class="img-fluid smallImg rounded mx-3"
                    src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358"
                    alt="">
                <img class="img-fluid smallImg rounded mx-3"
                    src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358"
                    alt="">
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
                { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421277820_805891488244379_5392141397176057853_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=5f2048&_nc_ohc=XvMJlPy6rbUAb7QzFXw&_nc_ht=scontent-sea1-1.xx&oh=00_AfD1xOlvGmhmJFZbRmUwaWlcGPkFbNC4t3lWaA6AwyjThQ&oe=662CB358', caption: 'Image 1' },
                { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421247711_805891481577713_2508292849161234904_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=1uudPkntXJoAb5oVJkL&_nc_ht=scontent-sea1-1.xx&oh=00_AfAWeSRTFC-jvAzdsFBKdCLdLDseiniaHl0Y-O0_CoH9HA&oe=662CAF06', caption: 'Image 2' },
                { url: 'https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/421249062_805891474911047_6568836907381943794_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_ohc=N_11mRCmfhsAb67Qhdl&_nc_ht=scontent-sea1-1.xx&oh=00_AfAWnHJGogpsqyPwJI8iZua4bkULseh1dmqCuHl5c1IMfQ&oe=662C974C', caption: 'Image 3' }
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
        }, 3000);
    }
};
</script>

<style scoped>
/* Add styles if necessary */
.coolImg {
    max-height: 75dvh;
    width: 100dvh;
    box-shadow: 5px 5px 20px black;
}

.smallImg {
    max-height: 35dvh;
    width: 45dvh;
    box-shadow: 5px 5px 20px black;
}

.ultralox {
    max-height: 40dvh;
    width: 55dvh;
}
</style>