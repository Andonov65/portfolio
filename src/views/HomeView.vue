<template>
  <main class="bg-secondary bg-opacity-25 w-100">
    <div class="container pt-4">


      <div>
        <general-info/>
        <hr/>
        <education/>
        <hr/>
        <experience/>
        <hr/>
        <skills/>
        <hr/>
        <activities/>
        <hr/>
      </div>

      <div class="text-center pb-3">
        <h4>If you could give me a thumbs up for my CV I would be grateful:</h4>
        <div class="d-flex flex-row justify-content-between w-25 m-auto mt-4 mb-4">
          <button @click="likesClick" class="badge rounded-pill text-primary fa-2x"><i class="fa fa-thumbs-up fa-3x" aria-hidden="true"></i></button>
          <button @click="dislikesClicks" class="badge rounded-pill text-danger fa-2x"><i class="fa fa-thumbs-down fa-3x" aria-hidden="true"></i></button>
        </div>

        <p  class="text-white p-4 bg-black m-auto" style="width: 20%" >{{showAverageFromLikesAndDislikes}} people like this CV.</p>
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
export default {
  name: 'Home',
  components: {Activities, Skills, Experience, Education, GeneralInfo},
  data(){
    return{
      likes: 0,
      clicksCounter: 0
    }
  },
  methods: {
    likesClick(){
      this.clicksCounter++;
      return this.likes++;
    },
    dislikesClicks(){
      this.clicksCounter++;
      return this.likes--;
    }
  },
  computed: {
    showAverageFromLikesAndDislikes(){
      if(isNaN(parseFloat((this.likes/this.clicksCounter)*100))){
        return "0%";
      }
      if(parseFloat((this.likes/this.clicksCounter)*100)<=-100){
        return "-100%";
      }
      return parseFloat((this.likes/this.clicksCounter)*100).toFixed(0)+"%";
    }
  }
}
</script>
