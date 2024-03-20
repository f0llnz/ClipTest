<template>
    <main style=" padding-top: 42px;">
        <div class="
        mainn 
        bg-white flex 
        flex-col
        gap-8
        justify-center
        px-4
        py-10
        " 
        style="width: 976px; height: 320px; border-radius: 20px; position: relative;">
        <div class="header flex justify-between">
            <h2 style="font-size: 20px ;color: #1D2D35; font-weight: 600;">ცნობილი ფაქტები</h2>
            <div class="buttons flex gap-2">
                <div class="left shadow-2xl"><img src="../../public/left.png" alt=""></div>
                <div class="right shadow-2xl"><img src="../../public/right.png" alt=""></div>
            </div>
        </div>
        <div class="slider items-center " style="width: 952px; height: 406px ">
            <Swiper
            :modules="modules"
            :space-between="15"
            :slides-per-view="3"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
            >
                <SwiperSlide>
                    <img src="/maincpic2.jpg" alt=""
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/forest.jpg" alt="" 
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/maincpic2.jpg" alt=""
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/forest.jpg" alt="" 
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/maincpic2.jpg" alt=""
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/forest.jpg" alt="" 
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/maincpic2.jpg" alt=""
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
                <SwiperSlide>
                    <img src="/forest.jpg" alt="" 
                    style="width: 288px; height: 120px; border-radius: 20px;">
                    <h1 style="font-size: 14px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე 
                        ღირებულების</h1>
                </SwiperSlide>
            </Swiper>
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
        .swiper-slide{
            border-radius: 20px;
            gap: 0.3rem;
            padding: 1rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 312px;
            height: 204px;
            background-color: #F0F4F5;
        }

        .left, .right{
            width: 40px !important;
            height: 40px !important;
            background-color: white !important;
            border-radius: 50% !important;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 3px 3px 3px #ccc;
            cursor: pointer;
        }

        @media only screen and (max-width: 1340px) and (min-width: 1180px) {
            .mainn{
                width: 840px !important;
                overflow-y: hidden;
                scrollbar-width: thin; 
                scrollbar-color: #F0F4F5 #ffffff;
            }
            .header h2{
                display: none;
            }
            .header .buttons{
                margin: auto;
            }
        }

        @media only screen and (max-width: 1180px) and (min-width: 800px) {
            .mainn{
                width: 928px !important;
                overflow-y: hidden;
                scrollbar-width: thin; 
                scrollbar-color: #F0F4F5 #ffffff;
            }

            .header h2{
                display: inline-block;
            }
        }

        @media only screen and (max-width: 360px) {
            .mainn{
                width: 360px !important;
                height: 320px !important;
                overflow-y: hidden;
                scrollbar-width: thin; 
                scrollbar-color: #F0F4F5 #ffffff;
            }
            main{
                padding-top: 0px !important;
            }
            .header .buttons{
                display: none;
            }
        }
  </style>