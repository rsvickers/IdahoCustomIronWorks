<script setup>

</script>

<template>
  <div class="container-fluid">
    <section class="row heroImg box">
      <div class="col-12 text-light box rounded p-2 mt-3 text-center text-shadow">
        <h1 class="">Idaho Custom Iron Works</h1>
        <h5 class="mt-5 p-2">We’re the company that exceeds the clients expectations. Idaho Custom Iron Works is locally
          owned,
          family operated and licensed in both Idaho and Oregon. We have over 15 years experience doing Commercial and
          Residential Metal Fabrication and install. </h5>
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
            src="https://mail.google.com/mail/u/3?ui=2&ik=299a11f884&attid=0.1&permmsgid=msg-f:1796706135910266378&th=18ef2eb614b2360a&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ9_JiHP6PHF-fgO6UZyISIpCZ6GoXhwzypOWw9T9cFro1t2qCDp_k0NDS7EejGoECuVhrtKXbPQ0k4027dTG90rOLaXtm5OJNc9cQKpGkn-fdM5VJdm82_4k8M&disp=emb&realattid=18ef2eb16c452350c661"
            alt="" class="img-fluid beforeAndAfter rounded">
        </div>
      </div>
    </section>


    <section class="row mt-5 mb-2">
      <div class="col-12 col-md-5 d-flex justify-content-center">
        <img class="img-fluid rounded coolImg"
          src="https://scontent-sea1-1.xx.fbcdn.net/v/t39.30808-6/420902139_805051591661702_8527944067580198862_n.jpg?stp=cp6_dst-jpg&_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=PY9apN3NUj0Ab4Dbs50&_nc_ht=scontent-sea1-1.xx&oh=00_AfC7QVLd7TLGdD6PI0sB1ZuqWqJktbD2r35nPu5m0zluhg&oe=662C96ED"
          alt="">
      </div>
      <div class="col-12 col-md-7 text-center">
        <h2>Commercial Work</h2>
        <router-link :to="{ name: 'Commercial' }">
          <p class="mt-4">Click here to learn more about our commercial work!</p>
        </router-link>
      </div>
    </section>

    <section class="row mt-5 mb-2">
      <div class="col-12 col-md-7 text-center">
        <h2>Residential Work</h2>
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


  </div>
</template>

<style scoped lang="scss">
.heroImg {
  background-image: url(https://idahocustomironworks.com/wp-content/uploads/2017/06/FB_IMG_1490236161047.jpg);
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
  max-height: 45dvh;
  width: 65dvh;
  box-shadow: 5px 5px 20px black;
}
</style>
