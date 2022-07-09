<template>
    <section>
    <div class="row ms-md-5">
        <div class="col ms-md-5">
            <div class="row ">
                <div class="d-flex">
                    <span>
                        <i @click="myFunction" class="fa fa-chevron-circle-down btn btn-outline-dark me-2 mt-1" aria-hidden="true"></i>
                    </span>
                    <h2><i class="fa fa-suitcase" aria-hidden="true"></i>  Experience</h2>
                </div>
            </div>


            <div id="hideDivExp" class="ms-md-5 mt-3  p-3 bg-light bg-opacity-25 rounded-3"  style="display: none">
                <p >
                    <i class="fa fa-circle" aria-hidden="true"></i>  <b>IT support</b> - Local Elections | 17 and 31 October 2021
                </p>
                <p>
                    <i class="fa fa-circle" aria-hidden="true"></i>  <b>Student coordinator</b> - Code Academy | July - September 2021
                </p>
            </div>
        </div>

    </div>
    </section>
</template>



<script>
    export default {
        name: "Experience",
        methods:{
            myFunction() {
                let x = document.getElementById("hideDivExp");

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