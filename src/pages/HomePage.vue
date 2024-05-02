<script>
export default {

  data() {
    return {
      images: [
        'https://idahocustomironworks.com/wp-content/uploads/2017/06/FB_IMG_1490236161047.jpg',
        'https://mail.google.com/mail/u/3?ui=2&ik=299a11f884&attid=0.2&permmsgid=msg-f:1797858015617073294&th=18f34656f971c08e&view=att&disp=safe&realattid=18f3464e8bcaa6c2dae3',
        'https://idahocustomironworks.com/wp-content/uploads/2017/06/FB_IMG_1490236166206.jpg',
        'https://idahocustomironworks.com/wp-content/themes/Idaho/images/ss-3.jpg',
        // 'https://idahocustomironworks.com/wp-content/themes/Idaho/images/ss-5.jpg',
        'https://mail.google.com/mail/u/3?ui=2&ik=299a11f884&attid=0.3&permmsgid=msg-f:1797857869538746663&th=18f34634f67f6127&view=att&disp=safe&realattid=18f3462b8417e4b90372',
        // Add more image URLs here
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
    // Start the slideshow when the component is mounted
    this.startSlideshow();
  },
  methods: {
    startSlideshow() {
      // Set interval to change image every 5 seconds (5000 milliseconds)
      this.slideshowInterval = setInterval(() => {
        this.nextImage();
      }, 2500); // Adjust timing as needed
    },
    nextImage() {
      // Increment index, reset to 0 if at the end of the array
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
  },
  beforeUnmount() {
    // Clear the interval when the component is destroyed to prevent memory leaks
    clearInterval(this.slideshowInterval);
  },
};
</script>


<template>
  <div class="container-fluid funFont">
    <section class="row heroImg box" :style="{ 'background-image': 'url(' + currentImage + ')' }">
      <!-- <img class="img-fluid coolImg rounded" :src="currentImage.url" :alt="currentImage.caption" /> -->
      <div class="col-12 text-light box rounded p-2 mt-3 text-center text-shadow">
        <h1 class="">Idaho Custom Iron Works</h1>
        <!-- <h5 class="mt-5 p-2">We’re the company that exceeds the clients expectations. Idaho Custom Iron Works is locally
          owned,
          family operated and licensed in both Idaho and Oregon. We have over 15 years experience doing Commercial and
          Residential Metal Fabrication and install. </h5> -->
        <h6>We're not just any fabrication company; we specialize in crafting custom ironworks tailored to our clients'
          unique visions. Idaho Custom Iron Works combines over 15 years of experience with our dedication to exceeding
          expectations. As a locally owned and family-operated business licensed in both Idaho and Oregon, we take pride
          in delivering exceptional results in both commercial and residential projects. Your imagination is our
          blueprint, and we're here to turn your ideas into stunning realities.</h6>
      </div>
    </section>

    <section class="row mt-4 mb-2">
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
          <p class="mt-4">Click here to learn more about UltraLox!</p>
        </router-link>
      </div>
      <div class="col-12 col-md-5 text-center mt-3">
        <div>
          <h5>Before</h5>
          <img
            src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/420474234_803642351802626_7995411150805441809_n.jpg?stp=cp6_dst-jpg&_nc_cat=103&ccb=1-7&_nc_sid=5f2048&_nc_ohc=6NswcLJK6xMAb4PZDGj&_nc_ht=scontent-sea1-1.xx&oh=00_AfABzPhPqCbbFTnjQjl34ONw1rNW-qeMVrS9BgBGjDdNKg&oe=66276C6F"
            alt="" class="img-fluid beforeAndAfter rounded">
        </div>
        <div>
          <h5 class="mt-5">After</h5>
          <img
            src="https://mail.google.com/mail/u/3?ui=2&ik=299a11f884&attid=0.1&permmsgid=msg-f:1796706135910266378&th=18ef2eb614b2360a&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ84vIuwYSu3MP_w5_W9WqXBgwSO9_exPuSBUI4zeXTP3o0LKaUin_IApM9mmEMfs8Uq5LIHNwnyxQj1DrsN6AsVIhjyne2Bd9p2dbDxvoldISbqt0zTk1oAsZ0&disp=emb&realattid=18ef2eb16c452350c661"
            alt="" class="img-fluid beforeAndAfter rounded">
        </div>
      </div>
    </section>


    <section class="row mt-5 mb-2">
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
          <p class="mt-4">Click here to learn more about our commercial work!</p>
        </router-link>
      </div>
    </section>

    <section class="row mt-5 mb-2">
      <div class="col-12 col-md-7 text-center">
        <h2>Residential Work</h2>
        <p>Elevate your residential spaces with our exquisite ironwork, meticulously designed to enhance both the beauty
          and safety of your property. From timeless balcony designs that offer a private oasis to elegant railings that
          add character to your home's exterior. With a keen eye for detail and a passion for quality, our team will
          work closely with you to bring your vision to life, ensuring a seamless integration of functionality and
          aesthetics.</p>
        <router-link :to="{ name: 'Residential' }">
          <p class="mt-4">Click here to learn more about our residential work!</p>
        </router-link>
      </div>
      <div class="col-12 col-md-5 d-flex justify-content-center">
        <img class="img-fluid rounded coolImg"
          src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/402611988_762649029235292_2579745254667678574_n.jpg?stp=cp6_dst-jpg&_nc_cat=108&ccb=1-7&_nc_sid=5f2048&_nc_ohc=2Ie7JFppwsQAb49UqqS&_nc_ht=scontent-sea1-1.xx&oh=00_AfAT5BOKV2UHyOflFqItqNifuCg0PyWym2VjWvVdKpcADQ&oe=662CA6D4"
          alt="">
      </div>
    </section>


    <section class="row mt-5 mb-2">
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
          <p class="mt-4">Click here to learn more about our custom work!</p>
        </router-link>
      </div>
    </section>

    <section class="row mt-5 mb-2">
      <div class="col-12">
        <h1 class="text-center">Who we work with!</h1>
      </div>
      <div class="mt-3 mb-3">
        <!-- <marquee behavior="" direction=""> -->
        <div class="d-flex align-items-center justify-content-between">
          <div class="mx-5">
            <a href="https://ultralox.com/" title="Click Here to see the UltraLox Website!">
              <img class="img-fluid logo"
                src="https://idahocustomironworks.com/wp-content/uploads/2021/08/UL-Logo-2020-Horizontal-300x59.png"
                alt="">
            </a>
          </div>

          <div class="mx-5">
            <a href="https://www.harmonyrailing.com/" title="Click Here to see the Harmony Website!">
              <img class="img-fluid logo"
                src="https://www.deckandrailing.com/wp-content/uploads/2021/08/Harmony-Railing-Logo-600x151.png" alt="">
            </a>
          </div>

          <div class="mx-5">
            <a href="https://www.viewrail.com/?hsa_grp=1245747043062995&hsa_net=adwords&hsa_src=o&hsa_ad=&hsa_tgt=kwd-77859376985053:loc-190&hsa_kw=viewrail&hsa_cam=1584923268&hsa_acc=7699129968&hsa_mt=e&hsa_ver=3&msclkid=fe1d19961b781bcf6eb87fa58402b715&utm_source=bing&utm_medium=cpc&utm_campaign=Viewrail%20-%20Brand%20-%20Search%20-%20VR%20-%20Bing&utm_term=viewrail&utm_content=Viewrail"
              title="Click Here to see the ViewRail Website!">
              <img class="img-fluid logo rounded"
                src="https://3944142.fs1.hubspotusercontent-na1.net/hub/3944142/hubfs/Viewrail-Logo-Sep-23-2021-12-30-42-11-PM.png?height=120&name=Viewrail-Logo-Sep-23-2021-12-30-42-11-PM.png"
                alt="">
            </a>
          </div>

          <div class="mx-5">
            <a href="https://superiordecksmfg.com/" title="Click here to see the Superior Deck Website!">
              <img class="img-fluid logo rounded"
                src="https://superiordecksmfg.com/wp-content/uploads/2021/02/Logo-Superior-Deck.png" alt="">
            </a>
          </div>

        </div>
        <!-- </marquee> -->
      </div>
    </section>


  </div>
</template>

<style scoped lang="scss">
.heroImg {
  // background-image: url(https://idahocustomironworks.com/wp-content/uploads/2017/06/FB_IMG_1490236161047.jpg);
  background-size: cover;
  background-position: center;
  min-height: 65dvh;
}

.box {
  background-color: rgba(52, 52, 52, 0.785);
  border-radius: 1%;
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
  // font-family: "Crete Round", serif;
  font-family: "Tektur", sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>
