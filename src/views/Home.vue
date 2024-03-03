<template>
  <div id="overlay" @click="toggleNav" v-if="showNav"></div>
  <!-- <h3>Header</h3> -->
  <div
    class="hg-mobile-menu"
    style="display: none; background-color: rgb(119, 68, 99)"
  >
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

  <div class="row my-header hg-mobile-menu" style="">
    <h1 class="header">
      The Hidden Beauty <br />
      of the Hebrew Genealogies
    </h1>
  </div>
  <div class="my-paper">
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8 my-center">
        <h5><br /></h5>
        <h2>Harmonizing Old Testament Words and Numbers</h2>
        <h5><br /></h5>
        <p>
          Hidden Beauty offers to the Body of Christ a promising solution to a
          nagging and contentious Bible problem that has escaped explanation for
          two thousand years. The problem has to do with whether Shem's
          genealogy in Genesis 11 is complete or not, and if not, where and how
          many names are omitted. Historically, the Church has interpreted it as
          complete, but this view conflicts with numerous other Scriptures.
          Further, recent discoveries of huge numbers of cuneiform tablets
          testify to an earlier Flood date than is found by adding the numbers
          in Shem's genealogy. We propose that Shem's list has been shortened
          from 45-65 names to ten which means the Flood of Noah occurred nearer
          4000 BC than 2500 BC. This solution eliminates the many biblical
          conflicts, confirms recent cuneiform finds and comes with a book full
          of biblical support.
        </p>
        <p>
          <b>From the Executive Summary</b>
        </p>

        <a
          href="/The-Hidden-Beauty-of-the-Hebrew-Genealogies.pdf"
          target="_blank"
          download="The-Hidden-Beauty-of-the-Hebrew-Genealogies"
          ><button
            class="btn btn-primary"
            style="
              font-size: 2rem;
              color: rgb(119, 68, 99);
              background-color: white;
              border: 1px solid rgb(119, 68, 99);
            "
          >
            Download PDF

            <span class="glyphicon glyphicon-download"></span>
          </button>
        </a>
        <a href="/executive-summary"
          ><button
            class="btn btn-primary"
            style="
              font-size: 2rem;
              color: rgb(119, 68, 99);
              background-color: white;
              margin-left: 10px;
              border: 1px solid rgb(119, 68, 99);
            "
          >
            Read Here
            <span class="glyphicon glyphicon-book"></span>
          </button>
        </a>
      </div>
      <div class="col-sm-2"></div>
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8 my-center">
        <div id="about">
          <h1><br /></h1>
          <h2>About the Author:</h2>
          <img
            src="../assets/lloyd-anderson-picture.png"
            alt=""
            style="width: 20%"
          />
          <h3><b>Lloyd Anderson</b> <i style="color: gray"></i></h3>
          <p>
            Lloyd Anderson received his Masters in Theology from Dallas
            Theological Seminary in 1966. He was a pastor for many years, before
            founding the Mount Saint Helens Creation Center with his wife,
            Doris, in 1998. Lloyd’s passion for God’s word and determined
            vigilance for accuracy and truth shone through his seminars and
            guided tours on the importance of Mount St. Helens as example of the
            catastrophic processes likely taking place during the Biblical
            deluge, and he also traveled to churches throughout the region
            speaking about the truths of Biblical creation. He retired from
            MSHCC in 2014, and has been researching and writing on Hebrew
            genealogy and chronology since.
          </p>
        </div>
      </div>
      <div class="col-sm-2"></div>
    </div>
    <div>
      <h1><br /></h1>
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8">
        <p style="font-size: 1.3rem">
         The Hidden Beauty of Hebrew Genealogies: Harmonizing Old Testament Words and Numbers, Seventh Edition, 7/2022.  Frequent updates.  
Copyright © 2016, © 2017, © 2018, © 2019, © 2020, © 2021, © 2022 by Lloyd Tontz Anderson
All rights reserved.

        </p>
        <p style="font-size: 1.3rem">
        Unless otherwise indicated, all Scripture quotations are from The ESV® Bible (The Holy Bible, English Standard Version®), copyright © 2001 by Crossway, a publishing ministry of Good News Publishers.  Used by permission.  All rights reserved.  
 

        </p>
        <p style="font-size: 1.3rem">
         Scripture quotations marked CSB have been taken from the Christian Standard Bible®, Copyright © 2017 by Holman Bible Publishers. Used by permission.  Christian Standard Bible® and CSB® are federally registered trademarks of Holman Bible Publishers. 
        </p>
        <h3>Library of Congress Cataloging-in-Publication Data</h3>
        <p>
          Anderson, Lloyd Tontz The Hidden Beauty of Hebrew Genealogies / Lloyd
          Tontz Anderson
        </p>
      </div>
      <div class="col-sm-2"></div>
    </div>
    <div>
      <h1><br /><br /></h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      showNav: false,
    };
  },
  methods: {
    toggleNav() {
      this.showNav = !this.showNav;
    },
  },
};
</script>
