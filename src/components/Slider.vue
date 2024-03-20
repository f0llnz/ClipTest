<template>
  <main style="padding-top: 42px;">
    <div class=" mainn  
    bg-white flex 
    justify-center
    px-4
    py-4
    " 
    style="width: 976px; height: 606px; border-radius: 20px;">
      <div class="slider items-center " style="width: 952px; height: 406px ">
          <Swiper
          :modules="modules"
          :space-between="5"
          :slides-per-view="1"
          :pagination="{ clickable: true, dynamicBullets: true }"
          @swiper="onSwiper"
          @slideChange="onSlideChange"
          :navigation="true"
          >
              <SwiperSlide>
                  <img class="images" src="/maincpic2.jpg" alt=""
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/forest.jpg" alt="" 
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/maincpic2.jpg" alt=""
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/forest.jpg" alt="" 
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/maincpic2.jpg" alt=""
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/forest.jpg" alt="" 
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/maincpic2.jpg" alt=""
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
              <SwiperSlide>
                  <img class="images" src="/forest.jpg" alt="" 
                  style="width: 952px; height: 406px; border-radius: 20px;">
              </SwiperSlide>
          </Swiper>
          <div class="main flex flex-col">
            <div class="small flex gap-1 py-3">
              <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
              <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
            </div>
            <h1 style="font-size: 24px; color: #1D2D35; font-weight: 700;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
              ღირებულების ინფრასტრუქტურული პროექტები დაიწყება</h1>
            <h5 class="py-2" style="font-size: 15px ;color: #657178; font-weight: 600;">განთავსების (ლისტინგის) ორგანიზატორი სომხეთის ბანკი სს “არდშიბანკია”. ობლიგაციის ნომინალი - 1000 USD</h5>
          </div>
      </div>
    </div>
  </main>
</template>

<script setup>
    import { Navigation, Pagination} from 'swiper/modules';
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/bundle';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';
    import 'swiper/css/scrollbar';
</script>

<script>
    export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Navigation, Pagination]
      };
    },
  };
</script>

<style lang="css" scoped>
 @media only screen and (max-width: 1340px) and (min-width: 1181px) {
      main{
        width: 840px !important;
        height: 630px !important;
      }
      .mainn{
        padding-left: 150px;
        width: 840px !important;
        height: 630px !important;
      }
      .images{
        width: 816px !important;
        height: 406px !important; 
      }
      .main{
        width: 816px !important;
      }
      .main h5{
        font-size: 13.5px !important;
        padding-top: 1rem;
      }
      .slider{
        width: 816px !important;
        margin-left: -8.5rem;
      }
    }

    @media only screen and (max-width: 1180px) and (min-width: 800px) {
      main{
        width: 928px !important;
        height: 606px !important;
      }
      .mainn{
        padding-left: 150px;
        width: 928px !important;
        height: 606px !important;
      }
      .images{
        width: 904px !important;
        height: 406px !important; 
      }
      .main{
        width: 904px !important;
      }
      .main h5{
        font-size: 13.5px !important;
        padding-top: 1rem;
      }
      .slider{
        width: 816px !important;
        margin-left: -8.5rem;
      }
    }

    @media only screen and (max-width: 360px) {
      main{
        width: 360px !important;
        height: 496px !important;
      }
      .mainn{
        padding-left: 150px;
        width: 360px !important;
        height: 496px !important;
      }
      .images{
        width: 328px !important;
        height: 280px !important; 
      }
      .main{
        width: 360px !important;
      }
      .main h5{
        display: none;
      }
      .main h1{
        font-size: 20px !important;
      }
      .slider{
        width: 328px !important;
        margin-left: -8.5rem;
      }
    }
</style>