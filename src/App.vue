<template>
  <master>
    <template slot="header">
      <headerComponent/>
    </template>
    <template slot="main">
      <mainComponent/>
    </template>
    <template slot="footer">
      <footerComponent/>
    </template>
  </master>
</template>

<script>

import master from './components/layout/Master'
import headerComponent from './components/Header'
import mainComponent from './components/Main'
import footerComponent from './components/Footer'
export default {
  components:{
    master,
    headerComponent,
    mainComponent,
    footerComponent
  }
 
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
