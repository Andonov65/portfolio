<template>
  <main style="overflow-x: hidden" class="bg-info bg-gradient bg-opacity-50 w-100 h-100">
    <div class="container pt-4">


      <div class="row">
        <general-info/>

        <div class="col-12 col-lg-6">
          <hr/>
          <education/>
          <hr/>
          <experience/>
          <hr/>
          <skills/>
        </div>
        <div class="col-12 col-lg-6">
          <hr/>
          <overall-rating/>
        </div>
      </div>
      <div class="row">
        <div class="col-12">
          <hr/>
          <activities/>
          <hr/>
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
        <div class="row d-flex justify-content-center">
          <div class="p-4 col-10 col-md-6 col-lg-4 text-center" v-html="showStarsFromLikesAndDislikes"></div>
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
      clicksCounter: 0,
      dislikes: 0
    }
  },
  methods: {
    likesClick(){
      this.clicksCounter++;
      this.likes++;
    },
    dislikesClicks(){
      this.clicksCounter++;
      this.dislikes++;
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
    },
    showStarsFromLikesAndDislikes(){
      if(parseFloat((this.likes/this.clicksCounter)*100)===0 || isNaN(parseFloat((this.likes/this.clicksCounter)*100))){
        return '<i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
      }else if(parseFloat((this.likes/this.clicksCounter)*100)<=20){
        if(parseFloat((this.likes/this.clicksCounter)*100)<=10){
          return '<i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
        }
        return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
      }else if(parseFloat((this.likes/this.clicksCounter)*100)<=40 && parseFloat((this.likes/this.clicksCounter)*100)>20){
        if(parseFloat((this.likes/this.clicksCounter)*100)<=30){
          return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
        }
        return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
      }else if(parseFloat((this.likes/this.clicksCounter)*100)<=60 && parseFloat((this.likes/this.clicksCounter)*100)>40){
        if(parseFloat((this.likes/this.clicksCounter)*100)<=50){
          return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
        }
        return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
      }else if(parseFloat((this.likes/this.clicksCounter)*100)<=80 && parseFloat((this.likes/this.clicksCounter)*100)>60){
        if(parseFloat((this.likes/this.clicksCounter)*100)<=70){
          return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
        }
        return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-o" aria-hidden="true"></i>';
      }else if(parseFloat((this.likes/this.clicksCounter)*100)<=100 && parseFloat((this.likes/this.clicksCounter)*100)>80){
        if(parseFloat((this.likes/this.clicksCounter)*100)===100){
          return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i>';
        }
        return '<i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star fa-2x" aria-hidden="true"></i><i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i>';
      }
    }
  },
  watch: {
    likes(){
        console.log("Like clicked, number of likes: " + this.likes);
    },
    dislikes(){
        console.log("Dislike clicked, number of dislikes: " + (this.dislikes));
    }
  }
}
</script>
