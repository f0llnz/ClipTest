<template>
    <div class="Patterns flex flex-col gap-8">
      <div class="patterns side p-2" style="width: 304px; height: 396px; border-radius: 20px; background-color: #FFFFFF;">
          <img src="/pic5.png" class="pimages" alt="" style="width: 288px; height: 264px; border-radius: 20px;">
          <div class="main flex flex-col">
              <div class="small flex gap-1 py-2">
                <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
              </div>
              <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების  </h1>
          </div>
      </div>
      <div class="saerto flex gap-8">
        <div class="first flex flex-col gap-8">
            <div class="patterns p-2" style="width: 304px; height: 188px; border-radius: 20px; background-color: #FFFFFF;">
                <img src="/pic1.png" class="pimages" alt="" style="width: 288px; height: 96px; border-radius: 20px;">
                <div class="main flex flex-col">
                    <div class="small flex gap-1 py-2">
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
                    </div>
                    <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ </h1>
                  </div>
            </div>
            <div class="patterns p-2" style="width: 304px; height: 188px; border-radius: 20px; background-color: #FFFFFF;">
                <img src="/pic2.png" class="pimages" alt="" style="width: 288px; height: 96px; border-radius: 20px;">
                <div class="main flex flex-col">
                    <div class="small flex gap-1 py-2">
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
                    </div>
                    <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ </h1>
                </div>
            </div>
        </div>
            <div class="patterns responsive p-2" style="width: 304px; height: 396px; border-radius: 20px; background-color: #FFFFFF;">
                <img src="/pic5.png" class="pimages" alt="" style="width: 288px; height: 264px; border-radius: 20px;">
                <div class="main flex flex-col">
                    <div class="small flex gap-1 py-2">
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
                    </div>
                    <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ ლარამდე ღირებულების  </h1>
                  </div>
            </div>
        <div class="last flex flex-col gap-8">
            <div class="patterns p-2" style="width: 304px; height: 188px; border-radius: 20px; background-color: #FFFFFF;">
                <img src="/pic3.png" class="pimages" alt="" style="width: 288px; height: 96px; border-radius: 20px;">
                <div class="main flex flex-col">
                    <div class="small flex gap-1 py-2">
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
                    </div>
                    <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ </h1>
                  </div>
            </div>
            <div class="patterns p-2" style="width: 304px; height: 188px; border-radius: 20px; background-color: #FFFFFF;">
                <img src="/pic4.png" class="pimages" alt="" style="width: 288px; height: 96px; border-radius: 20px;">
                <div class="main flex flex-col">
                    <div class="small flex gap-1 py-2">
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">12.08.2023</p>
                      <p style="background-color: #F5F8FF; border-radius: 5px; padding: 5px; font-size: 12px; font-weight: 700;">პოლიტიკა</p>
                    </div>
                    <h1 style="font-size: 15px; color: #1D2D35; font-weight: 600;">ქვემო ქართლის რეგიონში 20 მლნ </h1>
                  </div>
            </div>
        </div>
      </div>
    </div>
</template>

<script setup>

</script>

<style lang="css" scoped>

    .side{
      display: none;
    }

   @media only screen and (max-width: 1340px) and (min-width: 1180px) {
      .patterns{
        width: 264px !important;
      }
      .patterns .main h1{
        font-size: 13px !important;
      }
    }

    @media only screen and (max-width: 1180px) and (min-width: 800px) {
      
      
      .responsive{
        display: none;
      }
      
      .patterns{
        width: 448px !important;
        height: 252px !important;
      }
      
      .pimages{
        width: 432px !important;
        height: 160px !important;
      }
      .side{
        display: block;
        width: 928px !important;
        height: 388px !important;
      }
      .side .pimages{
        width: 904px !important;
        height: 280px !important;
      }
    }

    @media only screen and (max-width: 360px) {
     
      .responsive{
        display: none;
      }
      
      .patterns{
        width: 360px !important;
        height: 276px !important;
      }
      
      .pimages{
        width: 344px !important;
        height: 160px !important;
      }
      
      .saerto{
        display: flex;
        flex-direction: column;
      }
      
      .side{
        display: block;
        width: 360px !important;
        height: 412px !important;
      }

      .side .pimages{
        width: 336px !important;
        height: 280px !important;
      }
    }
</style>