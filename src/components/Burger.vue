<template>
  <div class="burger" @click="toggleMenu" :class="{ open: isOpen }">
    <div class="burger-icon">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
    <div class="menu" v-show="isOpen">
      <ul>
        <li>პოლიტიკა</li>
        <li>საზოგადოება</li>
        <li>სამართალი</li>
        <li>ბიზნესი & ეკონომიკა</li>
        <li>ეკონომიკა</li>
        <li>რელიგია</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Burger',
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>

<style scoped>
.burger {
  cursor: pointer;
  position: relative;
}

.burger-icon {
  width: 30px;
  height: 20px;
  position: relative;
  margin-top: -0.4rem;
  margin-right: 0.7rem;
}

.bar {
  width: 100%;
  height: 4px;
  background-color: #333;
  border-radius: 2px;
  margin-bottom: 5px;
}

.open .bar:nth-child(1) {
  transform: translateY(6px) rotate(45deg);
}

.open .bar:nth-child(2) {
  opacity: 0;
}

.open .bar:nth-child(3) {
  transform: translateY(-6px) rotate(-45deg);
}

.menu {
  position: absolute;
  top: 433%;
  right: -200%;
  width: 700%;
  height: 30vh;
  background-color: white;
  display: none;
  z-index: 999;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  box-shadow: 2px 3px 6px #ccc;
}

.open .menu {
  display: block;
  margin: auto;
}

.menu ul {
  list-style-type: none;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0rem 2rem 0rem 2rem;
}

.menu ul li {
  margin-bottom: 10px;
  padding: 10px;
}
</style>