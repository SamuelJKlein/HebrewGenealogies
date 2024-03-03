<template>
  <div id="overlay" @click="toggleNav" v-if="showNav"></div>
  <!-- <h3>Header</h3> -->
  <div
    class="hg-mobile-menu"
    style=" background-color: rgb(119, 68, 99)"
  >
  <div v-if="showMobileMenu" class="">
    <i class="fas fa-bars"></i>
    <div
      id="chapterList"
      style="
        background-color: white;
        padding-left: 15px;
        font-size: 2.5rem;
        z-index: 9999 !important;
      "
    >
      <a class="chapter-list" href="/chapter-one">Chapter One</a>
      <br />
      <a href="/chapter-two">Chapter Two</a>
      <br />
      <a href="/chapter-three">Chapter Three</a>
      <br />
      <a href="/chapter-four">Chapter Four</a>
      <br />
      <a href="/chapter-five">Chapter Five</a>
    </div>
  </div> 
    <nav class="navbar navbar-default navbar-fixed-top">
      <div class="container-fluid">
        <!-- Overlay for when the mobile menu is open -->

        <!-- Title / show menu button for mobile -->
        <div
          class="navbar-header"
          style="
            border-bottom: solid rgb(119, 68, 99) 5px;
            background-color: white;
            height: 7rem;
          "
        >
          <a
            id="title-of-page"
            class="navbar-brand"
            style="color: black; background-color: white"
          >
            <a href="/" style="color: black">
              The Hidden Beauty of the Hebrew Genealogies</a
            >

            <i
              @click="toggleNav"
              class="fas fa-bars"
              style="margin-left: 2rem; float: right"
            ></i>
          </a>
        </div>

        <!-- show website navigation for mobile -->
        <div v-if="showNav" class="page-list nav navbar-nav">
          <div>
            <a href="/">Home</a>
          </div>
          <div><a href="/executive-summary">The Book</a></div>
          <div><a href="#about">About Author</a></div>
          <!-- <div>
            <a href="https://everythingintheworldexists.blogspot.com/">Blog</a>
          </div> -->
        </div>

        <!-- <div v-if="0 !== 0" class="nav navbar-nav">
          <li class="">
            <a class="chapter-list" href="/chapter-one">Chapter One</a>
          </li>
          <li><a href="/chapter-two">Chapter Two</a></li>
          <li><a href="/chapter-three">Chapter Three</a></li>
          <li><a href="/chapter-four">Chapter Four</a></li>
          <li><a href="/chapter-five">Chapter Five</a></li>
        </div> -->
      </div>
    </nav>
  </div>
  <!-- Line break so the menu doesn't cover the text -->
  <!-- <div class="hg-mobile-menu">
    
    <h2>
      <br />
    </h2>
  </div> -->

  <!-- <div
    class="jumbotron"
    style="
      background-image: url('https://repository.sbts.edu/bitstream/handle/10392/5735/752_5333.JPG?sequence=2&isAllowed=y');
      background-size: cover;
    "
  >
    <h1>HI THERE!</h1>
  </div> -->


  <div class="my-paper">
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8 my-center">
      <h3 class="hg-mobile-menu"> <br>

    </h3> 
   
    <ul style="list-style-type: none;">
    <li><h2>Articles <br>

    </h2></li>

      <li v-for="article in articleList" :key="article.url"> <a :href="article.url"> <h3>{{  article.name  }}</h3>
      <p>{{  article.description  }}</p> </a></li>
         
    </ul>
      </div>
      <div class="col-sm-3"></div>
    </div>
    
    <div>
      <h1><br /></h1>
    </div>
  
    <div>
      <h1><br /><br /></h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import articleList from '../articles/article-list.js'
export default {
  name: "Home",
  components: {},
  data() {
    return {
      showNav: false,
      articleList
    };
  },
  methods: {
    toggleNav() {
      this.showNav = !this.showNav;
    },
  },
};
</script>
