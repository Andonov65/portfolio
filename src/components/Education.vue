<template>
    <section>
    <div class="row ms-md-5">
        <div class="col ms-md-5">
            <div class="row ">
                <div class="d-flex">
                    <h2><i class="fa fa-university fa-2x" aria-hidden="true"></i>  Education </h2>
                    <span>
                        <i @click="myFunction" class="fa fa-chevron-circle-down fa-2x btn btn-outline-dark ms-2 mt-3" aria-hidden="true"></i>
                    </span>
                </div>
            </div>

            <div id="hideDivEdu" class="ms-md-5 mt-3" style="display: none">
                <p >
                    <i class="fa fa-circle" aria-hidden="true"></i>  <b>2019 - </b>in progress | Faculty of Computer Science and Engineering on UKIM - Skopje
                </p>
                <p>
                    <i class="fa fa-circle" aria-hidden="true"></i>  <b>2015 - 2019</b> | Gymnasium High School "Nikola Karev" - Skopje
                </p>
                <p>
                    <i class="fa fa-circle" aria-hidden="true"></i>  <b>2007 - 2015</b> | Elementary School "Kiril Pejcinovikj"
                </p>
            </div>
        </div>

    </div>


    </section>
</template>

<script>
    export default {
        name: "Education",
        methods:{
            myFunction() {
                let x = document.getElementById("hideDivEdu");

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