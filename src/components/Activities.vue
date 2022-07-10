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
                        <h3><i class="fa fa-bar-chart" aria-hidden="true"></i> Activities</h3>
                    </div>
                </div>

                <div class="ms-md-5 mt-3 p-3 bg-warning bg-opacity-25 rounded-3" :class="{'d-none' : !show}">
                    <ul class="list-unstyled fs-5">
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i> Participated in
                            KONTAKT MK as a member of SP FINKI
                        </li>
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i> Group project for
                            libraries and reading rooms. The link to the page:
                            <a class="text-decoration-none" href="https://dians-lab.herokuapp.com/home">Library
                                project</a> and several other similar projects that are locally on my computer
                        </li>
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i>
                            14.03.2021-16.03.2021 Participated in React training organized by EESTEC LC
                        </li>
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i> Attended
                            presentations organized by FEIT and Code and Meet
                        </li>
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i> One-day webinar on
                            Python organized by Brainster
                        </li>
                        <li class="font-small"><i class="fa fa-dot-circle-o" aria-hidden="true"></i> 2019 – ongoing
                            active participation in the Student Parliament of FINKI
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
    export default {
        name: "Activities",
        data() {
            return {
                show: false
            }
        }
    }
</script>

<style scoped>

</style>