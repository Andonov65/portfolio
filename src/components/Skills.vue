<template>
    <section>
        <div class="row ms-md-5">
            <div class="ms-md-5">
                <div class="row ">
                    <div class="d-flex">
                        <span>
                            <i @click="myFunction" class="fa fa-chevron-circle-down fa-2x btn btn-outline-dark me-2 mt-3" aria-hidden="true"></i>
                        </span>
                        <h2><i class="fa fa-cogs fa-2x" aria-hidden="true"></i>  Skills</h2>
                    </div>
                </div>

                <div id="hideDivSkill" class="ms-md-5 mt-3 h-25"  style="display: none" >
                    <ul class="row list-unstyled fs-5 col-11 col-md-12"  >
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  C/C++</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  JAVA</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  HTML5 & CSS3</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  Unity</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  Adobe Photoshop CS6/CS</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  Microsoft Office</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  Java Spring</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  ASP.NET / MVC</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  PostgreSQL</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  JavaScript</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  JQuery</li>
                        <li class="col-12 col-md-4"><i class="fa fa-check-circle-o" aria-hidden="true"></i>  Bootstrap</li>
                    </ul>
                </div>
            </div>

        </div>
    </section>
</template>


<script>
    export default {
        name: "Skills",
        methods:{
            myFunction() {
                let x = document.getElementById("hideDivSkill");

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