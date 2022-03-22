<template>
  <div id="app">
    <MyHeader />
  </div>
</template>

<script>
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";
import '@fortawesome/fontawesome-free/css/all.css';

import MyHeader from './components/MyHeader.vue'

export default {
  name: 'App',
  components: {
    MyHeader
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  overflow: auto;
}

</style>
