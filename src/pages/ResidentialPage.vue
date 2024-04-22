<template>
    <div class="container-fluid">
        <section class="row mt-4 mb-2 justify-content-center">
            <h3 class="mt-4 mb-5 text-center">Check out our Residential Work</h3>
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