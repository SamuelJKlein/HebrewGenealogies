<template>
 <div class="main-text col-sm-8" :style="sometimesFixed">
    <div v-html="chapterHtml"></div>
    <div class="row">
      <a
        style="font-size: 2rem; float: left"
        :href="previousUrl"
        class="col-sm-4"
        ><span class="glyphicon glyphicon-chevron-left"></span> Previous
      </a>
      <a style="font-size: 2rem; float: center" href="#" class="col-sm-4"
        >To Top
      </a>
      <a style="font-size: 2rem; float: right" :href="nextUrl" class="col-sm-4"
        >Next<span class="glyphicon glyphicon-chevron-right"></span
      ></a>
      <br /><br />
    </div>

    <p style="font-size: 14px">
   The Hidden Beauty of Hebrew Genealogies: Harmonizing Old Testament Words and Numbers, Seventh Edition, 7/2022.  Frequent updates.  
Copyright © 2016, © 2017, © 2018, © 2019, © 2020, © 2021, © 2022 by Lloyd Tontz Anderson
All rights reserved.

    </p>
  </div>
</template>

<script>
export default {
  props: ["chapterHtml", "previousUrl", "nextUrl"],
  computed: {
    sometimesFixed() {
      if (this.$store.state.showMenu) {
        return "position:fixed;";
      }
      return "";
    },
  },
  mounted() {
    let v = this;
    let touchableElement = document.querySelector("body");
    let touchstartX = null;
    let touchstartY = null;
    let touchendX = null;
    let touchendY = null;
    touchableElement.addEventListener(
      "touchstart",
      function (event) {
        touchstartX = event.changedTouches[0].screenX;
        touchstartY = event.changedTouches[0].screenY;
      },
      false
    );

    touchableElement.addEventListener(
      "touchend",
      function (event) {
        touchendX = event.changedTouches[0].screenX;
        touchendY = event.changedTouches[0].screenY;
        handleGesture();
      },
      false
    );

    function handleGesture() {
      if (touchendX + 80 < touchstartX) {
        console.log("pretty cool...");
        window.location.href = v.nextUrl;
      }

      if (touchendX > touchstartX + 80) {
        console.log("pretty cool... yeah");
        window.location.href = v.previousUrl;
      }

      if (touchendY < touchstartY) {
        console.log("Swiped Up");
      }

      if (touchendY > touchstartY) {
        console.log("Swiped Down");
      }

      if (touchendY === touchstartY) {
        console.log("Tap");
      }
    }
  },
};
</script>
   




