<script>
    import { Swiper, SwiperSlide } from "swiper/svelte";
  
    // Import Swiper styles
    import "swiper/css";
  
    import "swiper/css/pagination";
  
    import "./style/swiper.css";
  
    // import required modules
    import { Mousewheel, Pagination } from "swiper";

    import CodeBox from "./codebox.svelte"
    import AboutBar from "./about.svelte"
    import Projects from "./projects.svelte"
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
    class="mySwiper swiper-v"
  >
  <SwiperSlide class="bg-emerald-900">
  </SwiperSlide>
  
  <SwiperSlide class="bg-zinc-800">
    <AboutBar/>
  </SwiperSlide>
  
    
    <SwiperSlide class="bg-emerald-900">
      <CodeBox/>
    </SwiperSlide>

    <SwiperSlide class="bg-zinc-800">
      <Projects/>
    </SwiperSlide>
    
  </Swiper>
  


<style>

</style>