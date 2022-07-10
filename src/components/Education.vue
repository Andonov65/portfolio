<template>
    <section>
        <div class="row ms-md-5">
            <div class="col ms-md-5">
                <div class="row ">
                    <div class="d-flex align-items-center">
                    <span>
                        <i @click="show = !show" class="fa fa-chevron-circle-down btn btn-outline-dark me-2 "
                           aria-hidden="true"></i>
                    </span>
                        <h3><i class="fa fa-university" aria-hidden="true"></i> Education </h3>
                    </div>
                </div>

                <div class="ms-md-5 mt-3 p-3 bg-success bg-opacity-50 rounded-3" :class="{'d-none' : !show}">
                    <p  class="font-small">
                        <i class="fa fa-circle" aria-hidden="true"></i> <b>2019 - </b>in progress | Faculty of Computer
                        Science and Engineering on UKIM - Skopje
                    </p>
                    <p class="font-small">
                        <i class="fa fa-circle" aria-hidden="true"></i> <b>2015 - 2019</b> | Gymnasium High School
                        "Nikola Karev" - Skopje
                    </p>
                    <p class="font-small">
                        <i class="fa fa-circle" aria-hidden="true"></i> <b>2007 - 2015</b> | Elementary School "Kiril
                        Pejcinovikj"
                    </p>
                </div>
            </div>

        </div>


    </section>
</template>

<script>
    export default {
        name: "Education",
        data() {
            return {
                show: false
            }
        }
    }
</script>

<style scoped>

</style>