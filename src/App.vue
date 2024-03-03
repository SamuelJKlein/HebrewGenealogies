<template>
  <link rel="stylesheet" :href="styleRef" />
  <the-header></the-header>

  <router-view />
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  components: { TheHeader },
  data() {
    return {
      currentStyle: false,
    };
  },
  methods: {
    toggleStyle() {
      this.currentStyle = !this.currentStyle;
    },
  },
  computed: {
    showMobileMenu() {
      var mobileSite = window.matchMedia("(max-width:780px)");
      if (mobileSite.matches) {
        return true;
      }
      return false;
    },
    styleRef() {
      if (this.currentStyle === true) {
        return "./science.css";
      } else {
        return "";
      }
    },
  },
  beforeCreate() {
  
   
  }
};
</script>
