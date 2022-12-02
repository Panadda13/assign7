<template>
    <div>
        <Navbar />
        <section class="home">
            <div class="image">
                <img src="images/profile.png" alt=""> 
            </div>
            <div class="content">
                <h3>{{name}}</h3>
                <span>{{motto}}</span>
                <p>{{content}}</p>
                <router-link to="/about" class="btn"> about me <i class="fas fa-user"></i> </router-link>
            </div>
        </section>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
export default {
    components: { Navbar },
    data() {
        return{
            name: 'Panadda Sawangphol',
            motto: 'The scariest thing in the world is getting something for nothing.',
            content: 'Studying at the Faculty of Engineering Department of Multimedia and Entertainment, 2nd year, Bangkok University'
        }
    },
    beforeMount() {
        this.fetchExperince()
    }
}
</script>

<style>

</style>