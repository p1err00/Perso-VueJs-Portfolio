<template>
  <Home/>
  <Resume/>
  <Competences/>
  <Projets/>
  <Contact/>
</template>

<script>
import Home from './components/Home.vue'
import Resume from './components/Resume.vue'
import Competences from './components/Competences.vue'
import Projets from './components/Projets.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    Home,
    Resume,
    Competences,
    Projets,
    Contact
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f8ca99;
  scroll-behavior: smooth;
}

</style>
