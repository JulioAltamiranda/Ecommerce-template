<template>
  <master :show="show">
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
  },
  data(){
    return{
      show:true
    }
  },
  mounted(){
    window.addEventListener('load',this.loading)
  },
  methods:{
    loading(){
      this.show=false
    }
  }
 
}
</script>

