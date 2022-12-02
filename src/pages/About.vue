<template>
    <div>
        <Navbar />

        <section class="about">

            <h1 class="heading"> about <span>me</span> </h1>

            <div class="row">

                <div class="info-container">

                    <h1>personal info</h1>

                    <div class="box-container"> 

                        <div class="box">
                            <h3> <span>name : </span> Panadda Sawangphol </h3>
                            <h3> <span>age : </span> 20 </h3>
                            <h3> <span>email : </span> panadda.sawa@bumail.net </h3>
                            <h3> <span>address : </span> Chanthaburi, Thailand 22160 </h3>
                        </div>

                        <div class="box">
                            <h3> <span>Faculty of : </span> Engineering </h3>
                            <h3> <span>Department of : </span> Multimedia and Entertainment </h3>
                            <h3> <span>University : </span> Bangkok University </h3>
                            <h3> <span>language : </span> thai </h3>
                        </div>

                    </div>

                    <a href="/profilewithcss/files/resume.pdf" class="btn"> download CV <i class="fas fa-download"></i>
                    </a>

                </div>

                <div class="count-container">

                    <div class="box">
                        <h3>2013-2017</h3>
                        <p>Lambertpitchayalai School</p>
                    </div>

                    <div class="box">
                        <h3>2018-2020</h3>
                        <p>Siyanusorn School</p>
                    </div>

                    <div class="box">
                        <h3>2021-Present</h3>
                        <p>Bangkok University</p>
                    </div>

                    <div class="box">
                        <h3>5+</h3>
                        <p>Certificates</p>
                    </div>

                </div>

            </div>

        </section>

        <!-- about section ends -->

        <!-- skills section starts  -->

        <section class="skills">

            <h1 class="heading"> <span>my</span> skills </h1>

            <div class="box-container">
                <div class="box">
                    <img src="images/icon-1.png">
                    <h3>html</h3>
                </div>
                <div class="box">
                    <img src="images/icon-2.png">
                    <h3>css</h3>
                </div>
                <div class="box">
                    <img src="images/icon-3.png">
                    <h3>javascript</h3>
                </div>
                <div class="box">
                    <img src="images/icon-4.png">
                    <h3>sass</h3>
                </div>
                <div class="box">
                    <img src="images/icon-5.png">
                    <h3>angular</h3>
                </div>
                <div class="box">
                    <img src="images/icon-6.png">
                    <h3>react.js</h3>
                </div>
            </div>

        </section>

        <!-- skills section ends -->
    </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import axios from 'axios'

export default {
    components: { Navbar },
    methods: {
        async fetchExperience() {
            try {
                let res = await axios.get("https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/experiences")
                this.experiences = res.data
            } catch (error) {
                
            }
        }
    }
}
</script>

<style>

</style>