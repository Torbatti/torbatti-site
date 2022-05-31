<script>
    import { Swiper, SwiperSlide } from "swiper/svelte";
  
    // Import Swiper styles
    import "swiper/css";
  
    import "swiper/css/pagination";
    import "swiper/css/navigation";
  
    import "./style/swiper.css";
  
    // import required modules
    import { Pagination, Navigation } from "swiper";
    const pagination = {
    clickable: true,
    renderBullet: function (index, className) {
      return '<span class="' + className + '">' + (index + 1) + "</span>";
    },
    }; 
  </script>


<Swiper {pagination} navigation={true} modules={[Pagination,Navigation]} class="mySwiper2 swiper-h">
    <SwiperSlide>Slide 1</SwiperSlide>
    <SwiperSlide>Slide 2</SwiperSlide>
    <SwiperSlide>Slide 3</SwiperSlide>
    <SwiperSlide>Slide 4</SwiperSlide>
</Swiper>
  

<style>
 

</style>