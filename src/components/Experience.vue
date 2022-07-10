<template>
    <section>
        <div class="row ms-md-5">
            <div class="col ms-md-5">
                <div class="row ">
                    <div class="d-flex align-items-center">
                    <span>
                        <i @click="show = !show" class="fa fa-chevron-circle-down btn btn-outline-dark me-2"
                           aria-hidden="true"></i>
                    </span>
                        <h3><i class="fa fa-suitcase" aria-hidden="true"></i> Experience</h3>
                    </div>
                </div>


                <div class="ms-md-5 mt-3 p-3 bg-light bg-opacity-25 rounded-3" :class="{'d-none' : !show}">
                    <p class="font-small">
                        <i class="fa fa-circle" aria-hidden="true"></i> <b>IT support</b> - Local Elections | 17 and 31
                        October 2021
                    </p>
                    <p class="font-small">
                        <i class="fa fa-circle" aria-hidden="true"></i> <b>Student coordinator</b> - Code Academy | July
                        - September 2021
                    </p>
                </div>
            </div>

        </div>
    </section>
</template>


<script>
    export default {
        name: "Experience",
        data() {
            return {
                show: false
            }
        }
    }
</script>

<style scoped>

</style>