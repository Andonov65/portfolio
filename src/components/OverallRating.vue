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
                        <h3><i class="fa fa-bars" aria-hidden="true"></i> Overall Rating and other skills</h3>
                    </div>
                </div>

                <div class="ms-md-5 mt-3 p-3 bg-primary bg-opacity-25 rounded-3" :class="{'d-none' : !show}">
                    <ul class="row list-unstyled fs-5 col-12 col-lg-8">
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i> Time
                            management
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Communication
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Adaptability
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Problem-solving
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Teamwork
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Creativity
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Patience
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Flexibility
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i>
                            Attention to detail
                        </li>
                        <li class="col-12 font-small"><i class="fa fa-arrow-circle-o-right" aria-hidden="true"></i> Work
                            ethic
                        </li>
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
        data() {
            return {
                show: false
            }
        }
    }
</script>

<style scoped>

</style>