<template>
  <div id="app">
    <MyHeader />
    <SectionUno />
    <SectionDue />
    <SectionTre />
    <SectionQuattro />
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

export default {
  name: 'App',
  components: {
    MyHeader,
    SectionUno,
    SectionDue,
    SectionTre,
    SectionQuattro,
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

</style>
