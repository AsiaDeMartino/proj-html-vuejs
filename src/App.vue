<template>
  <div id="app">
    <MyInfo  />
  </div>
</template>

<script>
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";
import '@fortawesome/fontawesome-free/css/all.css';

import MyInfo from './components/MyInfo.vue'

export default {
  name: 'App',
  components: {
    MyInfo
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
}

</style>
