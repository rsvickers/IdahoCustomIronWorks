<template>
  <div class="container-fluid funFont">
    <section class="row heroImg box" :style="{ 'background-image': 'url(' + currentImage + ')' }">
      <div class="col-12 text-light px-0 text-center text-shadow d-flex justify-content-center">
        <div class="p-4 p-md-5 box">
          <h1 class="">Idaho Custom Iron Works</h1>
          <h6>We're not just any fabrication company; we specialize in crafting custom ironworks tailored to our
            clients'
            unique visions. Idaho Custom Iron Works combines over 15 years of experience with our dedication to
            exceeding
            expectations. As a locally owned and family-operated business licensed in both Idaho and Oregon, we take
            pride
            in delivering exceptional results in both commercial and residential projects. Your imagination is our
            blueprint, and we're here to turn your ideas into stunning realities.</h6>
        </div>
      </div>
    </section>

    <section class="row mt-5 mb-2 px-4 align-items-center">
      <div class="col-12 col-md-7 text-center">
        <img class="img-fluid"
          src="https://idahocustomironworks.com/wp-content/uploads/2021/08/UL-Logo-2020-Horizontal-300x59.png"
          alt="UltraLox Interlocking Technology">
        <p class="mt-3">Almost two decades of commercial and residential custom iron works. The Treasure Valley has a
          new technology now available called ULTRALOX INTERLOCKING® TECHNOLOGY, premium powder-coated aluminum picket
          and glass railing systems for decks, patios and swimming pools with low-maintenance living in mind. Our
          dedication to research and development ensures a uniquely engineered railing system that meets
          commercial/residential building codes throughout the US.</p>
        <p class="mt-4">ULTRALOX INTERLOCKING® TECHNOLOGY high-performance railings are made of durable aluminum with a
          long-lasting powder-coated finish to stay looking like new. We back that up with a 20-year limited warranty.
          We guarantee that your glass and aluminum railing system will continue looking great for years to come.</p>
        <p class="mt-4">Additionally, ULTRALOX INTERLOCKING® TECHNOLOGY strives to respect the environment and the
          quality of life of its employees by developing maintenance-free products that are recyclable and through our
          manufacturing process, waste is disposed of in a responsible manner.</p>
        <p> We are the only dealers in the Treasure Valley offering this system! If you would like more information call
          Idaho Custom Iron Works 208-602-2780</p>
        <router-link :to="{ name: 'UltraLox' }">
          <p class="mt-4">Click here to see more of UltraLox!</p>
        </router-link>
      </div>
      <div class="col-12 col-md-5 text-center mt-3">
        <div>
          <h5>Before</h5>
          <img src="/src/assets/img/before1.jpg" alt="" class="img-fluid beforeAndAfter rounded">
        </div>
        <div>
          <h5 class="mt-5">After</h5>
          <img src="/src/assets/img/after1.jpg" alt="" class="img-fluid beforeAndAfter rounded">
        </div>
      </div>
    </section>


    <section class="row mt-5 mb-2 px-4 align-items-center">
      <div class="col-12 col-md-5 d-flex justify-content-center order-2 order-md-1">
        <img class="img-fluid rounded coolImg"
          src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/420902139_805051591661702_8527944067580198862_n.jpg?stp=cp6_dst-jpg&_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=PY9apN3NUj0Ab4Dbs50&_nc_ht=scontent-sea1-1.xx&oh=00_AfC7QVLd7TLGdD6PI0sB1ZuqWqJktbD2r35nPu5m0zluhg&oe=662C96ED"
          alt="">
      </div>
      <div class="col-12 col-md-7 text-center order-1 order-md-2">
        <h2>Commercial Work</h2>
        <p class="mt-3">Idaho Custom Iron Works is your premier destination for exquisite custom balconies and rails,
          designed to elevate
          the aesthetics and safety of commercial spaces. With a passion for craftsmanship and a dedication to
          excellence, we specialize in crafting custom made iron structures that seamlessly integrate functionality with
          style. Whether you're envisioning a striking balcony overlooking a bustling cityscape or sturdy yet elegant
          railings for a commercial property, our skilled artisans are here to turn your vision into reality. Explore
          our portfolio to witness the beauty and durability of our ironwork, and let us bring an unparalleled level
          of sophistication and security to your commercial project</p>
        <router-link :to="{ name: 'Commercial' }">
          <p class="mt-4">Click here to see more of our commercial work!</p>
        </router-link>
      </div>
    </section>

    <section class="row mt-5 mb-2 px-4 align-items-center">
      <div class="col-12 col-md-7 text-center">
        <h2>Residential Work</h2>
        <p>Elevate your residential spaces with our exquisite ironwork, meticulously designed to enhance both the beauty
          and safety of your property. From timeless balcony designs that offer a private oasis to elegant railings that
          add character to your home's exterior. With a keen eye for detail and a passion for quality, our team will
          work closely with you to bring your vision to life, ensuring a seamless integration of functionality and
          aesthetics.</p>
        <router-link :to="{ name: 'Residential' }">
          <p class="mt-4">Click here to see more of our residential work!</p>
        </router-link>
      </div>
      <div class="col-12 col-md-5 d-flex justify-content-center">
        <img class="img-fluid rounded coolImg"
          src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/402611988_762649029235292_2579745254667678574_n.jpg?stp=cp6_dst-jpg&_nc_cat=108&ccb=1-7&_nc_sid=5f2048&_nc_ohc=2Ie7JFppwsQAb49UqqS&_nc_ht=scontent-sea1-1.xx&oh=00_AfAT5BOKV2UHyOflFqItqNifuCg0PyWym2VjWvVdKpcADQ&oe=662CA6D4"
          alt="">
      </div>
    </section>


    <section class="row mt-5 mb-2 px-4 align-items-center">
      <div class="col-12 col-md-5 d-flex justify-content-center order-2 order-md-1">
        <img class="img-fluid rounded coolImg mb-3"
          src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/406189883_770513675115494_8499299986155006685_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=N97Ky8dM1KIAb5het3s&_nc_ht=scontent-sea1-1.xx&oh=00_AfAR8n6i3Tq8KW8y8h5ygKdjY6mghgNYteY0LXRe3LqkSg&oe=662CBCBE"
          alt="">
      </div>
      <div class="col-12 col-md-7 text-center order-1 order-md-2">
        <h2>Custom Work</h2>
        <p class="mt-3">From initial concept to final installation, we collaborate closely with our clients, ensuring
          that every detail surpasses expectations.
          Explore our portfolio to discover the beauty and diversity of our custom work. Join us on a journey where
          imagination knows no bounds and where iron becomes more than just a material—it becomes a testament to the
          beauty of craftsmanship and the power of individuality.</p>
        <router-link :to="{ name: 'Custom' }">
          <p class="mt-4">Click here to see more of our custom work!</p>
        </router-link>
      </div>
    </section>

    <section class="row mt-5 mb-4">
      <div class="col-12 mt-4">
        <h1 class="text-center">Who we work with!</h1>
      </div>
      <div class="row align-items-center justify-content-around my-3">
        <div class="col mx-5 lighten-30 selectable rounded p-3 d-flex justify-content-center">
          <a href="https://ultralox.com/" title="Click Here to see the UltraLox Website!" target="_blank">
            <img class="img-fluid logo"
              src="https://idahocustomironworks.com/wp-content/uploads/2021/08/UL-Logo-2020-Horizontal-300x59.png"
              alt="">
          </a>
        </div>

        <div class="col mx-5 lighten-30 selectable rounded p-3 d-flex justify-content-center">
          <a href="https://www.harmonyrailing.com/" title="Click Here to see the Harmony Website!" target="_blank">
            <img class="img-fluid logo"
              src="https://www.deckandrailing.com/wp-content/uploads/2021/08/Harmony-Railing-Logo-600x151.png" alt="">
          </a>
        </div>

        <div class="col mx-5 lighten-30 selectable rounded p-3 d-flex justify-content-center">
          <a href="https://www.viewrail.com/?hsa_grp=1245747043062995&hsa_net=adwords&hsa_src=o&hsa_ad=&hsa_tgt=kwd-77859376985053:loc-190&hsa_kw=viewrail&hsa_cam=1584923268&hsa_acc=7699129968&hsa_mt=e&hsa_ver=3&msclkid=fe1d19961b781bcf6eb87fa58402b715&utm_source=bing&utm_medium=cpc&utm_campaign=Viewrail%20-%20Brand%20-%20Search%20-%20VR%20-%20Bing&utm_term=viewrail&utm_content=Viewrail"
            title="Click Here to see the ViewRail Website!" target="_blank">
            <img class="img-fluid logo rounded"
              src="https://3944142.fs1.hubspotusercontent-na1.net/hub/3944142/hubfs/Viewrail-Logo-Sep-23-2021-12-30-42-11-PM.png?height=120&name=Viewrail-Logo-Sep-23-2021-12-30-42-11-PM.png"
              alt="">
          </a>
        </div>

        <div class="col mx-5 lighten-30 selectable rounded p-3 d-flex justify-content-center">
          <a href="https://superiordecksmfg.com/" title="Click here to see the Superior Deck Website!" target="_blank">
            <img class="img-fluid logo rounded"
              src="https://superiordecksmfg.com/wp-content/uploads/2021/02/Logo-Superior-Deck.png" alt="">
          </a>
        </div>
      </div>
    </section>


  </div>
