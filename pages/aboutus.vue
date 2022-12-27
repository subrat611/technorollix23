<template>
  <div class="about-page">
    <nav-bar />

    <!-- about container -->
    <div class="about-container">
      <!-- image container -->
      <div class="image-container">
        <nuxt-img
          src="/opju-image.png"
          format="webp"
          loading="lazy"
          class="opju-bg-image"
        />
        <div class="overlay"></div>
        <p class="title">about</p>
      </div>

      <!-- about -->
      <div class="about-content">
        <!-- about opju -->
        <div class="about-opju">
          <p class="about-title">about o.p. jindal university</p>
          <p class="about-para">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam rerum
            error non natus debitis hic ipsum esse, doloremque dolorum optio
            labore ipsam similique aspernatur, placeat repellendus earum
            excepturi eveniet ratione soluta ducimus eius libero. Possimus
            aliquid voluptatem vel, praesentium fugit ducimus, quae maiores
            quibusdam sit, quas placeat tempore earum facilis voluptatibus? Fuga
            voluptatem officia autem aperiam, impedit, exercitationem
            consequatur, dignissimos tempora mollitia qui commodi! Veritatis
            ratione dignissimos voluptatem reprehenderit ad odio ducimus
            quisquam nihil minus magni eum omnis libero rem, qui sit repudiandae
            optio possimus, cupiditate accusantium consequatur doloribus
            nesciunt? Rem quasi dignissimos quaerat distinctio ab impedit culpa
            error sequi?
          </p>
        </div>

        <!-- patron message -->
        <div class="patron-container">
          <p class="patron-title-one">patron's message</p>
          <p class="patron-title-two">
            SHRI NAVEEN JINDAL Chairman, Jindal Steel and Power Ltd
          </p>
          <p class="patron-para">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias,
            quasi voluptatibus placeat iste atque culpa, perspiciatis molestiae
            asperiores velit iusto aspernatur dignissimos cupiditate ipsam quod
            enim quia deserunt officia porro. Nostrum amet ratione quis sit
            nesciunt vitae reprehenderit, doloribus hic fugiat autem rerum
            accusamus distinctio iure ipsam nobis qui natus expedita! Explicabo
            maiores iusto culpa voluptatem aliquid fuga excepturi blanditiis
            sequi asperiores, animi ex quod distinctio aut error unde placeat in
            fugiat numquam illo nemo hic nihil modi. Quia ad enim molestias
            dolores maiores eaque earum ducimus fuga laborum voluptatum,
            asperiores labore, totam ipsam nulla modi nisi, consectetur
            consequuntur sequi.
          </p>
          <p class="patron-para">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Consequatur laborum rem sed suscipit corrupti odio quae
            exercitationem, dicta assumenda corporis incidunt ea vitae rerum
            eveniet asperiores impedit deleniti voluptates. Quos nihil sint
            inventore autem voluptates minus, consectetur optio quo eaque. Eum
            iure consequuntur, totam perspiciatis distinctio inventore provident
            quasi quo in ea perferendis saepe consequatur officia, numquam rerum
            doloremque itaque voluptatem eveniet vero voluptatum est suscipit,
            iste nostrum omnis. Iure beatae ipsum explicabo laudantium autem
            cumque quis ad similique sunt iste vitae incidunt labore fuga
            repellendus modi, quam molestiae omnis. Neque dignissimos blanditiis
            itaque assumenda quia earum nulla laboriosam recusandae.
          </p>
        </div>

        <!-- about technorollix -->
        <div class="about-techno">
          <p class="techno-title">about technorollix</p>
          <p class="techno-para">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi magni
            aut cum at corrupti consequuntur molestiae facere laborum ullam
            labore amet, deserunt tenetur officia. Illo repellat ducimus
            veritatis? Minus officia esse repellat quas molestiae natus optio,
            eveniet magnam explicabo labore aperiam corporis est magni vitae
            architecto temporibus quis. Aut voluptates repellendus ut minima
            vero enim libero laboriosam velit possimus laudantium natus
            explicabo quam neque laborum quidem, sapiente ab illum corrupti sit
            ratione quas voluptatem corporis numquam. At labore culpa debitis
            porro, dolor assumenda facere doloribus id quisquam hic maiores
            perspiciatis, beatae dolorem tempore sint totam praesentium
            reiciendis perferendis accusantium aspernatur.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<style lang="scss" scoped>
.about-page {
  background: #000;

  .about-container {

    color: #fff;
    .image-container {
      position: relative;
      height: 350px;
      width: 100vw;

      .opju-bg-image {
        position: absolute;
        height: 100%;
        width: 100%;
        object-fit: cover;
      }

      .overlay {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-color: #000;
        opacity: 0.5;
      }

      .title {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 2rem;
        text-transform: uppercase;
        color: #fff;
        font-weight: bold;
      }
    }

    .about-content {
      padding: 1rem 5rem;
      font-family: 'Poppins', sans-serif;
      font-weight: 600;

      .about-opju {
        margin-bottom: 2rem;
        .about-title {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1.5rem;
        }
      }

      .patron-container {
        margin-bottom: 2rem;
        .patron-title-one {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1rem;
        }
        .patron-title-two {
          font-size: 1.5rem;
        }
      }

      .about-techno {
        margin-bottom: 2rem;
        .techno-title {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1rem;
        }
      }
    }
  }
}
</style>
