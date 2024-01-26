<template>
  <HeaderNav /> 
  <ContentSec /> 
  <FooterSec />
</template>

<script>


import ContentSec from './components/ContentSec.vue'
import FooterSec from './components/FooterSec.vue'
import HeaderNav from './components/HeaderNav.vue'


export default {
  name: 'App',
  components: {
    HeaderNav,
    ContentSec,
    FooterSec
    },
  }


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
