<template>
    <nav class="bg-white text-black">
      <div class="flex justify-between items-center navbar" style="padding: 32px 15.6%;">
        <div class="logo-container">
            <img src="../../public/Logo.png" alt="" class="logo">
        </div>
        <ul class="flex space-x-3 gap-6 firstUl">
            <li v-for="(item, index) in visibleItems" :key="index">
            <a :href="item.link" style="color: #657178; font-weight: 600; font-size: 18px;">{{ item.label }}</a>
            </li>
            <li class="dropdown">
            <a href="#" class="flex items-center justify-center gap-2 other" style="color: #657178; font-weight: 600; font-size: 18px;">
                სხვა
                <svg class="arrow" width="11" height="7" viewBox="0 0 11 7" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M10.0303 0.96967C10.3232 1.26256 10.3232 1.73744 10.0303 2.03033L6.03033 6.03033C5.73744 6.32322 5.26256 6.32322 4.96967 6.03033L0.96967 2.03033C0.676777 1.73744 0.676777 1.26256 0.96967 0.96967C1.26256 0.676777 1.73744 0.676777 2.03033 0.96967L5.5 4.43934L8.96967 0.96967C9.26256 0.676777 9.73744 0.676777 10.0303 0.96967Z" fill="#657178"/>
                </svg>
            </a>
            <ul class="dropdown-menu shadow-2xl">
                <li v-for="(item, index) in dropdownItems" :key="index">
                <a style="color: #657178; font-weight: 600; font-size: 18px;" :href="item.link">{{ item.label }}</a>
                </li>
            </ul>
            </li>
        </ul>
        <div class="flex items-center intel">
          <div class="mr-4 flex justify-center items-center rounded-full cursor-pointer" style="background-color: #F5F8FF; width: 32px; height: 32px;">
            <img src="../../public/Facebook.png" alt="Facebook Icon">
          </div>
          <div class="mr-4 flex justify-center items-center rounded-full cursor-pointer" style="background-color: #F5F8FF; width: 32px; height: 32px;">
            <img src="../../public/Instagram.png" alt="Instagram Icon">
          </div>
          <div class="flex items-center">
            <div class="relative">
              <input
                style="background-color: #F5F8FF;" 
                type="text"
                placeholder="ძიება"
                class="bg-white rounded-full py-2 px-4 pr-10 w-56 h-12 focus:outline-none focus:ring-2 focus:ring-blue-500">
              <img src="../../public/Icon.png" alt="magnifying glass" class="absolute right-3 top-1/2 transform -translate-y-1/2">
            </div>
          </div>
        </div>
      </div>
    </nav>
  </template>
  
<script setup>

  import Burger from './Burger.vue'
  import { ref, computed, onMounted, onUnmounted, reactive } from 'vue';

  const menuItems = [
      { label: 'პოლიტიკა', link: '#' },
      { label: 'საზოგადოება', link: '#' },
      { label: 'სამართალი', link: '#' },
      { label: 'ბიზნესი & ეკონომიკა', link: '#' }
  ];

  const dropdownItems = reactive([
      { label: 'ეკონომიკა', link: '#' },
      { label: 'რელიგია', link: '#' },
  ]);
  const windowWidth = ref(window.innerWidth);
  let isMobile = windowWidth.value <= 1907;

  const updateWidth = () => {
      const newWidth = window.innerWidth;
      const newIsMobile = newWidth <= 1907;
      
      if (isMobile !== newIsMobile) {
          isMobile = newIsMobile;
          if (isMobile) {
              const lastItem = menuItems.pop();
              if (lastItem) {
                  dropdownItems.unshift(lastItem);
              }
          } else {
              const firstItem = dropdownItems.shift();
              if (firstItem) {
                  menuItems.push(firstItem);
              }
          }
      }
      windowWidth.value = newWidth;
  };

  const visibleItems = computed(() => {
      return isMobile ? menuItems.slice(0, -1) : menuItems;
  });

  onMounted(() => {
      window.addEventListener('resize', updateWidth);
  });

  onUnmounted(() => {
      window.removeEventListener('resize', updateWidth);
  });

</script>


  <style scoped>

  a{
    text-decoration: none;
    font-family: "BPG Banner Caps", sans-serif;
  }

  .dropdown:hover .other {
    color: #585EE3 !important;
  }

  .dropdown:hover path {
    fill: #585EE3 !important;
    }

  a:hover{
    color: #585EE3 !important; 
  }

  .logo{
    min-width: 138px;
    cursor: pointer;
  }

  .dropdown-menu a:hover {
      color: #585EE3 !important; 
  }

  .intel {
    margin-left: 6%;
  }
  
  ::placeholder {
    color: #1D2D35;
  }
  
  .logo-container {
    margin-right: 25px; 
    border-right: 1px solid #ccc;
    padding-right: 25px; 
  }
  
  .dropdown {
    position: relative;
  }
  
  .dropdown-menu {
    display: none;
    position: absolute;
    background-color: white;
    border: 1px solid #ccc;
    left: -50%;
    top:100%;
    padding: 10px;
    z-index: 1000;
    border-radius: 1rem;
    min-width: 180px;
    width: auto;
    box-shadow: black;
    border: none;
  }

  .dropdown:hover .dropdown-menu,
    .dropdown-menu:hover {
      display: block;
      padding: 0.5rem;
    }

  .dropdown-menu li{
    padding: 0.5rem;
    color: #657178;
  }
  
  .dropdown:hover .dropdown-menu {
    display: block;
  }
  
  @media only screen and (max-width: 1680px) and (min-width: 1024px)  {
    .navbar{
        padding: 32px 50px !important;
    }
  }

  @media only screen and (max-width: 1180px) and (min-width: 0px)  {
    .firstUl{
      display: none;
    }

    .intel{
      padding-right: 5rem !important;
    }
  }

  @media only screen and (max-width: 360px) {
    .firstUl{
      display: none;
    }
    .intel{
      display: none;
    }
    }
  </style>