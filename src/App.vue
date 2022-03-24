<template>
  <div id="app">
    <MyHeader />
    <SectionUno />
    <SectionDue />
    <SectionTre />
    <SectionQuattro />
    <SectionCinque />
    <SectionSei />
    <MyFooter />
  </div>
</template>

<script>
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";
import '@fortawesome/fontawesome-free/css/all.css';

import MyHeader from './components/MyHeader.vue'
import SectionUno from './components/SectionUno.vue'
import SectionDue from './components/SectionDue.vue'
import SectionTre from './components/SectionTre.vue'
import SectionQuattro from './components/SectionQuattro.vue'
import SectionCinque from './components/SectionCinque.vue'
import SectionSei from './components/SectionSei.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    SectionUno,
    SectionDue,
    SectionTre,
    SectionQuattro,
    SectionCinque,
    SectionSei,
    MyFooter
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;900&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
  overflow-y: scroll;
  overflow-x: hidden ;
}

img {
    max-width: 100%;
    display: block;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

h1{
  font-weight: bold;
}

</style>
