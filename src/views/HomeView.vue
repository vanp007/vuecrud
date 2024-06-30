
<template>
  <div class="container">
    <!-- Heading Row-->
    <div class="row gx-4 gx-lg-5 align-items-center my-5">
      <div class="col-lg-7">
        <img
          class="img-fluid rounded mb-4 mb-lg-0"
          src="/src/assets/img/pic1.jpg"
          alt="..."
        />
      </div>
      <div class="col-lg-5">
        <h1 class="font-weight-light">MWANALUGALI MKOBA CLASS OF 2012</h1>
        <p>
          This is a template that is great for small businesses. It doesn't have
          too much fancy flare to it, but it makes a great use of the standard
          Bootstrap core components. Feel free to use this template for any
          project you want!
        </p>
        <a class="btn btn-success" href="#!">Read More</a>
      </div>
    </div>
    <!-- Call to Action-->
    <div class="my-1 py-1 text-center">
      <h3 class="">LATEST EVENTS</h3>
    </div>
    <!-- Content Row-->
    <!--div class="row gx-4 gx-lg-5">
      <div class="col-md-4 mb-5">
        <div class="card h-100">
          <h2 class="card-header">Event One</h2>
          <div class="card-body">
            <img class="card-img" src="/src/assets/img/com1.jpg" alt="..." />
          </div>
          <div class="card-footer">
            <a class="btn btn-success btn-sm" href="#!">More Info</a>
          </div>
        </div>
      </div>
      <div class="col-md-4 mb-5">
        <div class="card h-100">
          <h2 class="card-header">Event Two</h2>
          <div class="card-body">
            <img class="card-img" src="/src/assets/img/com2.jpg" alt="..." />
          </div>
          <div class="card-footer">
            <a class="btn btn-success btn-sm" href="#!">More Info</a>
          </div>
        </div>
      </div>
      <div class="col-md-4 mb-5">
        <div class="card h-100">
          <h2 class="card-header">Event Three</h2>
          <div class="card-body">
            <img class="card-img" src="/src/assets/img/com3.jpg" alt="..." />
          </div>
          <div class="card-footer">
            <a class="btn btn-success btn-sm" href="#!">More Info</a>
          </div>
        </div>
      </div>
    </div-->
  </div>

  <!-- Carousel-->
  <Carousel
    class="mb-4"
    :items-to-show="3"
    :autoplay="5000"
    :wrap-around="true"
  >
    <Slide v-for="slide in 10" :key="slide">
      <div class="bg-success carousel__item">{{ slide }}</div>
    </Slide>

    <!-- <template #addons>
      <Pagination />
    </template> -->
  </Carousel>

  <!-- Footer-->
  <footer class="py-5 bg-dark">
    <div class="container px-4 px-lg-5">
      <p class="m-0 text-center text-white">
        Copyright &copy; {{ new Date().getFullYear() }} | Developed and
        Maintained by Mwanalugali Mkoba
      </p>
    </div>
  </footer>
</template>

<style>
.carousel__item {
  min-height: 200px;
  width: 100%;
  background-color: var(--vc-clr-primary);
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>

<script>
import { defineComponent } from "vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "WrapAround",
  components: {
    Carousel,
    Slide,
    Pagination,
  },
});
</script>
