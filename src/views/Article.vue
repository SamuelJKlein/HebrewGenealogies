<template>
  <div id="read-page" class="row">
   {{  currentArticle  }}
  </div>
</template>

<script>



import notFound from "../chapters-html/not-found.js";
import articleOne from "../articles/article-one.js"
export default {

  data() {
    return {
    };
  },
  computed: {
    
   
    currentArticle() {
     switch (this.$route.params.chapterNumber) {
        case "one":
          return articleOne;
       

        default:
          console.log(this.$route.params.chapterNumber);
          console.log(notFound);

          return {
            html:
              "<h2 style='color:red;font-family:menlo'>/" +
              this.$route.params.chapterNumber +
              "</h2>" +
              notFound.html,
          };

       
      }
    },
  },
  
};
</script>