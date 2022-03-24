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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
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
