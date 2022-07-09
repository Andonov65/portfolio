<template>
  <main style="overflow-x: hidden" class="bg-secondary bg-opacity-25 w-100 h-100">
    <div class="container pt-4">


      <div class="row">
        <general-info/>
        <hr/>
        <div class="col">
          <education/>
          <hr/>
          <experience/>
          <hr/>
          <skills/>
          <hr/>
          <activities/>
          <hr/>
        </div>
        <div class="col">
          <overall-rating/>
        </div>

      </div>

      <div class="row">
        <div class="col rounded-start bg-success p-1"></div>
        <div class="col bg-warning bg-opacity-50"></div>
        <div class="col bg-warning"></div>
        <div class="col bg-danger"></div>
        <div class="col bg-danger bg-opacity-50"></div>
        <div class="col bg-info bg-opacity-50"></div>
        <div class="col bg-primary"></div>
        <div class="col rounded-end bg-info"></div>
      </div>

      <div id="buttonRate" class="row">
        <div class="d-flex flex-row justify-content-center mt-4 mb-4">
          <button @click="showRateForm" class="btn btn-outline-dark fa-2x">Rate this CV</button>
        </div>

      </div>

      <div id="showDiv" class="pb-3" style="display: none">
        <h4 class="text-center ms-md-5">If you could give me a thumbs up for my CV I would be grateful:</h4>
        <div class="d-flex flex-row justify-content-center mt-4 mb-4">
          <button @click="likesClick" class="badge rounded-pill text-primary fa-2x"><i class="fa fa-thumbs-up fa-2x" aria-hidden="true"></i></button>
          <button @click="dislikesClicks" class="badge rounded-pill text-danger fa-2x"><i class="fa fa-thumbs-down fa-2x" aria-hidden="true"></i></button>
        </div>
        <div class="row d-flex justify-content-center">
          <div class="text-white p-4 col-10 col-md-6 col-lg-4 text-center bg-black" >{{showAverageFromLikesAndDislikes}} people like this CV.</div>
        </div>
       </div>
    </div>
  </main>

</template>

<script>



import GeneralInfo from "@/components/GeneralInfo";
import Education from "@/components/Education";
import Experience from "@/components/Experience";
import Skills from "@/components/Skills";
import Activities from "@/components/Activities";
import OverallRating from "@/components/OverallRating";
export default {
  name: 'Home',
  components: {OverallRating, Activities, Skills, Experience, Education, GeneralInfo},
  data(){
    return{
      likes: 0,
      clicksCounter: 0
    }
  },
  methods: {
    likesClick(){
      this.clicksCounter++;
      this.likes++;
    },
    dislikesClicks(){
      this.clicksCounter++;
    },
    showRateForm(){
      let buttonRate = document.getElementById("buttonRate");
      buttonRate.style.display = "none";

      let formRate = document.getElementById("showDiv")
      formRate.style.display = "block";
    }
  },
  computed: {
    showAverageFromLikesAndDislikes(){
      if(isNaN(parseFloat((this.likes/this.clicksCounter)*100))){
        return "0%";
      }

      return parseFloat((this.likes/this.clicksCounter)*100).toFixed(0)+"%";
    }
  }
}
</script>
