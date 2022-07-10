<template>
    <section>
        <div class="row ms-md-5">
            <div class="ms-md-5">
                <div class="row ">
                    <div class="d-flex align-items-center">
                        <span>
                            <i @click="show = !show" class="fa fa-chevron-circle-down btn btn-outline-dark me-2"
                               aria-hidden="true"></i>
                        </span>
                        <h3><i class="fa fa-cogs" aria-hidden="true"></i> Skills</h3>
                    </div>
                </div>

                <div class="ms-md-5 mt-3 p-3 bg-info bg-opacity-25 rounded-3" :class="{'d-none' : !show}">
                    <ul class="row list-unstyled fs-5 col-11 col-md-12">
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            C/C++
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            JAVA
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            HTML5 & CSS3
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            Unity
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            Adobe Photoshop CS6/CS
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            Microsoft Office
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            Java Spring
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            ASP.NET / MVC
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            PostgreSQL
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            JavaScript
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            JQuery
                        </li>
                        <li class="col-12 col-md-4 font-small"><i class="fa fa-check-circle-o" aria-hidden="true"></i>
                            Bootstrap
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </section>
</template>


<script>
    export default {
        name: "Skills",
        data() {
            return {
                show: false
            }
        }
    }
</script>

<style scoped>

</style>