<script>
    import { Swiper, SwiperSlide } from "swiper/svelte";
  
    // Import Swiper styles
    import "swiper/css";
  
    import "swiper/css/pagination";
  
    import "./style/swiper.css";
  
    // import required modules
    import { Mousewheel, Pagination } from "swiper";

    import CodeBox from "./codebox.svelte"
  </script>
  
  
  
  
  <Swiper
    direction={"vertical"}
    slidesPerView={1}
    spaceBetween={0}
    mousewheel={true}
    pagination={{
      clickable: true,
    }}
    modules={[Mousewheel, Pagination]}
    class="mySwiper"
  >
    <SwiperSlide class="bg-emerald-900">
      <CodeBox/>
    </SwiperSlide>
  
    <SwiperSlide class="bg-zinc-800">
    Slide 2
    </SwiperSlide>
    
    <SwiperSlide class="bg-emerald-900">
    Slide 3
    </SwiperSlide>
    <SwiperSlide class="bg-zinc-800">
    Slide 4
    </SwiperSlide>
    
  </Swiper>
  


<style>

</style>