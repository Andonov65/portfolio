<template>
    <section>
        <div class="row ms-md-5">
            <div class="col ms-md-5">
                <div class="row ">
                    <div class="d-flex">
                        <span>
                            <i @click="myFunction" class="fa fa-chevron-circle-down fa-2x btn btn-outline-dark me-2 mt-3" aria-hidden="true"></i>
                        </span>
                        <h2><i class="fa fa-bar-chart fa-2x" aria-hidden="true"></i>  Activities</h2>
                    </div>
                </div>

                <div id="hideDivActivity" class="ms-md-5 mt-3 h-50"  style="display: none">
                    <ul class="list-unstyled fs-5">
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  Participated in KONTAKT MK as a member of SP FINKI</li>
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  Group project for libraries and reading rooms. The link to the page:
                            <a href="https://dians-lab.herokuapp.com/home">Library project</a> and several other similar projects that are locally on my computer</li>
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  14.03.2021-16.03.2021 Participated in React training organized by EESTEC LC</li>
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  Attended presentations organized by FEIT and Code and Meet</li>
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  One-day webinar on Python organized by Brainster</li>
                        <li><i class="fa fa-dot-circle-o" aria-hidden="true"></i>  2019 – ongoing active participation in the Student Parliament of FINKI</li>
                    </ul>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
    export default {
        name: "Activities",
        methods:{
            myFunction() {
                let x = document.getElementById("hideDivActivity");

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