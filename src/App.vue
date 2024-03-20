<script setup>
  import Navbar from './components/Navbar.vue';
  import Slider from './components/Slider.vue';
  import News from './components/News.vue';
  import KnownFacts from './components/KnownFacts.vue';
  import Popular from './components/Popular.vue';
  import Patterns from './components/Patterns.vue';
  import Burger from './components/Burger.vue'
</script>

<template >
  <main style="background-color: #F0F4F5;">
    <nav style="position: relative;">
      <Burger class="burger" style="position: absolute;"/>
      <Navbar />
    </nav>
    <div class="body" style="padding-left: 15%">
      <slider class="responsive"/>
      <div class="side flex gap-8">
        <Slider />
        <News />
      </div>
      <div class="responsive newsandpopular flex py-10">
        <News />
        <Popular />
      </div>
      <div class="bottom flex gap-5">
        <div class="below flex flex-col gap-5">
          <KnownFacts />
          <Patterns />
        </div>
        <Popular class="side"/>
      </div>
    </div>
  </main>
</template>

<style scoped>

    .burger{
      display: none;
    }

    .responsive{
      display: none;
    }

    @media only screen and (max-width: 1920px) and (min-width: 1680px) {
      .body{
        padding-left: 15% !important;
      }
    }

    @media only screen and (max-width: 1680px) and (min-width: 1440px) {
      .body{
        padding-left: 2.5% !important;
      }
    }

    @media only screen and (max-width: 1440px) and (min-width: 1180px) {
      .body{
        padding-left: 2.0% !important;
      }
    }
    
    
    @media only screen and (max-width: 1180px) and (min-width: 1024px) {
      .body{
        padding-left: 1% !important;
      }
    }
    
    @media only screen and (max-width: 1180px) and (min-width: 359px) {
      .burger{
        display: inline-block;
        top: 3rem;
        right: 2rem;
      }

      .responsive{
        display: flex;
      }
      
      .body .side{
        display: none;
      }

      .newsandpopular{
        display: flex;
        flex-direction: row;
        gap: 2rem;
      }
    }

    @media only screen and (max-width: 1180px) and (min-width: 1038px) {
      .body{
        padding-left: 5% !important;
      }
    }

    @media only screen and (max-width: 1038px) and (min-width: 800px) {
      .body{
        padding-left: 1% !important;
      }
    }

    @media only screen and (max-width: 360px) {
      .body{
        padding-left: 0% !important;
      }
      .newsandpopular{
        display: flex;
        flex-direction: column;
        gap: 2rem;
      }
    }
</style>
