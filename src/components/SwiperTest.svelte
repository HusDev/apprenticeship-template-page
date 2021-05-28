<script>
  // Import Swiper Svelte components
  import { Swiper, SwiperSlide } from "swiper/svelte";
  import "swiper/swiper-bundle.min.css";
</script>

<div>
  <h1>Swiper</h1>
  <!-- Swiper here -->
  <Swiper
    spaceBetween={50}
    slidesPerView={3}
  >
    <SwiperSlide>
      <div class="box">slide 1</div>
    </SwiperSlide>
    <SwiperSlide>
      <div class="box">slide 2</div>
    </SwiperSlide>
    <SwiperSlide>
      <div class="box">slide 3</div>
    </SwiperSlide>
    <SwiperSlide>
      <div class="box">slide 4</div>
    </SwiperSlide>
  </Swiper>
</div>

<style>
  div {
    margin-top: 200px;
  }

  .box {
    height: 200px;
    background-color: grey;
  }
</style>
