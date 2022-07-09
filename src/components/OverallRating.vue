<template>
    <section>
        <div class="row ms-lg-5">
            <div class="ms-lg-5">
                <div class="row ">
                    <div class="d-flex">
                         <span>
                            <i @click="myFunction" class="fa fa-chevron-circle-down fa-2x btn btn-outline-dark me-2 mt-3" aria-hidden="true"></i>
                         </span>
                        <h2><i class="fa fa-bars fa-2x" aria-hidden="true"></i>  Overall Rating and other skills</h2>
                    </div>
                </div>

                <div id="hideDivOtherSkill" class="ms-md-5 mt-3 h-25"  style="display: none" >
                    <ul class="row list-unstyled fs-5 col-12 col-lg-5"  >
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Time management</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Communication</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Adaptability</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Problem-solving</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Teamwork</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Creativity</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Patience</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Flexibility</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Attention to detail</li>
                        <li class="col-12"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>  Work ethic</li>
                    </ul>
                    <div class="row d-flex flex-row justify-content-center">
                        <div class="col">
                            <i class="fa fa-star fa-2x" aria-hidden="true"></i>
                            <i class="fa fa-star fa-2x" aria-hidden="true"></i>
                            <i class="fa fa-star fa-2x" aria-hidden="true"></i>
                            <i class="fa fa-star fa-2x" aria-hidden="true"></i>
                            <i class="fa fa-star-half-o fa-2x" aria-hidden="true"></i>
                        </div>

                    </div>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
    export default {
        name: "OverallRating",
        methods:{
            myFunction() {
                let x = document.getElementById("hideDivOtherSkill");

                if (x.style.display === "none") {
                    x.style.display = "block";
                } else {
                    x.style.display = "none";
                }
            }
        }
    }
</script>

<style scoped>

</style>