</template>


<script>
import fp1 from '../assets/img/fp1.jpg'
import fp2 from '../assets/img/fp2.jpg'
import fp3 from '../assets/img/fp3.jpg'
export default {

  data() {
    return {
      images: [
        fp1,
        fp2,
        fp3,
      ],
      currentIndex: 0,
    };
  },
  computed: {
    currentImage() {
      return this.images[this.currentIndex];
    },
  },
  mounted() {
    this.startSlideshow();
  },
  methods: {
    startSlideshow() {
      this.slideShowInterval = setInterval(() => {
        this.nextImage();
      }, 2500);
    },
    nextImage() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
  },
  beforeUnmount() {
    clearInterval(this.slideShowInterval);
  },
};
</script>


<style scoped lang="scss">
.heroImg {
  background-size: cover;
  background-position: center;
  min-height: 65dvh;
}

.box {
  background-color: rgba(52, 52, 52, 0.785);
  min-width: 45vw;
  max-height: 100vh;
  align-items: center;
  box-shadow: 0px 5px 20px black;
}

.text-shadow {
  text-shadow: 2px 2px 4px black;
}

.beforeAndAfter {
  max-height: 33dvh;
  width: 55dvh;
  box-shadow: 5px 5px 20px black;
}

.coolImg {
  background-image: url(currentImage);
  background-size: cover;
  background-position: center;
  max-height: 45dvh;
  width: 65dvh;
  box-shadow: 5px 5px 20px black;
}

.logo {
  max-height: 25dvh;
  max-width: 30dvh;
}

.funFont {
  font-family: "Tektur", sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>
